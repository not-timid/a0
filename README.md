# a0

__NOT-TIMID Alpha 0 - trying out the current stable version of Next.js, 13.4.7__

https://not-timid.com/

This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

---

## Steps to build this demo

1. `node --version` is `v16.20.0`, which is greater than the minimum stated in
   [the 'installation' docs, Node.js 16.8
   ](https://nextjs.org/docs/getting-started/installation)
2. `npx create-next-app@latest` to set up everything automatically
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
3. As described in [the 'basePath' docs,
   ](https://nextjs.org/docs/app/api-reference/next-config-js/basePath),
   [the 'distDir' docs,
   ](https://nextjs.org/docs/app/api-reference/next-config-js/distDir) and
   [the 'deploying' docs,
   ](https://nextjs.org/docs/app/building-your-application/deploying/static-exports)
   change:  
   `const nextConfig = {}` in next.config.js  
   ...to...  
   ```
   const nextConfig = {
     // Optional: Change the build app's base path `` -> `/a0`
     basePath: '/a0',
     // Optional: Change the output directory `out` -> `docs`
     distDir: 'docs',
     // Optional: Enable a static export
     output: 'export',
   }
   ```
4. `npm run dev` to start the development server
   ```
   > not-timid@0.1.0 dev
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
5. Open http://localhost:3000/a0 _NOT http://localhost:3000 as suggested,_ to
   see the default Next.js page.  
   ...note that .next/ is ~70 MB for 57 items
6. For the time being, replace the contents of the two .css files in src/app/
   with something more minimal
7. Remove references to the 'Inter' font from src/app/layout.tsx
8. Change the `title` and `description` in src/app/layout.tsx
9. Replace the content of src/app/page.tsx and delete the two `import`s
10. Create 256x256, 48x48, 32x32 and 16x16 GIFs
11. `convert *.gif favicon.ico` and replace Next.js's default src/app/favicon.ico
12. Control-C to stop `npm run dev`
13. `npm run lint` and make sure there are no errors
14. `npm run build` and wait for the docs/ folder to fill up:
    ```
    > not-timid@0.1.0 build
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
      └ chunks/webpack-be906ccf662ec045.js     1.64 kB
    
    Route (pages)                              Size     First Load JS
    ─ ○ /404                                   182 B          74.7 kB
    + First Load JS shared by all              74.5 kB
      ├ chunks/framework-8883d1e9be70c3da.js   45 kB
      ├ chunks/main-6a050bdd50e19c45.js        27.7 kB
      ├ chunks/pages/_app-998b8fceeadee23e.js  195 B
      └ chunks/webpack-be906ccf662ec045.js     1.64 kB
    
    ○  (Static)  automatically rendered as static HTML (uses no initial props)
    ```
15. `mv docs a0` to temporarily rename the 'docs/' folder to 'a0/'
16. `static-server --version`, or globally install this handy NPM module
17. `static-server` and check that http://localhost:9080 works ok
18. Control-C and `mv a0 docs` ready for GitHub Pages to deploy
19. `touch docs/.nojekyll` so that GitHub Pages dows not ignore the
    underscore-prefixed folder 'docs/_next/'

---

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js
  features and API
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial

You can check out [the Next.js GitHub repository
](https://github.com/vercel/next.js/) - your feedback and contributions are
welcome!
