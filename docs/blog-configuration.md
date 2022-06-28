---
title: Blog Configuration
weight: 20
---

# Blog Configuration

You can configure everything about your blog (except the domain) with `truegit.yaml` file at the root of your repository. It is the existence of this file that makes your blog go live.

```yaml title="truegit.yaml"
title: My Blog
description: A blog about coding and the universe
logoImage: ./logo.jpg
# Must be a HEX value. Color Red for instance?
theme: "#FF0000"
bannerImage: ./banner.jpg
backgroundColor: "#FAF5EF"
socials:
  facebook: https://www.facebook.com/my-profile
  twitter: https://www.twitter.com/my-profile
  instagram: https://www.instagram.com/my-profile
  url: https://mywebsite.com
  youtube: https://www.youtube.com/c/my-channel
  linkedin: https://www.linkedin.com/in/my-profile
  email: hello@truegit.io
  github: https://github.com/my-profile
  reddit: https://www.reddit.com/user/my-profile
navLinks:
  - title: Hire me
    url: https://mywebsite.com
    isExternal: true
  - title: Must Read
    url: /must-read
blogFolder: blog
authors:
  author-1:
    name: Author 1
    title: Short title
    description: Long description
  author-2:
    name: Author 2
    title: Short title
    description: Long descripiton
```

## Title

The title of your blog. By default, this is empty.

```yaml
title: My Blog
```

## Description

The description of your blog. By default, this is empty.

```yaml
description: My Blog
```

## Logo

The logo of your blog. By default, this is empty. This logo is also used as the favicon for your blog.

```yaml
logoImage: ./logo.png
```

## Banner

The banner of your blog. By default, this is empty.

```yaml
bannerImage: ./banner.png
```

## Body Background

The background color of your blog. By default, this is white. Note that it must be a HEX value in quotes (to avoid YAML comment).

```yaml
backgroundColor: "#FAF5EF"
```

## Theme

The theme color of your blog. It must be **HEX** value and it might be in **quotes** like this `"#000000"` (otherwise yaml ignores it as a comment).

```yaml
theme: "#000000"
```

## Socials

You can configure the social links on the footer of your blog. We support the links for selected social platforms.

```yaml
socials:
  facebook: https://www.facebook.com/my-profile
  twitter: https://www.twitter.com/my-profile
  instagram: https://www.instagram.com/my-profile
  url: https://mywebsite.com
  youtube: https://www.youtube.com/c/my-channel
  linkedin: https://www.linkedin.com/in/my-profile
  email: hello@truegit.io
  github: https://github.com/my-profile
  reddit: https://www.reddit.com/user/my-profile
```

## Navigation Links

We always have a link for your About page (`about.md` file at the root blog folder), Tags page, and Authors page at the top of your blog navigation.

You can add extra links. Note that the `isExternal` flag opens the link on a separate tab. Note that you may also use relative urls.

```yaml
navLinks:
  - title: Hire me
    url: https://mywebsite.com
    isExternal: true
  - title: Must Read
    url: /must-read
```

## Blog Folder

By default, we scan for posts and collection everywhere in your repository. If you want to limit the files to be scanned to a specific directory, you can use `blogFolder` option.

```yaml
blogFolder: ./blog
```

## Authors

You can add authors for your blog using the `authors` field. This is an object with keys as the author IDs and values as the metadata for the authors. You can reference the authors in your posts by [using their IDs](/docs/post#authors).

```yaml
authors:
  author-1:
    name: Author 1
    title: Short title
    description: Long description
  author-2:
    name: Author 2
    title: Short title
    description: Long descripiton
```
