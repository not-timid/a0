# a0

__NOT-TIMID Alpha 0: A minimal 'Coming Soon' page, bootstrapped with__
__`create-next-app` 13.4.7__

⊖ __Version:__ 0.0.0  
⊖ __Repo:__ <https://github.com/not-timid/a0>  
⊖ __URL:__ <https://not-timid.com/a0/>

---

## Tech stack

This is a [Next.js](https://nextjs.org/) project bootstrapped with
[`create-next-app`
](https://github.com/vercel/next.js/tree/canary/packages/create-next-app). For
more about Next.js:

- [Next.js Documentation](https://nextjs.org/docs)
- [Learn Next.js](https://nextjs.org/learn)
- [The Next.js GitHub repository](https://github.com/vercel/next.js/)

---

## Set up the project

### __Set up your development machine__

1. Check your __Git__ version:  
   `git --version # should be 'git version 2.20.1' or greater`
2. Check your __Node__ version:  
   `node --version # should be 'v16.8.0' or greater`  
   Node 16.8.0 is the minimum specified by [the Next.js 'installation' docs
   ](https://nextjs.org/docs/getting-started/installation)
3. Check your __VS Code__ version:  
   `code --version # should be '1.79.0' or greater`
4. In VS Code, install and enable the [`dnamsons.kimbie-dark-plus`
   ](https://marketplace.visualstudio.com/items?itemName=dnamsons.kimbie-dark-plus)
   theme

### __Set up the repo locally__

Clone the repository, and `cd` into it:  
`git clone https://github.com/not-timid/a0.git && cd a0`

Install the dependencies:  
`npm i`

Open the `a0` repo in VS Code:  
`code .`

---

## Handy dev commands

Serve a development build of the app locally, with hot-reloading:  
`npm run dev`

Use ESLint to check for problems with JavaScript code:  
`npm run lint`

Build the app to the docs/ folder:  
`npm run build`

Serve the build locally:  
`npm run start`

---

## Steps to build this demo

1. `npx create-next-app@latest` to set up everything automatically
   ```
   Need to install the following packages:
     create-next-app@13.4.7
   Ok to proceed? (y) y
   ? What is your project named? not-timid
   ? Would you like to use TypeScript with this project? › No / Yes [Yes]
   ? Would you like to use ESLint with this project? › No / Yes [Yes]
   ? Would you like to use Tailwind CSS with this project? › No / Yes [No]
   ? Would you like to use `src/` directory with this project? › No / Yes [Yes]
   ? Use App Router (recommended)? › No / Yes [Yes]
   ? Would you like to customize the default import alias? › No / Yes [No]
   Creating a new Next.js app in [-path-to-current-directory-]/not-timid.

   Using npm.
   
   Initializing project with template: app 
   
   
   Installing dependencies:
   - react
   - react-dom
   - next
   - typescript
   - @types/react
   - @types/node
   - @types/react-dom
   - eslint
   - eslint-config-next


   added 291 packages, and audited 292 packages in 42s
   
   116 packages are looking for funding
     run `npm fund` for details
   
   5 moderate severity vulnerabilities
   
   To address all issues, run:
     npm audit fix
   
   Run `npm audit` for details.
   Success! Created not-timid at [-path-to-current-directory-]/not-timid
   ```
   ...note that node_modules/ is ~277 MB for 14,533 items
2. As described in [the 'basePath' docs,
   ](https://nextjs.org/docs/app/api-reference/next-config-js/basePath),
   [the 'distDir' docs,
   ](https://nextjs.org/docs/app/api-reference/next-config-js/distDir) and
   [the 'deploying' docs,
   ](https://nextjs.org/docs/app/building-your-application/deploying/static-exports)
   change:
   ```js
   const nextConfig = {}
   ```
   in next.config.js, to:
   ```js
   const nextConfig = {
     // Optional: Change the build app's base path `` -> `/a0`
     basePath: '/a0',
     // Optional: Change the output directory `out` -> `docs`
     distDir: 'docs',
     // Optional: Enable a static export
     output: 'export',
   }
   ```
3. Add a `"description"` to package.json, and change the `"version"` from
   `"0.1.0"` to `"0.0.0"` (for Alpha 0)
4. `npm run dev` to start the development server
   ```
   > not-timid@0.0.0 dev
   > next dev
   
   - ready started server on 0.0.0.0:3000, url: http://localhost:3000
   We detected TypeScript in your project and reconfigured your tsconfig.json
   file for you. Strict-mode is set to false by default.
   
   The following suggested values were added to your tsconfig.json. These values
   can be changed to fit your project's needs:
   
             - include was updated to add 'docs/types/**/*.ts'
   
   - event compiled client and server successfully in 640 ms (20 modules)
   - wait compiling...
   - event compiled client and server successfully in 232 ms (20 modules)
   ```
   ...note that there is no .next/ folder yet
5. Open http://localhost:3000/a0 _NOT http://localhost:3000 as suggested,_
   to see the default Next.js page.  
   ...note that .next/ is ~70 MB for 57 items
6. For the time being, replace the contents of the two .css files in src/app/
   with something more minimal
7. Remove references to the 'Inter' font from src/app/layout.tsx
8. Change the `title` and `description` in src/app/layout.tsx
9. Replace the content of src/app/page.tsx and delete the two `import`s
10. Create 256x256, 48x48, 32x32 and 16x16 GIFs
11. `convert *.gif favicon.ico` and replace Next.js's default
    src/app/favicon.ico
12. Control-C to stop `npm run dev`
13. `npm run lint` and make sure there are no errors
14. Delete the public/ folder (the two .svg files are not needed)
15. Change the `"build"` script in package.json to:  
    `"next build && touch docs/.nojekyll"`  
    We need to add a docs/.nojekyll file at this point because:
    - When `next build` starts running, it empties the docs/ folder
    - GitHub Pages usually ignores underscore-prefixed folders, like docs/_next/
    - The special docs/.nojekyll file overrides that GitHub Pages behavior
16. `npm run build` and wait for the docs/ folder to fill up:
    ```
    > not-timid@0.0.0 build
    > next build
    
    - info Creating an optimized production build  
    - info Compiled successfully
    - info Linting and checking validity of types ...(node:11402)
      [ESLINT_PERSONAL_CONFIG_SUPPRESS] DeprecationWarning: ...
    (Use `node --trace-deprecation ...` to show where the warning was created)
    - info Linting and checking validity of types  
    - info Collecting page data  
    - info Generating static pages (4/4)
    - info Finalizing page optimization  
    
    Route (app)                                Size     First Load JS
    ┌ ○ /                                      0 B                0 B
    └ ○ /favicon.ico                           0 B                0 B
    + First Load JS shared by all              77.6 kB
      ├ chunks/769-fd0a62696b61f5c4.js         25.3 kB
      ├ chunks/bce60fc1-49ee79ad31766ac6.js    50.5 kB
      ├ chunks/main-app-0c47c9e29c6a23eb.js    216 B
      └ chunks/webpack-0e9befa4c9ed903b.js     1.64 kB
    
    Route (pages)                              Size     First Load JS
    ─ ○ /404                                   182 B          74.7 kB
    + First Load JS shared by all              74.5 kB
      ├ chunks/framework-8883d1e9be70c3da.js   45 kB
      ├ chunks/main-cdf6ebeb4c274dc4.js        27.7 kB
      ├ chunks/pages/_app-998b8fceeadee23e.js  195 B
      └ chunks/webpack-0e9befa4c9ed903b.js     1.64 kB
    
    ○  (Static)  automatically rendered as static HTML (uses no initial props)
    ```
17. Change the `"start"` script in package.json from `"next start"` to
    `"npx serve@latest"`, because
    `"next start" does not work with "output: export" configuration`
18. Add the `"prestart": "mv docs a0",` script to package.json
19. And add the `"poststart": "mv a0 docs",` script
20. `npm start`, which may prompt you to install the `serve` package:
    ```
    Need to install the following packages:
    serve@14.2.0
    Ok to proceed? (y) y
    ```
    ...and check that http://localhost:3000/a0/ works ok
21. Control-C, and check that docs/ looks ready to deploy to GitHub Pages
