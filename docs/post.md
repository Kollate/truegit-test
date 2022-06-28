---
title: Post
weight: 16
---

You can create a post by adding a new markdown file with `.md` extension to your repository. If you are using a specific folder (`blogFolder` specified in `truegit.yaml` file) for all your posts, the file must be inside that folder. We support [Github Flavored markdown](https://github.github.com/gfm/).

Each post can be configured by adding the front matter to your file. The front matter should be at the top of your file
and is enclosed by `---`.

```md title="post.md"
---
title: This is my post title
subTitle: This is a description of this post.
date: 1989/07/11
bannerImage: ./banner.png
slug: this-is-my-slug
tags: [kubernetes, graphql]
authors:
  - author-1
  - author-2
featured: true
---

Hey this is my first post. _How do you like it?_
```

Below are the fields that can be configured for your posts.

## Title

The title of your post.

Default: First H1 tag of your post

```yaml
title: My post's title
```

## Subtitle

The subtitle of your post.

Default: Empty

```yaml
subTitle: My post's sub title
```

## Publish Date

The date the post is published on.

Default: The file commit date.

Supports [Date.parse](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/parse) method

Examples: "YYYY-MM-DD", "Month Date, Year"

```yaml
date: 1989/07/11
```

## Banner Image

The banner image of your post. It must be a [path](/docs/assets) to an image file in your repository.

Supports `png`, `jpeg`, `jpg`, and `webp` formats.

```yaml
bannerImage: ./banner.png
```

## Slug

The absolute path for your post shown on the URL.

Default: The path to your post relative to the root folder.

Example: If you have a post located at /blog/collection/my-post.md, it will have the default slug `/collection/my-post`.
If you want the slug to be `/this-is-my-slug`, you can use

```yaml
slug: this-is-my-slug
```

## Tags

Tags are a way to organize your posts by hashtags. It allows your viewer to see all the posts with a specific tag.

```yaml
tags: [kubernetes, graphql]
```

## Authors

The IDs of authors of this post. To reference an author, you must [add the author](/docs/authors) in your blog configuration file.

Default: No authors

Example

```yaml
authors:
  - author-1
  - author-2
```

You must add the authors in `truegit.yaml` before referencing them

```yaml
authors:
  author-1:
    name: Author 1
    title: Short title
    description: Long descripiton
  author-2:
    name: Author 2
    title: Short title
    description: Long descripiton
```

## Edit Suggestion

By default, the viewers may suggest an edit to your posts on Truegit or on public Github repository. Every suggestion made on Truegit creates a Pull Request in your repository. To disable this for an individual post, you can use

```yaml
disableSuggestEdit: true
```

## Draft

By default, every post create in your repository is published to your blog. If you want to keep a post in the draft state, you may use the `draft` flag.

Note that a draft can only be viewed by you.

```yaml
draft: true
```

## Skip Listing

Sometimes you may not want a post to be listed but is can be viewed. For instance, you may not want to list the `about.md` page. Setting `skipListing` flat to true removes the post from any of the lists.

```yaml
skipListing: true
```

## Featured Post

To feature a post on the landing page of your blog, you can use the `featured` flag. Note that we currently feature only one post per blog.

Default: No posts are featured. They are sorted in descending order of the [publish date](#publish-date).

```yaml
featured: true
```

---
