---
layout: page
title: Docusaurus
permalink: /docusaurus/
resource: true
---

https://docusaurus.io/


# Preview changes locally

To preview your changes as you edit the files, you can run a local development server that will serve your website and reflect the latest changes.

```
$ npm run start

> rabbit-hole@0.0.0 start
> docusaurus start

[INFO] Starting the development server...
[SUCCESS] Docusaurus website is running at: http://localhost:3000/kb/
Browserslist: browsers data (caniuse-lite) is 9 months old. Please run:
  npx update-browserslist-db@latest
  Why you should do it regularly: https://github.com/browserslist/update-db#readme

✖ Client
  Compiled with some errors in 5.29s
```

# Installation

Article: https://docusaurus.io/docs/installation

```
$ npx create-docusaurus@latest rabbit-hole classic
```

Docusaurus version, as set in `package.json`:

```
$ npx docusaurus --version
3.7.0
```

Don't forget to install Yarn and auto-gen a `yarn.lock` file:

```
$ yarn install
```


# Build and Deploy

Article: https://docusaurus.io/docs/deployment

Use Yarn (not npm) because it scales better and LinkedIn's Docusaurus implementation uses it.

Local build:

```
$ yarn build
```

Local deploy (for previewing on my mac before pushing to production):

```
$ yarn run start
```

# Deploy to GitHub Pages with GitHub Actions

Article: https://docusaurus.io/docs/deployment#deploying-to-github-pages

