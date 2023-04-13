# mrizkiaiman-turborepo

Generate project template by running the following command:

```sh
npx mrizkiaiman-create-app turborepo projectName
```

## What's inside?

This Turborepo includes the following packages/apps:

### **Main Stack**

- **`Next.js`**
- **`TypeScript`**
- **`Tailwind CSS`** (update the config at `packages/configs/tailwind/tailwind.config.js`)

### **Apps and Packages**

- `docs`: a [Next.js](https://nextjs.org/) app
- `web`: another [Next.js](https://nextjs.org/) app
- `ui`: a stub React component library shared by both `web` and `docs` applications
- `eslint-config-custom`: `eslint` configurations (includes `eslint-config-next` and `eslint-config-prettier`)
- `tsconfig`: `tsconfig.json`s used throughout the monorepo
- `configs`: `tailwind` config that used for styling (you can put any kind of shared config here)

### **Utilities**

This Turborepo has some additional tools already setup for you:

- [TypeScript](https://www.typescriptlang.org/) for static type checking
- [ESLint](https://eslint.org/) for code linting
- [Prettier](https://prettier.io) for code formatting

## Build

To build all apps and packages, run the following command:

```
cd my-turborepo
pnpm build
```

## Development

To develop all apps and packages, run the following command:

```
cd my-turborepo
pnpm dev
```

## Remote Caching

Turborepo can use a technique known as [Remote Caching](https://turbo.build/repo/docs/core-concepts/remote-caching) to share cache artifacts across machines, enabling you to share build caches with your team and CI/CD pipelines.

By default, Turborepo will cache locally. To enable Remote Caching you will need an account with Vercel. If you don't have an account you can [create one](https://vercel.com/signup), then enter the following commands:

```
cd mrizkiaiman-turborepo
npx turbo login
```

This will authenticate the Turborepo CLI with your [Vercel account](https://vercel.com/docs/concepts/personal-accounts/overview).

Next, you can link your Turborepo to your Remote Cache by running the following command from the root of your Turborepo:

```
npx turbo link
```
