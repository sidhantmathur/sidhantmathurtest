---
layout: post
title:  "Static Site Generators"
date:   2018-03-06 20:00:00 -0600
categories: web dev
comments: true
---

***Static Website Generators*** are an increasingly popular tool for web development. Many developers including myself find static site generators to be incredibly convenient and powerful tools; this very blog was made with a static site generator. Why exactly is this a trend? Let's get into it. 

## Dynamic vs. Static Websites

Most websites with interactive or user added content (like comments or posts) have a server (with an appropriate OS), database, backend routing, plugins and more. Furthermore when there is a CMS (Content Management System: Wordpress, Drupal) involved (as it typically is for clients) then there's CMS specific themes, plugins, and the CMS application itself. Now *that* is a ton of stuff. 

Statically generated websites have none of that; they're just HTML, CSS, and JavaScript files generated and hosted on a server. This confers significant advantages, while not having as much of a disadvantage in features as you may think. 

## Ease of Development

Static site generators are very easy to create and deploy. All I did to create this blog was fork a repository called [Jekyll Now](https://github.com/barryclark/jekyll-now) and edit the configuration file. Github automatically generates and deploys your Jekyll website. From that point, all you have to do is add blog posts in markdown. Obviously, if you want a custom theme, it will take some work, but getting the website itself up and running is no issue at all. 

This is perfect if you, like me, don't want to spend too much time on the design and coding of a blog or website; rather focusing on the content while working on other projects. 

## Lightweight

Statically generated websites are much faster than dynamic websites. Heavy duty backends that are present on most websites really slow everything down and add a lot of bloat to the server. Static websites eliminate almost all of that. 

This way you can have a website that: 

1. Loads faster
2. Takes less server space

Which in turn allows you to: 

1. Keep users engaged
2. Save money on servers
3. Be better prepared for traffic spikes

Speed is a critical measure for websites; [53% of mobile users abandon a website that takes longer than 3 seconds to load.](https://www.doubleclickbygoogle.com/articles/mobile-speed-matters/) Too many businesses, big and small, have bloated web pages that take far too long to load causing users to become bored and frustrated. If you want users to pay attention, you can't be wasting their time loading. 

[You can use this calculator to see what effect your slower page speeds are having.](https://www.doubleclickbygoogle.com/articles/mobile-speed-adds-up/) 

![Server Strain](https://images.pexels.com/photos/17840/pexels-photo.jpg?w=1260&h=750&dpr=2&auto=compress&cs=tinysrgb)

### Why are Static Websites Faster? 

Static websites improve speed and alleviate servers because they are so incredibly small causing the strain per "serve" to a user to be reduced. Also, static websites have fewer files, in general, causing it to have a faster load as well: 5000 files together taking up 1 GB of space take more time to download than one large file that takes up 1 GB of space. The reason for this is because the server and your computer have to make a sort of "handshake" for every individual file slowing down the entire process. Backend frameworks tend to have a ***lot*** of files, especially in heavyweight or slower frameworks like Ruby on Rails. 

A **simplified** way to think about this: the reduced space in conjunction with fewer files allows the server to spend a ton fewer resources: less CPU strain because of less file processing, and less RAM usage because the file size for the concurrently running websites is smaller. For example, using a static website generator means that 1 GB of RAM can run maybe 500 of your websites vs 50 with a typical dynamic site and the CPU isn't straining to make a billion handshakes because all it has to do is load 5-10 files instead of 50-100. So you can have 10 times the users with the same server space, and those users will receive their content much faster because the CPU on the server isn't strained at all. 

## Security

CMSs are both finicky and vulnerable. Avoiding them will prevent common exploits from affecting your website. It's been estimated that [almost 70% of Wordpress websites are vulnerable to very common exploits and hacks](https://www.wpwhitesecurity.com/wordpress-security-news-updates/statistics-70-percent-wordpress-installations-vulnerable/). This isn't a thing that is easily mitigated either: [even the most powerful people in the world are vulnerable to this.](https://www.theregister.co.uk/2016/04/07/panama_papers_unpatched_wordpress_drupal/) This is the nature of having a visible backend or CMS; people can easily identify and exploit it.  With a static website, you get around this because you often don't even ***have*** a backend to exploit. Even if you do have a very simple backend, hackers won't be able to know which backend framework or language you're using which makes the entire process much more difficult for them. 

![Moving Parts](https://images.pexels.com/photos/414579/pexels-photo-414579.jpeg?w=1260&h=750&dpr=2&auto=compress&cs=tinysrgb)

## Reliability

One of the most fundamental ideas when it comes to engineering a physical product is that less moving parts result in greater reliability. This is also true for websites. Even if your website works perfectly now, over time something will go wrong. This happens whenever there is a server and complex backend involved. There is sort of this code "rot" that happens for a myriad of unidentifiable reasons and your perfectly running website will go down if not maintained. Having a statically generated website means that there are almost no "moving parts", and the website can stay online for years without much maintenance. 

## Features Parity

One of the biggest disadvantages of static websites is their lack of features and interactivity. Dynamic websites have no problem making users interact and post things on the website. This isn't as big of a problem as you may think though. 

All the major static site generators are slowly adding many of the most common features of fully fledged websites. There is a [plugin that allows for comments to be posted](https://staticman.net/), (or you could use a [service like Disqus](https://disqus.com/)). When it comes to forms, [Netlify has a form handler](https://www.netlify.com/docs/form-handling/). Can't search on a static website? Oh wait [you can](https://www.algolia.com/) Do you want your clients to have a nice CMS interface? There are ways of hooking up the generator with a CMS and generating a new post upon clicking submit in the CMS. You can even [email in posts](https://github.com/masukomi/JekyllMail). As you can see, if you want a feature in a static website, there is probably already someone working on it and it will just get better and better over time. 

## Version Control: GitHub

I use Jekyll to run this blog, and I chose it specifically for its integration with Github pages. Absolutely free server and domain? Automatic generation upon push? Github as version control? Sign me up. 

The advantage of version control is that you can take a look at the edits you've made to your blog, from the grammar edits to the spellings, and even better, if someone else finds an issue, they can make a request to fix it in GitHub. It's like your readers are working together with you on an open source project to make the best blog possible. 

More than that, there are backups to all changes, so you can easily revert to an earlier stage if something goes wrong. Constantly backing up databases is a much clumsier alternative. 

## Conclusion

It's clear from what I've written, I like static site generators. In descending order, I like: 

1. Cheap and Lightweight on Servers
2. Secure
3. Fast
4. Convenient to Use
5. Version Control
6. Near Feature Parity

I think that most businesses can move towards a static website with no real ill effects. Most major features can be outsourced to another website or plugin that handles it. Statically generated websites are good enough for heavy duty things like [the Obama campaign](http://kylerush.net/blog/meet-the-obama-campaigns-250-million-fundraising-platform/), [Github Services](https://services.github.com/), [the Ruby on Rails blog](http://weblog.rubyonrails.org/), [the new Healthcare.gov](https://developmentseed.org/blog/new-healthcare-gov-is-open-and-cms-free/), ([and more!](http://planetjekyll.github.io/showcase/)) and they're convenient enough for small blogs like this one to use. 

Static website generators are the future, and we should be happy about it; who doesn't want a faster and lighter-weight web experience?  