---
title: Assets
---

We store all the images in your blog folder in a S3 bucket and power their delivery through Cloudfront. We only store images with extensions ".jpg", ".png", ".jpeg", and ".webp". We also limit uploading images with size less than 20Mb.

To reference a image in your blog configuration file or posts, you can use either relative link or an absolute link. Absolute links are relative to the [blogFolder](/docs/blog-configuration#blog-folder) of your repository. For relative links in your posts, we use the post directory as the base directory relative to which we get the image location. For relative links in your blog configuration, we use the `blogFolder` as the base folder.
