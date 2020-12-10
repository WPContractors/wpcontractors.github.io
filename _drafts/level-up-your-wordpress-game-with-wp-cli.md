---
date: 2020-12-10 15:10:08 +0000
authorz: ''
categories: []
title: Level Up Your WordPress Game with WP-CLI
description: ''
image: "/uploads/wp-cli.png"
thumbnail: "/uploads/wp-cli.png"
color_overlay: ''

---
Building and managing WordPress websites often require time-consuming tasks. Did you know that everything within wp-admin can be completed faster with one tool? And did you know that in moments of fatal plugin and theme error, you can respond quickly to mitigate the situation? If this sounds like what you've been looking for, then buckle up and get ready to level up your WordPress game.

### **What is WP CLI?**

WP-CLI is a command-line interface, specifically designed for WordPress. With it, you can quickly toggle plugin status, easily version control your plugins, themes, and WordPress core files. You can even update options in the database and much, much more.

Before we get into the grit of WP-CLI, let's outline some preconditions needed to use this interface. Depending on where your WordPress site is hosted, you may or may not have direct access to this tool, as it requires [SSH access](https://en.wikipedia.org/wiki/SSH_(Secure_Shell)). If you're self-hosted or working with WordPress locally, then feel free to move onto the next section. For those already hosted, check out your hosting providers' support center–if that fails contact their support team to find out.

If self-hosting with a provider like Digital Ocean, their default WordPress image comes with WP CLI automatically installed. If WP CLI is not already installed or you're working locally, then check out these [steps on how to install.](https://wp-cli.org/#installing)

## **Using WP CLI**

Let's start with the basics. Every WP CLI command follows the same pattern of use. More or less, the commands are formatted accordingly.  

    wp thing dothething --extra-things

Now that you understand the syntax, let's look at some of the amazing things you can do with WP-CLI.

**Quick tip**, if you run into this error:

> Error: YIKES! It looks like you're running this as root. You probably meant to run this as the user that your WordPress installation exists under.

Add the flat **--allow-root** to your commands.