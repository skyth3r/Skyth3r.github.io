---
title: Mastodon Author Tags
date: 2024-10-12T09:20:00
description: Adding Mastodon author tags to my Hugo website
tags: ['mastodon']
---

[Mastodon 4.3](https://blog.joinmastodon.org/2024/10/mastodon-4.3/) was just released a few days ago and it comes with an interesting new feature, 'Author Tags' (the term was coined by [Robb Knight](https://rknight.me/blog/setting-up-mastodon-author-tags/) a few days ago).

Author Tags essentially allow you to add some metadata to pages on your website that links the content to your Mastodon profile, and when a post from your site is shared on Mastodon, the preview card should include a button titled 'More from USER' which links to the author's Mastodon profile.

This is handy for instances where someone else might share one of your posts, giving readers not only a chance to read the article but also view/follow the author of said post. I think it's a great new addition that is going to have an impact on all authors on the fediverse.

I ended up adding this to my Hugo theme by adding a new snippet of code (see below) to my head partial and updating my `config.toml` to include a Mastodon author parameter.
```
<!-- Mastodon Author Tag -->
{{ if .Site.Params.Mastodon }}
<meta name="fediverse:creator" content="{{ .Site.Params.mastodon.author }}" />
{{ end }}
```