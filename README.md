# Nx Deno cheetah <img alt="cutest logo ever" src='https://raw.githubusercontent.com/azurystudio/cheetah/dev/.github/cheetah.svg' width='32px' />

![cheetah love bagde](https://img.shields.io/badge/%E2%99%A5%EF%B8%8F-white?style=flat-square&label=cheetah&labelColor=824561)

✨ **This workspace has been generated by [Nx, a Smart, fast and extensible build system.](https://nx.dev)** ✨

Example repo of nx monorepo with [cheetah](https://github.com/azurystudio/cheetah)(deno) backend server and example extension for it.
Example extension simply adds `x-powered-by` header to the response.

### Create new nx monorepo

```bash
npx create-nx-workspace@latest <workspace-name>
```

### Create Deno App and library

Before creating nx apps/libs we have to install `@nx/deno` package

```bash
yarn add -D @nx/deno

nx list @nx/deno # Run to list capabilities of @nx/deno
```

To create Deno application:

```bash
nx g @nx/deno:app
```

To create Deno library:

```bash
nx g @nx/deno:lib
```

## Deploy!

### Deno Deploy

In order to deploy your cheetah app on [Deno Deploy](https://deno.com/deploy) you have to create new project.

Then you can add Git Integration by selecting your cheetah monorepo repository -> Automatic mode -> Select your server entry file `apps/cheetah-backend/src/mod.ts`

Or you can deploy it from CLI as well!

First of all you have to setup deploy config, run following command to do so

```bash
nx g @nx/deno:setup-deploy --site <your-deno-deploy-project-name>
```

Then run deploy command on your your project by specyfing preview or production environment and passing access token.

```bash
nx run cheetah-backend:deploy:<preview | production> --token=<your access token from deno deploy dashboard>
```
