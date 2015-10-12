---
layout: post
title:  "Starting a Blog With Jekyll"
date:   2015-10-12 01:44:07
categories: jekyll
---
Hi, I'm Alex, and welcome to my blog. I think it only seems natural to make the first post about the tool which was used in the creation of this blog so let's talk about Jekyll.

[Jekyll][jekyll] is a fascinatingly simple way to get a blog or static web site up and running in a matter of minutes, perhaps even seconds. It's installed as a Ruby gem from the command line:

{% highlight bash %}
~ gem install jekyll
~ jeykll new my-blog
~ cd my-blog
~ serve jekyll
{% endhighlight %}

That's all you have to do to get up and running. Navigate to port 4000 and you'll see what looks very much like a blog with a default post and template in place.

##Posts

Of course, you'll actually want to write your own content. Check out the file structure and you'll see a folder called `_posts`. You can get a feel for how writing a post works by looking at the default example. One of the first things you'll notice is that the filename starts with a date formatted like `2015-10-11`. This a Jekyll requirement that lets it know that this file is supposed to be a post.

The post's file extension can be a number of things from HTML to Markdown to Textile. Besides the date formatting in the filename, the only other requirement is that it begins with a YAML Front Matter block, which looks like this:

{% highlight html %}
---
layout: post
title: My Awesome Blog Post
---
{% endhighlight %}

You can add other variables inside the triple-dashes like categories and tags that would organize your blog posts. After that, it's simply just the content of your post, which is another aspect I like about Jekyll. There's no logging into a blogging platform. There's no database to worry about. There's just a simple text file on your laptop that makes writing effortless.

Another cool feature is the built-in code highlighter that I've used a couple times in this post. Simply use the highlight tag along with the name of the language you want to display, and the code inside your block will be rendered elegantly.

##Layout

We'll just touch on this briefly because it's pretty self-explanatory when you examine the file structure. A folder called `_includes` handles the header and footer while `_layouts` provides the basic structure for pages and posts. You can change these or leave them as is. There's also a SASS file in the `css` folder where you can make simple or complex changes.

Edit the `_config.yml` file in the root directory to change basic site variables like the blog's title and description.  


## Deployment

Now you have a working blog with content that you've written, but it's not going to do much good on your localhost port. You've got to share it with the world! 

Jekyll provides a number of options, and you can [read more about them here][jekyll-deployment]. The simplest method is to simply FTP the `_site` folder to where you want it on your web hosting provider. If you don't want to deal with hosting, [Github Pages][github-pages] is a simple and free solution. You can even set up a Git post-receive hook that will automate deployment of your changes every time you push.

##Final Thoughts
Yes, creating my own custom blog wouldn't have been difficult, but it's not something I would have wanted to spend even a few hours on. Using a platform like Blogger is obviously an option if time is a concern, but then the look of your site is heavily constrained. 

I think that Jekyll is the best of both worlds because it quickly gives you a nice, clean-looking blog out of the box that any developer can easily customize as little or as much as he or she wants.

[jekyll]: http://jekyllrb.com
[jekyll-deployment]: http://jekyllrb.com/docs/deployment-methods/
[github-pages]: http://pages.github.com/
