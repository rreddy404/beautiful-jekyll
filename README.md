
## Features

### Mobile-first
**Beautiful Jekyll** is designed to look great on both large-screen and small-screen (mobile) devices. Load up your site on your phone or your gigantic iMac, and the site will work well on both, though it will look slightly different.

### Customizable

Many personalization settings in `_config.yml`, such as setting your name and site's description, changing the background colour/image, setting your avatar to add a little image in the navigation bar, customizing the links in the menus, customizing what social media links to show in the footer, etc.

### Allowing users to leave comments

If you want to enable comments on your site, Beautiful Jekyll supports the [Disqus](https://disqus.com/) comments plugin.  To use it, simply sign up to Disqus and add your Disqus shortname to the `disqus` parameter in the `_config.yml`.

If the `disqus` parameter is set in the configuration file, then all blog posts will have comments turned on by default. To turn off comments on a particular blog post, add `comments: false` to the YAML front matter. If you want to add comments on the bottom of a non-blog page, add `comments: true` to the YAML front matter.

### Adding Google Analytics to track page views

Beautiful Jekyll lets you easily add Google Analytics to all your pages. This will let you track all sorts of information about visits to your website, such as how many times each page is viewed and where (geographically) your users come from.  To add Google Analytics, simply sign up to [Google Analytics](http://www.google.com/analytics/) to obtain your Google Tracking ID, and add this tracking ID to the `google_analytics` parameter in `_config.yml`.

### Sharing blog posts on social media

By default, all blog posts will have buttons at the bottom of the post to allow people to share the current page on Twitter/Facebook/LinkedIn.  You can choose to enable/disable specific social media websites in the `_config.yml` file. You can also turn off the social media buttons on specific blog posts using `social-share: false` in the YAML front matter.

### RSS feed

Beautiful Jekyll automatically generates a simple RSS feed of your blog posts, to allow others to subscribe to your posts.  If you want to add a link to your RSS feed in the footer of every page, find the `rss: false` line in `_config.yml` and change it to `rss: true`.

### Page types

- **post** - To write a blog post, add a markdown or HTML file in the `_posts` folder. As long as you give it YAML front matter (the two lines of three dashes), it will automatically be rendered like a blog post. Look at the existing blog post files to see examples of how to use YAML parameters in blog posts.
- **page** - Any page outside the `_posts` folder that uses YAML front matter will have a very similar style to blog posts.
- **minimal** - If you want to create a page with minimal styling (ie. without the bulky navigation bar and footer), assign `layout: minimal` to the YAML front matter.
- If you want to completely bypass the template engine and just write your own HTML page, simply omit the YAML front matter. Only do this if you know how to write HTML!

### YAML front matter parameters

These are the main parameters you can place inside a page's YAML front matter that **Beautiful Jekyll** supports.

Parameter   | Description
----------- | -----------
title       | Page or blog post title
subtitle    | Short description of page or blog post that goes under the title
tags        | List of tags to categorize the post. Separate the tags with commas and place them inside square brackets. Example: `[personal, self help, finance]`
bigimg      | Include a large full-width image at the top of the page.  You can either give the path to a single image, or provide a list of images to cycle through (see [my personal website](http://deanattali.com/) as an example).
comments    | If you want do add Disqus comments to a specific page, use `comments: true`. Comments are automatically enabled on blog posts; to turn comments off for a specific post, use `comments: false`. Comments only work if you set your Disqus id in the `_config.yml` file.
show-avatar | If you have an avatar configured in the `_config.yml` but you want to turn it off on a specific page, use `show-avatar: false`. If you want to turn it off by default, locate the line `show-avatar: true` in the file `_config.yml` and change the `true` to `false`; then you can selectively turn it on in specific pages using `show-avatar: true`.
image       | If you want to add a personalized image to your blog post that will show up next to the post's excerpt and on the post itself, use `image: /path/to/img`.
share-img   | If you want to specify an image to use when sharing the page on Facebook or Twitter, then provide the image's full URL here.
social-share | If you don't want to show buttons to share a blog post on social media, use `social-share: false` (this feature is turned on by default).
use-site-title | If you want to use the site title rather than page title as HTML document title (ie. browser tab title), use `use-site-title: true`. When set, the document title will take the format `Site Title - Site Description` (eg. `My website - A virtual proof that name is awesome!`). By default, it will use `Page Title` if it exists, or `Site Title` otherwise.
layout      | What type of page this is (default is `blog` for blog posts and `page` for other pages. You can use `minimal` if you don't want a header and footer)
js          | List of local JavaScript files to include in the page (eg. `/js/mypage.js`)
ext-js      | List of external JavaScript files to include in the page (eg. `//cdnjs.cloudflare.com/ajax/libs/underscore.js/1.8.2/underscore-min.js`). External JavaScript files that support [Subresource Integrity (SRI)](https://developer.mozilla.org/en-US/docs/Web/Security/Subresource_Integrity) can be specified using the `href` and `sri` parameters eg.<br/>`href: "//code.jquery.com/jquery-3.1.1.min.js"`<br/>`sri: "sha256-hVVnYaiADRTO2PzUGmuLJr8BLUSjGIZsDYGmIJLv2b8="`
css         | List of local CSS files to include in the page
ext-css      | List of external CSS files to include in the page. External CSS files using SRI (see `ext-js` parameter) are also supported.
googlefonts | List of Google fonts to include in the page (eg. `["Monoton", "Lobster"]`)
gh-repo   | If you want to show GitHub buttons at the top of a post, this sets the GitHub repo name (eg. `daattali/beautiful-jekyll`). You must also use the `gh-badge` parameter to specify what buttons to show.
gh-badge  | Select which GitHub buttons to display, available options are: [star, watch, fork, follow]. You must also use the `gh-repo` parameter to specify the GitHub repo.

### Advanced features (including how to use a custom URL address for your site)

I wrote [a blog post](http://deanattali.com/2015/03/12/beautiful-jekyll-how-to-build-a-site-in-minutes/) describing some more advanced features that I used in my website that are applicable to any Jekyll site.  It describes how I used a custom URL for my site (deanattali.com instead of daattali.github.io), how to add a Google-powered search into your site, and provides a few more details about having an RSS feed.

## Creating a User Page vs a Project Page

If you're not sure what the difference is, you can probably safely ignore this section.

If you want to use this theme to host a website that will be available at `https://YOURUSERNAME.github.io`, then you do not need to read this section. That is called a User Page, you can only have one User Page in your GitHub account, and it is what you get by default when forking this project.

If you want to use this theme to create a website for a particular repository, it will be available at `https://YOURUSERNAME.github.io/REPONAME`, and that is called a [Project Page](https://help.github.com/articles/user-organization-and-project-pages/). You can have a Project Page for each repository you have on GitHub. There are two important things to note when creating a project page:

1. In the configuration file (`_config.yml`), you should set `baseurl` to be `/projectname` instead of `""`.
2. Project Pages are served from a branch named `gh-pages`, and you should be generating all the website content on that branch. When you fork Beautiful Jekyll, you'll already have a `gh-pages` branch but you should delete it and generate it again from the `master` branch. The reason is that the `gh-pages` branch in its current form does not have the updated code of Beautiful Jekyll, so you need to create that branch from the `master` branch (which is where all my new features and work go into).

## Showcased users (success stories!)

To my huge surprise, Beautiful Jekyll has been used in over 500 websites in its first 6 months alone! Here is a hand-picked selection of some websites that use Beautiful Jekyll.

Want your website featured here? [Contact me](http://deanattali.com/aboutme#contact) to let me know about your website.


## Advanced: Local development using Docker

Beautiful Jekyll is meant to be so simple to use that you can do it all within the browser. However, if you'd like to develop locally on your own machine, that's possible too if you're comfortable with command line. Follow these simple steps set that up with Docker:

1. Make sure you have [Docker](https://www.docker.com/) installed.

2. Clone your repository locally.

    ```bash
    git clone https://github.com/<your_username>/<your_username>.github.io.git
    ```

3. Run the following shell commands to build the docker image and start the container for the first time:

    ```bash
    cd <repository_folder>
    docker build -t beautiful-jekyll $PWD
    docker run -d -p 4000:4000 --name beautiful-jekyll -v $PWD:/srv/jekyll beautiful-jekyll
    ```


Now that Docker is set up, you do not need to run the above steps again. You can now view your website at http://localhost:4000/. You can start the container again in the future with:

```bash
docker start beautiful-jekyll
```

And you can stop the server with:

```bash
docker stop beautiful-jekyll
```

Whenever you make any changes to `_config.yml`, you must stop and re-start the server for the new config settings to take effect.

Disclaimer: I personally am NOT using local development so I don't know much about running Jekyll locally. If you follow this route, please don't ask me questions because unfortunately I honestly won't be able to help!

## FAQ

Beautiful Jekyll is actively used by thousands of people with wildly varying degrees of competency, so it's impossible to answer all the questions that may arise. Below are answers to a few very common questions. Most questions that I get asked are not directly related to this theme, and instead are more general questions about Jekyll or web development. Many such questions can be answered by reading the [Jekyll documentation](http://jekyllrb.com/) or simply by Googling.

#### How do I change the number of posts per page OR the colour of the navigation bar OR the image in the navigation bar OR ...?

Beautiful Jekyll is built to be very customizable, and as such, many questions about "how do I change ..." can be answered by looking at the `_config.yml` file. The configuration file has many adjustable parameters to customize your site.

#### How do I add a favicon to my site?

Easy! Just place a valid `favicon.ico` (or another valid favicon image) in the root directory of your project. And then wait! It can take a while to update.

#### How do I move the blog to another page instead of having it on the home page?

The default style of Beautiful Jekyll is to feature the blog feed on the front page. But for many sites that's not the ideal structure, and you may want to have a separate dedicated page for the blog posts. To have the blog hosted on a different URL (for example at `<mysite.com>/blog`), copy the `index.html` file into a folder with the same name as the desired page (for example, to `blog/index.html`), and in the `_config.yml` file you need to add a parameter `paginate_path: "/<page name>/page:num/"` (for example `paginate_path: "/blog/page:num/"`).

#### What size do you recommend using for the `bigimg` photos?

Unfortunately, this is a no-answer! There isn't a one-size-fits-all solution to this, because every person will view your site on a different browser with different dimensions. Some browsers will have very wide aspect ratio, some will be narrower, some will be vertical (such as phones), different phones have different screens, etc. The image will always be centered, so the only tip I can give is that you should make sure the important part of the image is in the middle so that it'll always show. Other than that, every browser will show a different clipping of the image.

