# Gatsby 1.0 starter
[![XO code style](https://img.shields.io/badge/code_style-XO-5ed9c7.svg)](https://github.com/sindresorhus/xo)
[![Build Status](https://travis-ci.org/fabien0102/gatsby-starter.svg?branch=master)](https://travis-ci.org/fabien0102/gatsby-starter)
[![Build status](https://ci.appveyor.com/api/projects/status/k06pajqcm23lay1s/branch/master?svg=true)](https://ci.appveyor.com/project/fabien0102/gatsby-starter/branch/master)

Demo: https://fabien0102-gatsby-starter.netlify.com/
Storybook: https://fabien0102-gatsby-starter.netlify.com/docs/

Gatsby 1.0 starter for generate awesome static website working with a nice env development.

## Warning

This starter is currently in wip (see progression to #What's inside session).

## Getting started

Install this starter (assuming Gatsby is installed) by running from your CLI: 

```bash
$ gatsby new my-website https://github.com/fabien0102/gatsby-starter
```

Run `yarn start` (or press `F5` if you are on VSCode) to hot-serve your website on http://localhost:8000.

Run `yarn build` to create static site ready to host (`/public`)

## What's inside?

- [ ] Gatsby 1.0 (alpha)
  - [x] sharp
  - [x] offline support
  - [ ] google analytics
  - [x] manifest
  - [x] typescript
  - [x] blog in markdown
- [x] Best practices tools
  - [x] [Jest](https://facebook.github.io/jest/) / [Enzyme](http://airbnb.io/enzyme/)
  - [x] [Storybook](https://storybooks.js.org/)
  - [x] [Typescript](https://www.typescriptlang.org/) / [tslint](https://palantir.github.io/tslint/)
  - [x] [xo linter](https://github.com/sindresorhus/xo)
  - [x] [Hunsky](https://github.com/typicode/husky) & [lint-staged](https://github.com/okonet/lint-staged) for autofix each commit
  - [x] Travis/AppVeyor config (unix-osx-windows CI)
  - [x] Code climate config
- [ ] SEO
  - [ ] [Helmet](https://github.com/nfl/react-helmet)
- [x] [Semantic-ui](http://react.semantic-ui.com) for styling
- [x] Lazyboy tools
  - [x] [plop](https://github.com/amwmedia/plop) templates -> `yarn generate`

## Files structure
```
 .
 ├── data                          // website data (included into graphQL)
 │   ├── author.json               // list of blog authors
 │   ├── avatars                   // authors avatars
 │   └── blog                      // all blog data (posts, images)
 ├── gatsby-config.js              // gatsby configuration
 ├── gatsby-node.js                // gatsby node hooks
 ├── generators                    // generators (`yarn generate`)
 │   ├── blog-post-generator.js    // `blog post` generator
 │   ├── component-generator.js    // `component` generator
 │   ├── page-generator.js         // `page` generator
 │   ├── plopfile.js               // generators entry
 │   ├── templates                 // all templates (handlebar notation)
 │   └── utils.js                  // utils scripts for generators
 ├── package.json
 ├── public                        // output folder (in .gitignore)
 ├── README.md                     // this file
 ├── src                           // sources
 │   ├── components                // all react components
 │   ├── css                       // styles
 │   ├── declarations.d.ts         // declarations for no typescript modules/files
 │   ├── graphql-types.d.ts        // graphql types (`yarn graphql-types`)
 │   ├── html.tsx                  // main html (required)
 │   ├── layouts                   // layouts
 │   │   └── default.tsx           // default layout (required)
 │   ├── pages                     // all pages
 │   └── templates                 // all templates (used for procedural page creation, see `gatsby-node.js`)
 ├── tools                         // miscs tools for dev
 │   └── update-post-date.js       // update post date hook
 ├── tsconfig.json                 // typescript configuration
 ├── tslint.json                   // tslint configuration
 └── yarn.lock                     // yarn lock file
 ```

## Plop generators - `yarn generate`

To avoid any boring copy/past, this starter-kit have many generators to permit 
simple bootstrap of current file pattern (eg. components/pages/blog posts).

You can add/delete/modify any generators into `/generators` folder.

Be lazy and have fun!
