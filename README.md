# POSSE-Enabled Jekyll Site

A Jekyll site template with [POSSE](https://indieweb.org/POSSE) (Publish on your Own Site, Syndicate Elsewhere) features built-in.

## Features

- **RSS Feed** (`feed.xml`) - Full-content feed for subscribers and syndication tools
- **OpenGraph & Twitter Cards** - Rich previews when shared on social media
- **Syndication Links** - `rel="syndication"` markup linking to copies on other platforms
- **IndieWeb Microformats** - h-card, h-entry, and other microformats for IndieWeb compatibility
- **Webmention Support** - Endpoints configured for receiving interactions

## Setup

1. Install dependencies:
   ```bash
   bundle install
   ```

2. Edit `_config.yml` with your details:
   - Site title and description
   - Author information
   - Social media handles
   - Syndication targets

3. Run locally:
   ```bash
   bundle exec jekyll serve
   ```

## Writing POSSE Posts

Add syndication links to your front matter after publishing to other platforms:

```yaml
---
layout: post
title: "My Post Title"
syndication:
  - name: Bluesky
    url: https://bsky.app/profile/you/post/xxxxx
  - name: Twitter
    url: https://twitter.com/you/status/xxxxx
---
```

## Syndication Workflow

1. Write and publish your post here first
2. Share/copy to your social platforms (manually or via tools like Bridgy)
3. Update the post's `syndication` front matter with the URLs
4. The syndication links will appear at the bottom of your post

## Tools for Automation

- [Bridgy](https://brid.gy/) - POSSE-as-a-service
- [Micro.blog](https://micro.blog/) - Syndication hub
- [IFTTT](https://ifttt.com/) - RSS-based automation
