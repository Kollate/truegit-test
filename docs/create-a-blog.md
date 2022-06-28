---
featured: true
title: Create a blog
weight: 18
---

To create a blog on Truegit, you need to do follow these steps:

1. **Create a Github repository** with a `truegit.yaml` configuration file at the root folder ([Sample file](#minimal-truegityaml)). If you have an existing repository, simple add the `truegit.yaml` file. You may also **[fork this sample repository](https://bit.ly/3GwWozt)** to get started.
2. **Install the [Github App](https://bit.ly/3GyRCBG)** and give it access to the repository. You can do right after you install the app or configuring an existing installation to give it access to the repository. You can find your Truegit app inside Settings > Applications in your Github dashboard.
3. Go to your dashboard on Truegit (after creating your account on Truegit) and add the repository. Your blog should be live! To change your domain and manage your blog, you must **create an account** on [Truegit](https://truegit.io).

## Adding a new blog

Adding a new blog is simple. Make sure that you install the [Github App](https://bit.ly/3GyRCBG) and give it access to the repository where your blog lives (a repository with `truegit.yaml` file). Once you do that, you can add the repository to Treugit in the dashboard.

## Adding a new post

To create a new post, simply add a new markdown file to your repository. Read more [here](/docs/post)

## App Permissions

Our Github app requires permissions to read and write content of your repository, access Pull Requests (PR) and make new Pull Requests, and add comments to issues. We need to be able to write content to your repository so that you can edit your posts on Truegit and other viewers may suggest an edit to your posts. Each edit to your post creates a new PR, which you may choose to merge to the main branch.

## Updating Your blog

After your blog is created, all subsequent pushes to branches will generate Preview Deployments, and all changes made to the Production Branch (usually "main" or "master") will result in a Production Deployment. You may access these from your dashboard.

## Minimal truegit.yaml

Copy this file to a Github Repository to create a Truegit blog.

```yaml title="truegit.yaml"
title: My Blog
description: A blog about coding and the universe
```
