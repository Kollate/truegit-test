---
title: Collections
---

Collections are a way to categorize your blog posts. Each collection has a separate page on your blog with its own title and description. Each post of your blog can belong to a single collection only.

Collections are synonymous with directories in the blog folder of your repository. Note that the blog folder is the root folder of your repository by default. However you can change it to a specific directory using `truegit.yaml` file. [See Here](/docs/blog-configuration#blog-folder)

## Create a collection

To create collections, simply create a directories in your blog folder. Every post inside a collection directory belongs to that collection. Note that we only consider the single level deep folders to be collections.

You can configure each individual collection using `metadata.yaml` file at the root of the collection directory.

## Title

The title of your collection. This is by default the name of the directory of that collection.

```yaml title="my-collection/metadata.yaml"
title: My Collection
```

## Description

The description of your collection. This is by default empty.

```yaml title="my-collection/metadata.yaml"
description: This is the description that shows on the collection page.
```

## Skipping Navbar

Each collection of your blog gets a link on the secondary navigation bar of your blog. If you want to skip a collection from showing on the navigation bar, you can use `skipNavbar` flag

```yaml title="my-collection/metadata.yaml"
skipNavbar: true
```
