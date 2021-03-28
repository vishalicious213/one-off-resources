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

