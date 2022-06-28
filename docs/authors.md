---
weight: 6
---

# Authors

You can add authors for your blog using the `authors` field in the `truegit.yaml` configuration file. This is an object with keys as the author IDs and values as the metadata for the authors. You can reference the authors in your posts by [using their IDs](/docs/post#authors). We create a page on your blog for each author with their list of posts.

```yaml
authors:
  author-1:
    name: Author 1
    title: Short title
    description: Long description
    url: https://google.com
    profileImage: ./assets/author-1.png
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
  author-2:
    name: Author 2
    title: Short title
    description: Long descripiton
```
