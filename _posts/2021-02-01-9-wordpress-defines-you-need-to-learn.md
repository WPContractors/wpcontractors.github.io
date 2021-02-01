---
date: 2021-02-01 21:18:54 +0000
author: jessica-devine
categories: []
title: '9 WordPress Defines You Need to Learn '
description: 'As a WordPress Contractor, you probably know how powerful defines can
  be inside the wp-config.php file. In this guide, we are sharing nine WordPress defines
  we suspect you didn''t already know. '
image: "/uploads/alex-bachor-fwst3ppoe-a-unsplash-1.jpg"
thumbnail: "/uploads/alex-bachor-fwst3ppoe-a-unsplash.jpg"
color_overlay: ''

---
As a WordPress Contractor, you probably know how powerful defines can be inside the wp-config.php file. In this guide, we are sharing nine WordPress defines we suspect you didn't already know. Get your notebooks ready as we're about to share some awesome tricks and tips.

**_Note: Place these defines in wp-config.php just above the line #._**

### **1. Skip themes/plugins in core upgrades**

    define('CORE_UPGRADE_SKIP_NEW_BUNDLED', true);

This define stops WordPress core updates from reinstalling unused, bundled themes (like twentytwenty) and plugins (like hello dolly).

### **2. Control core update types**

    define('WP_AUTO_UPDATE_CORE', 'minor');

The above define allows WordPress to perform minor updates ONLY (ie. 5.5.x -> 5.6.x) but not major versions (ie. 5.9.x -> 6.0.x). This is extremely useful as major updates are known to cause the most issue when updating WordPress. Whereas minor updates are less likely to cause any massive problem.

    define('AUTOMATIC_UPDATER_DISABLED', true);

Although, you can even disable all updates completely (if you needed to for some reason or another).

### **3. Support outbound connections through a proxy server (amazing for intranet sites)**

    define('WP_PROXY_HOST', '192.168.0.1');
    define('WP_PROXY_PORT', '8000');
    define('WP_PROXY_USERNAME', '');
    define('WP_PROXY_PASSWORD', '');
    define('WP_PROXY_BYPASS_HOSTS', 'localhost');

Make sure to leave **WP_PROXY_USERNAME** & **WP_PROXY_PASSWORD** blank unless your network is using basic authentication. If it is, just fill in the user/password in the quotes.

### **4. Use a variable HOME and SITEURL**

You can override the database’s rigid HOME and SITEURL constant and allow the global host variable to be used instead:

    define ('WP_SITEURL', 'https://' . $_SERVER['HTTP_HOST']);
    define ('WP_HOME', 'https://' . $_SERVER['HTTP_HOST']);

This handy trick allows for multiple domains to be used with the same WordPress instance. For example, you can pair the above with these next two to use another domain for your /wp-admin/ than your user-facing public site (more on this method here):

    define ('COOKIE_DOMAIN', 'THING.YOURDOMAIN.COM');
    define ('WP_CONTENT_URL', "https://YOURDOMAIN.COM/wp-content");

**TIP**: Using $_SERVER\['HTTP_HOST'\] may cause WP-CLI to throw errors when running commands because the variable is not set during its runtime. It looks like this:

    PHP Notice: Undefined index: HTTP_HOST in phar:///usr/local/bin/wp/vendor/wp-cli/wp-cli/php/WP_CLI/Runner.php...

Thankfully, it doesn’t actually break anything – it’s just irritating. You can solve it with a handy condition like this before the above defines (just make sure to change YOURDOMAIN.COM:

    if (defined('WP_CLI') && WP_CLI) {
    $_SERVER['HTTP_HOST'] = $_SERVER['SERVER_NAME'] = 'YOURDOMAIN.COM'; }

### **5. Control autosave interval**

This define helps to prevent your database from getting bloated. As it sets the total number of allowed revisions per post/page. It also defines the interval at which posts/pages are snapshotted with the following:

    define('WP_POST_REVISIONS', 5);
    define('AUTOSAVE_INTERVAL', 300);

The AUTOSAVE_INTERVAL is set in seconds so 300 = 5 minutes.

This trick can be particularly useful when handing a project over to a client, especially if they're only updating content on the website and not too knowledgeable of WordPress core functions.

### **6. Set the interval to automatically empty trash (in days)**

    define('EMPTY_TRASH_DAYS', 2);

Another fantastic define to automate the emptying of trash in WordPress, and prevent further database bloat.

### **7. Compress all WordPress scripts into one request**

    define('CONCATENATE_SCRIPTS', true);

This reduces the amount of requests made by WordPress by compressing and joining all scripts into one single bundle. Which can help support overall Website performance.

### **8. Redirect non-existent pages instead of 404’ing**

    define('NOBLOGREDIRECT', 'https://YOURDOMAIN.COM/are-you-lost');

The above WordPress define is a great addition to the overall user experience and user interface. Rather than a boring 404 page, you can use a custom page to help the user get back on track.

### **9. Set an interval for WordPress mail**

Finally, we close with some mail defines. The below will set the WP_MAIL_INTERVAL in sections. Note that 300 seconds is 5 minutes.

    define('WP_MAIL_INTERVAL', 300);

**BONUS**: List all loaded defines available on your site

    print_r(@get_defined_constants());

That's it, pencils down! We bet you've learned something new today. Be sure to try out one of these new tricks as soon as you can!