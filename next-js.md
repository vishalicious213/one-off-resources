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
