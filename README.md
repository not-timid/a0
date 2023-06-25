# a0

__NOT-TIMID Alpha 0 - trying out the current stable version of Next.js, 13.4.7__

https://not-timid.com/

This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Steps to build this demo

Following the guide <https://nextjs.org/docs/getting-started/installation>:

1. `node --version` is `v16.20.0`, which is >= Node.js 16.8
2. `npx create-next-app@latest`:
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
   Creating a new Next.js app in /Users/richplastow/Work/2023-Work/NOT-TIMID/not-timid.github.io/not-timid.

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

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.
