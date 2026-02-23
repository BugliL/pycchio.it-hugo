---
date: "2026-02-22T13:17:32+01:00"
draft: true
title: "Automating Blog Deploy"
description: |-
    I am a lazy software engineer, and I don't like to do repetitive tasks. If I
    do something more than twice, my brain scratches and starts looking for a
    way to automate it. Compiling and deploying my blog is one of those tasks. I
    want to automate it, this is how I did it.
---

The best way I found to automate the deployment of my blog is to use 
`GitHub Actions` and `GitHub Pages`. I think there are many ways to do it, maybe
easier, but this  was the straightforward way I found to do it with the tools I
already use.

## What are GitHub Actions?
From official documentation: [GitHub Actions](https://docs.github.com/en/actions/get-started/understand-github-actionsO

> GitHub Actions is a continuous integration and continuous delivery (CI/CD)
> platform that allows you to automate your build, test, and deployment pipeline.
> You can create workflows that build and test every pull request to your
> repository, or deploy merged pull requests to production.


Pratically, when something happens in your repository, like a push, a pull
request, or a release, you can trigger a workflow that will do something.

## Whate are GitHub Pages?
From official documentation: [GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages)

> GitHub Pages is a static site hosting service that takes HTML, CSS, and
> JavaScript files straight from a repository on GitHub, optionally runs the files
> through a build process, and publishes a website.

The pages are hosted on `github.io` and you can use a custom domain if you want, more information can be found [here](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).


## How to automate the deployment of my blog?

I have found a good explanation (here)[https://gohugo.io/host-and-deploy/host-on-github-pages/] on how to deploy a Hugo blog on GitHub Pages.

The first thing I did was to create a workflow file in my repository. The file is called `.github/workflows/deploy.yml` and it contains the following code:

```yaml
name: Deploy Blog
on:
    push:
        branches:
        - main

jobs:
    build:
        runs-on: ubuntu-latest
        steps:
        - name: Checkout code
            uses: actions/checkout@v2

        - name: Set up Node.js
            uses: actions/setup-node@v2
            with:
            node-version: '14'

        - name: Install dependencies
            run: npm install

        - name: Build blog
            run: npm run build

        - name: Deploy to GitHub Pages
            uses: peaceiris/actions-gh-pages@v3
            with:
            github_token: ${{ secrets.GITHUB_TOKEN }}
            publish_dir: ./public
```