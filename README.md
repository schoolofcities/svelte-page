# Svelte + Vite + GitHub Pages

This template should help get you started developing with Svelte in Vite and host via GitHub Pages

First create a repository from scratch, or navigate into an existing one. 

Then build a basic Svelte app (if not copying from another)

```
npm init vite . -- --template svelte
```

Install required node packages
```
npm install
```

View/testing on localhost:
```
npm run dev
```

Building for production
```
npm run build
```

Then remove `/dist` from `.gitignore` (I just do this manually)

Add the repo name to `vite.config.js`

```
export default defineConfig({
  base: "/REPO-NAME/",
  plugins: [svelte()]
})
```

Then commit and push these changes
```
git add -A
git commit -m "include dist, update vite.config.js
git push
```

Then push the dist folder into a subtree activating gh-pages
```
git subtree push --prefix dist origin gh-pages
```

