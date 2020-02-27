---
title: Building a Jekyll Blog with Hydeout Theme in 2020!
layout: post
tags: dde
category: eee
date: 2020-02-25T03:25:47.979Z
summary: eee
---
Obligatory build a blog site to write a blog post about how you built the blog site. 

With Gatsby gaining popularity, I decided to go against the grain and try out Jekyll, a popular static site generator written in Ruby. Jekyll is like the kid who used to be cool but was abandoned once the cool new kid, Gatsby, came to town. So I thought I'd give it a chance. I think it's important to understand a bit of old tech to fully understand why the bright and shiny new tech was built and what pain points it was meant to solve. 

Getting the site up and running was quite straightforward especially considering I had no previous experience with Jekyll whatsoever. 

First I perused the themes on [jamstackthemes.dev/ssg/jekyll/](https://jamstackthemes.dev/ssg/jekyll/) and chose [Hydeout](https://github.com/fongandrew/hydeout). 

Then I followed the steps in the [Jekyll Quick Start](https://jekyllrb.com/docs/) guide, which I am going to re-hash here for demonstration purposes. 

`gem install jekyll bundler` from the directory where I keep all my projects

`jekyll new plum-nugget`

`cd plum-nugget`

`bundle exec jekyll serve`

Then at <http://127.0.0.1:4000/>, you'll find the default jekyll themed blog ready to go. 

Then in the Gemfile, I replaced 

```shell
gem "jekyll", "~> 4.0.0"
gem "minima", "~> 2.5"
```

with

```shell
gem "jekyll", "~> 3.8.6"
gem "jekyll-theme-hydeout"
gem "jekyll-paginate"
```

I had to delete my Gemfile.lock and re-run bundle install to get things working.

In the _config.yml file, I replaced the existing theme and plugins settings with

```yaml
markdown: kramdown
theme: jekyll-theme-hydeout
plugins:
  - jekyll-feed
  - jekyll-paginate
paginate: 5
```

 And last by not least, I had to rename the `index.md` file to `index.html`, and replaced its contents to:

```
---
layout: index
title: Home
---
```

Refreshed the page on <http://127.0.0.1:4000/>, and hydeout theme is applied!

### Netlify Hosting and Netlify CMS Integration

From here I was able to get the site integrated with Netlify and Netlify CMS following their well-written instructions [here](https://www.netlifycms.org/docs/add-to-your-site/). I will mention that I had previous experience with Netlify CMS so this part was easy for me but their documentation is honestly so good that I don't think I need to go over it. Before I knew it, I was able to easily start adding content to my site!!

### Making Customizations to the Theme

Making customizations to the theme is easy by copying a file from the `_includes` or `_layouts` folders in the theme directory, pasting it into my own `_includes` or `_layouts` folder and making changes to the html files themselves. Your changes overwrite the theme's files so you can make whatever updates you please.

### Lighthouse Audit Benchmark

| Performance | Accessibility | Best Practices | SEO |
|-------------|---------------|----------------|-----|
| 100         | 55            | 93             | 88  |

## Takeaways

I was able to get the site up and running in an evening, having to play around with some configuration parameters to get it to work. The documentation was not crystal clear so I had to trial-and-error before I got everything working. The Lighthouse Audit results are pretty interesting. Clearly performance with Jekyll is not something to be concerned about. However, it seems Accessibility and SEO need some improvements. I'm not sure if these results are due to the theme or jekyll itself. 

I plan to do this same exercise with a brand new Gatsby blog soon - it will be interesting to see what the Lighthouse Audit results are for a brand new Gatsby site.  
