# Next.JS setup

## CREATE LOCAL PROJECT
1. Install [Node.JS](https://nodejs.org/en/) if its not installed
2. Create a Next.JS app
    * Go to the folder where you want the app's subfolder to be created
    * `npx create-next-app appFolderName` (give the app's folder a name)
3. Run the development server so you can see the app in the browser
    * `npm run dev`
    * Open your browser and go to `localhost:3000` to view app

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
For example, my path might be: 
`git remote add origin https://github.com/vishalicious213/temp.git`

Scroll up, click on your repo's name, after your username and see the new repo.

## SETUP INITIAL PAGES
Files in the `/pages` folder will automatically have routing built into them. Subfolders in `/pages` will also have routing built in. For example, `localhost:3000/index` will open `index.js` if its in `/pages` and `localhost:3000/contact` will open `contact.js` if its in `/pages`.

1. Open the project in VS Code
2. Go to the `pages` folder and open index.js
3. Delete everything nested inside of \<main>
4. Add a temporary element in \<main>, like an \<h1> with the page's name so you know what page you're on when you navigate to it
5. Copy index.js for use as temporary boilerplate
6. Make a new page in the `pages` folder, for example `contact.js`
7. Paste the contents of index.js into the new page and change the name of the function from `Home` to something more appropriate to the page
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
        <a
          href="https://vercel.com?utm_source=create-next-app&utm_medium=default-template&utm_campaign=create-next-app"
          target="_blank"
          rel="noopener noreferrer"
        >
          Powered by{' '}
          <img src="/vercel.svg" alt="Vercel Logo" className={styles.logo} />
        </a>
      </footer>
    </div>
  )
}
```

## SETUP NAVIGATION
Create a `components` directory and create a navigation component that can be imported into each page after initial pages are set up in above steps (additional pages can also be added to the navigation afterwards, naturally).
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
`Link` enables client-side navigation using JavaScript. The browser does not reload the page. `Link` components are prefetched, so they are loaded in the background for faster render.
* Use the `Link` component from `next/link` as an \<a>. For example:
```javascript
import Link from 'next/link'

export default Nav() {
    return (
        <nav>
            <Link href='/'><a>Home</a></Link>
            <Link href='/about'><a>About</a></Link>
            <Link href='/services'><a>Services</a></Link>
            <Link href='/contact'><a>Contact</a></Link>
        </nav>
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

## ADD STYLES
* Stylesheets should go in the /styles folder
* Next.JS uses CSS Modules, so stylesheet files should end in `.module.css`
* When we __import__ the stylesheet, we give it a name in the given component

For example, this could be `about.module.css`:
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
We could name it anything we want, but _aboutStyles_ seemed self-explanatory.