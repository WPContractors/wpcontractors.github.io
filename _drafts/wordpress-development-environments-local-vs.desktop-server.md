---
date: 2021-01-21 17:12:12 +0000
author: evan-farmer
categories: []
title: 'WordPress Development Environments: Local vs. Desktop Server '
description: There are many options available for local website development. Desktop
  Server and Local are two of the best tools made specifically for WordPress and you
  should try them both today.
image: "/uploads/caspar-camille-rubin-0qvbnep1y04-unsplash-copy.jpg"
thumbnail: "/uploads/caspar-camille-rubin-0qvbnep1y04-unsplash.jpg"
color_overlay: ''

---
In the world of web development, there are various tools that one can use for setting up a local virtual server. Some are more of an integrated development environment (IDE) for testing and building websites or other software projects, others are more specific to the task of creating a website locally.

There are classic local server tools like [XAMMP](https://www.apachefriends.org/download.html) and [MAMP](https://www.mamp.info/en/) and some tools are more command-line-oriented, while others are web-based. However, they each provide a unique feature set that is often geared toward UX, in regard to both the skill level and common workflow patterns of their users. 

### **Benefits of Local WP Development**

Most consider it best practice to have a local copy of any production website available for testing and making changes. This helps reduce the risk of breaking the live site, while giving the developer a sandbox environment to test changes.

It’s wise to make this practice a part of your approach, and iis an essential part of forming a productive and safe workflow as a developer. Fortunately, there are some great tools out there to help get a local development set up running in no time!

Now, if you're using [WP-CLI](https://wpcontractors.com/blog/2020/12/10/level-up-your-wordpress-game-with-wp-cli/) in your daily workflow, you may not necessarily be a huge fan of these GUI oriented solutions for local development. With Local, in particular, you have to use their application to open the SSH container separately for each site, instead of directly executing commands in the working directory. However, the premium version of Desktop Server has a DS-CLI tool, giving you command line access to your projects, and WP-CLI is fully integrated.

### **WP Local Dev Solutions**

Now, let’s consider the two local dev tools mentioned already, Local and Desktop Server, which are specific to WordPress. Both of these pieces of software must be downloaded and installed on your machine and they each have a free and Pro version available.

There are good reasons to consider them both, so let’s take a look at some of the pros and cons. We'll explore the methods of deployment available, hosting options for production, and the unique features provided with both platforms.

### **Desktop Server**

The team at ServerPress launched Desktop Server about a decade ago so their product definitely has some longevity to it. The company brand and the software they maintain is reminiscent of Microsoft, but rest assured, they do offer support for both the latest Mac OS and Windows platforms. During installation, Desktop Server runs a wizard with simple instructions and some basic options for getting your virtual server up and running.

Once it’s set up, creating a local dev site is fairly straightforward, and utilizes a similar wizard for the process. Just follow the prompts and provide the necessary information, such as your system password, when confirming administrative access for creating the virtual servers. More on the setup process can be found [here](https://docs.serverpress.com/article/150-getting-started-with-desktopserver).

### **Desktop Server Limited & Premium**

When starting off with the free version of Desktop Server, you're limited to just three sites at any one time. This means that once you've created those three sites, before you spin up another installation of WordPress and start developing a new site, you'll have to delete one of the others first.

However, you can still create as many sites as you want using Desktop Server Limited, but you can only manage three at a time. And once you've used the application enough to reach that limit, you should have a good idea of whether or not it's worth it to [pay $99 per year](https://serverpress.com/get-desktopserver/) to license the software.

With Desktop Server Premium, you’ll have unlimited site creation and management capabilities. The paid service also gives you access to expedited support response, assisted deployment to any web host, localhost SSL support, and full seamless WP-CLI integration, just to name a few things.

### **Looking at Local**

As a more recent local dev tool, Local has gone by a few different names in its comparably shorter lifespan. First, it went by Pressmatic, before being [acquired by Flywheel](https://wptavern.com/flywheel-acquires-wordpress-local-development-tool-pressmatic), and then it was known as Local by Flywheel for a time. After the Flywheel acquisition, the product was made free for all users, with some major perks for signing up to use the Pro version!

These days, Flywheel has since been [acquired by WP Engine](https://wpengine.com/blog/wp-engine-to-acquire-flywheel/) and there are some additional host specific features for those who deploy to Flywheel or WP Engine. Even on the free version, you can push and pull your sites to and from your server with [Local Connect](https://localwp.com/connect/), but currently you do still have to use Flywheel or WP Engine for hosting.

Additionally, with the Pro version there's also a feature called [MagicSync](https://localwp.com/help-docs/local-pro/how-does-the-magic-sync-viewer-work-in-local-pro/) that "intelligently recommends which files to push or pull and gives you ultimate control over exactly which files should be synced to support your unique workflow." Overall, Local Pro offers some seriously powerful tools for optimizing your workflow, no matter where your sites are hosted!

### **More Local Perks**

Even though it does have a fancy, modern interface and has gone through many changes over its short lifespan thus far, Local is clearly quite accessible and very extensible for web dev novices and experts alike.

This local development tool is just full of useful features including an Apache or Nginx web server, MailHog, SSL certificates, and XDebug support. There are also several [great add-ons](https://localwp.com/add-ons/), and Local allows for developers to [build their own ](https://localwp.com/get-involved/build/)as well, to further modify or extend its functionalities.

Aside from all the great features included with Local, the main product is distributed for free, without limitations, and there's also a very informative and active [Community of users](https://localwp.com/community/) where tons of knowledge and information can be gleaned!

### **Finding the Best Tool for the Job**

While Local Pro has a much steeper price tag than Desktop Server Premium ($20/month compared to $99/year), the free version of Local really has almost no limitations. Neither product has any huge barriers to entry and they are both certainly worth trying out.

Although Desktop Server has been around for much longer, and also has a substantial user base and community built up around it, Local really seems to be the next up and coming local development platform. Whereas Desktop Server has more longevity and a substantial user base, it has fewer “bells and whistles,” and a more standard design.

With all the great features included with the Local app, its extensibility with add-ons, and advanced syncing capabilities, Local is a great choice for all your website development, deployment, and ongoing site maintenance needs!

  
 ****