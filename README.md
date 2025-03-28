[![Gitpod ready-to-code](https://img.shields.io/badge/Gitpod-ready--to--code-blue?logo=gitpod)](https://gitpod.io/#https://github.com/plausible/wordpress)

# [Plausible Analytics](https://plausible.io "Plausible Analytics") #

![WordPress version](https://img.shields.io/wordpress/plugin/v/plausible-analytics.svg) ![WordPress Rating](https://img.shields.io/wordpress/plugin/r/plausible-analytics.svg) ![WordPress Downloads](https://img.shields.io/wordpress/plugin/dt/plausible-analytics.svg)

Welcome to the Plausible Analytics WordPress Plugin GitHub repository. This is the code source and the center of active development. Here you can browse the source, look at open issues, and contribute to the project.

## Getting Started 

If you're looking to contribute or actively develop on Plausible Analytics then skip ahead to the [Local Development](https://github.com/plausible/wordpress/#local-development) section below. The following is if you're looking to actively use the plugin on your WordPress site.

### Minimum Requirements

* WordPress 4.8 or greater
* PHP version 5.6 or greater
* MySQL version 5.5 or greater

### Automatic installation

Automatic installation is the easiest option as WordPress handles the file transfers itself and you don't need to leave your web browser. To do an automatic install of Plausible Analytics, log in to your WordPress dashboard, navigate to the Plugins menu and click "Add New".

In the search field type "Plausible Analytics" and click Search Plugins. Once you have found the plugin you can view details about it such as the point release, rating and description. Most importantly of course, you can install it by simply clicking "Install Now".

### Manual installation

The manual installation method involves downloading our donation plugin and uploading it to your server via your favorite FTP application. The WordPress codex contains [instructions on how to do this here](https://codex.wordpress.org/Managing_Plugins#Manual_Plugin_Installation).


### Support
This repository is not suitable for support. Please don't use GitHub issues for support requests. To get support please use the following channels:

* [WP.org Support Forums](https://wordpress.org/support/plugin/plausible-analytics) - for all users

## Local Development 

To get started developing on the Plausible Analytics WordPress Plugin you will need to perform the following steps:

1. Create a new WordPress site with `plausible.test` as the URL

2. `cd` into your local plugins directory: `/path/to/wp-content/plugins/`

3. Clone this repository from GitHub into your plugins directory: `https://github.com/plausible/wordpress.git`

4. Run composer to set up dependencies: `composer install`

5. Run npm install to get the necessary npm packages: `npm install`

6. Activate the plugin in WordPress

That's it. You're now ready to start development.

### NPM Commands

Plausible Analytics relies on several npm commands to get you started:

* `npm run watch` - Live reloads JS and SASS files. Typically you'll run this command before you start development. It's necessary to build the JS/CSS however if you're working strictly within PHP it may not be necessary to run. 
* `npm run dev` - Runs a one time build for development. No production files are created.
* `npm run production` - Builds the minified production files for release.

### Development Notes

* Ensure that you have `SCRIPT_DEBUG` enabled within your wp-config.php file. Here's a good example of wp-config.php for debugging:
    ```
     // Enable WP_DEBUG mode
    define( 'WP_DEBUG', true );
    
    // Enable Debug logging to the /wp-content/debug.log file
    define( 'WP_DEBUG_LOG', true );
   
    // Loads unminified core files
    define( 'SCRIPT_DEBUG', true );
    ```
* Commit the `package.lock` file. Read more about why [here](https://docs.npmjs.com/files/package-lock.json). 
* Your editor should recognize the `.eslintrc` and `.editorconfig` files within the Repo's root directory. Please only submit PRs following those coding style rulesets. 
