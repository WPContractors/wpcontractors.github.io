---
date: 2020-12-10 15:10:08 +0000
authorz: matt-pritchard
categories: []
title: Level Up Your WordPress Game with WP-CLI
description: Building and managing WordPress websites often require time-consuming
  tasks. Did you know that everything within wp-admin can be completed faster with
  one tool? WP CLI!
image: "/uploads/wp-cli.png"
thumbnail: "/uploads/wp-cli.png"
color_overlay: ''

---
Building and managing WordPress websites often require time-consuming tasks. Did you know that everything within wp-admin can be completed faster with one tool? And did you know that in moments of fatal plugin and theme error, you can respond quickly to mitigate the situation? If this sounds like what you've been looking for, then buckle up and get ready to level up your WordPress game.

### **What is WP CLI?**

WP-CLI is a command-line interface, specifically designed for WordPress. With it, you can quickly toggle plugin status, easily version control your plugins, themes, and WordPress core files. You can even update options in the database and much, much more.

Before we get into the grit of WP-CLI, let's outline some preconditions needed to use this interface. Depending on where your WordPress site is hosted, you may or may not have direct access to this tool, as it requires [SSH access](https://en.wikipedia.org/wiki/SSH_(Secure_Shell)). If you're self-hosted or working with WordPress locally, then feel free to move onto the next section. For those already hosted, check out your hosting providers' support center–if that fails contact their support team to find out.

If self-hosting with a provider like Digital Ocean, their default WordPress image comes with WP CLI automatically installed. If WP CLI is not already installed or you're working locally, then check out these [steps on how to install.](https://wp-cli.org/#installing)

### **Using WP CLI**

Let's start with the basics. Every WP CLI command follows the same pattern of use. More or less, the commands are formatted accordingly.

    wp thing dothething --extra-things

Now that you understand the syntax, let's look at some of the amazing things you can do with WP-CLI.

**Quick tip**, if you run into this error:

> Error: YIKES! It looks like you're running this as root. You probably meant to run this as the user that your WordPress installation exists under.

Add the flat **--allow-root** to your commands.

### **List Plugins & Themes for WP CLI**

With these commands, you can quickly generate nicely formatted tables that contain information such as status, update, and version of your plugins and themes.

    wp plugin list

![](/uploads/pluginlist.png)

    wp theme list

If working with a Multisite substitute, use the flag:

    wp plugin list --url=blog.site.com

Sometimes when your website is experiencing errors from plugins or themes, it can prevent the CLI from displaying results. To bypass this, use the flags:

    wp theme list --skip-plugins --skip-themes

### **Break-Fix Support**

Has your client ever alerted you that their website is down, and all you see on the browser is a white screen or a site-wide 500 error? If so, then you _know_ the panic that sets in. Without a wp-admin dashboard, how are you to access the site? This is where WP CLI shines.

You can quickly disable plugins individually or all at once and easily change the theme.

    wp plugin deactivate bbpress

    wp plugin deactivate --all

    wp theme activate twentytwenty

![](/uploads/installandactivatetheme.png)

What if you only have one theme installed and that's causing the errors? No worries, you can download any theme from the WordPress repository and activate, all in one simple command:

    wp theme install twentytwenty && wp theme activate twentytwenty

Better yet, if you have [WordPress debugging](https://wordpress.org/support/article/debugging-in-wordpress/) enabled you should hopefully have an error identifying the exact plugin or theme causing your issue.

### Version Control

Updating and rolling back plugin/theme and core updates couldn't be any easier than with WP CLI.

1. **To update to the newest plugin, theme or core version:**

    wp core update

![](/uploads/pluginupdate.png)

2. **To force a downgrade:**

    wp core update --version=5.5.4 --force

3. **To downgrade/rollback a plugin or theme:**

    wp plugin update woocommerce --version=4.7.1

### Database

Quickly export, reset, and import databases:

    wp db export

    wp db reset

    wp db import yourfile.sql

**Run a search and replace:**

If you're changing domains or adding SSL to your WordPress site, the following commands are a must in your development toolbelt:

    wp search-replace "old-domain.com" 
    "new.domain.com" --precise --all-tables

    wp search-replace "http://my-domain.com" 
    "https://my.domain.com" --precise --all-tables

You can also use the flag **_--dry-run_** to see what the results of the search and replace would be.

**Important**: when making these types of changes to the database, it's crucial to purge your cache and reset your permalinks with the following:

    wp rewrite flush

    wp cache flush

### Direct Updates within Database

You can even update any option in the wp_options database table. Here are some examples:

**Update site blog description.**

    wp option update blogdescription "My website description"

![](/uploads/blogdescriptionupdate.png)

### Endless Possibilities with WP-CLI

We've only just tipped the iceberg of all things you can do with WP CLI. It's an extremely powerful interface, with endless options. You'll save so much time as a WordPress developer, it's worth your time picking up this new skill. Even if you've never used SSH before, let this be your introduction.

If you want to level up your WordPress game in 2021, apply this knowledge you've learned today!