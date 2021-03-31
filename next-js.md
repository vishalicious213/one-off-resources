# Next.JS setup

## CREATE LOCAL PROJECT
1. Install [Node.JS](https://nodejs.org/en/) if its not installed
2. Create a Next.JS app
    * Go to the folder where you want the app's subfolder to be created
    * `npx create-next-app appFolderName` (give the app's folder a name)
3. Navigate into the app's subfolder and run the development server so you can see the app in the browser
    * `npm run dev`
    * Open your browser and go to `localhost:3000` to view the app

## CREATE GITHUB REPO
1. Log into [GitHub](https://github.com/new) and click the `+` on the top-right and choose `New repository`
2. Give the repo a name (in the "Repository name" field)
3. Select "Public" or "Private"
4. Leave the readme, gitignore and license blank
5. Click `Create repository`
6. A new page will load with repo setup instructions. Follow the ones labeled "...or create a new repository on the command line"
```
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/[your user name]/[repo name].git
git push -u origin main
```
* The above will initialize a repo, stage all files in the repo's local directory and push them to the main branch on GitHub
* For example, my path might be: 
    `git remote add origin https://github.com/vishalicious213/test-repo.git`
* Don't use capital letters in your repo's name. Its not allowed on GitHub anymore

Scroll up, click on your repo's name, after your username and see the new repo.

## SETUP INITIAL PAGES
Files in the `/pages` folder will automatically have routing built into them. Subfolders in `/pages` will also have routing built in. 

For example:
* `localhost:3000/index` will open `index.js` if its in `/pages`
* `localhost:3000/contact` will open `contact.js` if its in `/pages`
* `localhost:3000/blog/post1` will open `/blog/post1.js` if its in `/pages`

### STEPS:

1. Open the project in VS Code
2. Go to the `pages` folder and open index.js
3. Delete everything nested inside of \<main>
4. Add a temporary element in \<main>, like an \<h1> with the page's name, so you know what page you're looking at when you navigate to it
5. Copy `index.js` for use as temporary boilerplate
6. Make a new page in the `pages` folder, for example `contact.js`
7. Paste the contents of `index.js` into the new page and
    * change the name of the function from `Home` to something more appropriate to the page
    * change the content of the \<h1> or other temporary element to something that identifies the page
8. Repeat steps 6 & 7 for any additional pages

Here's a template for ease of use:
```javascript
import Head from 'next/head'
import styles from '../styles/Home.module.css'

export default function Home() {
  return (
    <div className={styles.container}>
      <Head>
        <title>Project or page name goes here</title>
        <link rel="icon" href="/favicon.ico" />
      </Head>

      <main className={styles.main}>
        <h1 className={styles.title}>HOME PAGE</h1>
      </main>

      <footer className={styles.footer}>
        Footer Goes Here
      </footer>
    </div>
  )
}
```

## SETUP NAVIGATION
Create a `components` directory on the same level as `public` and `pages` and create a navigation component in it that can be imported into each page after initial pages are set up in above steps (additional pages can also be added to the navigation afterwards).
* JavaScript files in the `pages` folder or its subfolders use their filename as the URL path
* Pages are React components exported from a file in the `pages` directory
* Page routes are based on their file name, so:
    * `pages/index.js` uses the `/` route
    * `pages/about.js` uses `/about` as its route
    * `pages/products/hat` uses `/products/hat` as its route
* Page components can have any name but must be exported as default. For example:
```javascript
export default function Hat() {
    return <h2>Buy this hat!</h2>
}
```

### Link component
* `Link` enables client-side navigation using JavaScript. The browser does not reload the page. 
* `Link` components are prefetched, so they are loaded in the background for faster render.
* Use the `Link` component from `next/link` as an \<a>. For example:

```javascript
import Link from 'next/link'

export default Nav() {
    return (
        <nav id='menu'>
            <Link href='/'><a>Home</a></Link>
            <Link href='/about'><a>About</a></Link>
            <Link href='/services'><a>Services</a></Link>
            <Link href='/contact'><a>Contact</a></Link>
        </nav>

        <style jsx>
          {`
            #menu {
              width: 50%;
              display: flex;
              justify-content: space-between;
              margin: 0 auto;
            }
          `}
        </style>
    )
}
```

Import the nav component into any pages that need it and render it. For example, at the top of index.js, include:
```javascript
import Nav from '../components/nav'
```
And somewhere in the body, probably at the top, above \<main> add:
```javascript
<Nav />
```

## ADD STATIC FILES (images, documents, etc.)
* Static files - like images - are served from the top-level `public` directory
* These files are referenced from the root of the application, like `pages`. For example:
```javascript
<img src='/hero-image.jpg ' alt='Schecter Stiletto Studio 5L Bass' className={aboutStyles.hero}/>
```
* `/hero-image.jpg` would reside in the `public` directory

## CUSTOMIZE EACH PAGE'S \<Head>
* Modify a page's metadata through the <Head> component (note the capital 'H')
```javascript
import Head from 'next/head'
```
```javascript
<Head>
    <title>About Us | Website Name</title>
</Head>
```

# Next.JS STYLING

## STYLING OPTION 1 - INCLUDE STYLES IN COMPONENT
1. In the component's JSX, include an element called `style` with an attribute called `jsx` and wrap its contents with curly braces and backticks.
2. This is usually done at the bottom of the JSX, after all of the content.
3. This type of style cannot include core html elements, like `div`. It can include __classes__ & __ids__.
4. Use this type of styling for elements with __conditional styling__. For example, elements that use JavaScript to add/remove classes. It can be combined with other styling methods.

```javascript
<style jsx>
  {`
    .button {
      border: 1px solid white;
      color: black;
    }
  `}
</style>
```

## STYLING OPTION 2 - ADD STYLES WITH CSS MODULES
* Stylesheets should go in the /styles folder
* Next.JS uses __styled-jsx__, a CSS-in-JS library, so stylesheet files should end in `.module.css`
* SASS support is built-in
* When we _import_ a stylesheet, we give it a name in the given component

For example, this file could be `about.module.css`:
```css
.hero {
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;
}

.info {
    margin: 3rem auto;
    padding: 0;
    width: 80%;
}
```
In the imports section at the top of `about.js` we could import that file, and name it at the same time like this:
```javascript
import aboutStyles from '../styles/about.module.css'
```
We could name it/import it as anything we want, but _aboutStyles_ seems self-explanatory. When adding classes to elements in the __about page__ we have to remember to include `aboutStyles` in the className, along with the name of the class.
```javascript
<section className={aboutStyles.hero}>
    ...
</section>
```

Multiple classes can be added to an element like this:
```javascript
<div className={`${aboutStyles.info} ${aboutStyles.anotherClass}`}>
    ...
</div>
```

## STYLING OPTION 3 - ADD GLOBAL CSS IN `pages/_app.js`

* Global styles are loaded on every page from `pages/_app.js`.
* `App` is the top-level component common to all pages. It can keep state when navigating between pages.

To load [global CSS](https://nextjs.org/docs/basic-features/built-in-css-support#adding-a-global-stylesheet) files, create `pages/_app.js` like this and __restart the development server__ with `npm run dev`:

```javascript
export default function App({ Component, pageProps }) {
  return <Component {...pageProps} />
}
```

__** `pages/_app.js` is the only file that global CSS files can be imported from. They cannot be imported from anywhere else. **__

* The global css file can be placed anywhere and named anything
* In general, create a `styles` folder and a `global.css` file
* The file must be imported into `pages/_app.js`

```javascript
import '../styles/global.css'

export default function App({ Component, pageProps }) {
  return <Component {...pageProps} />
}
```