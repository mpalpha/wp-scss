=== WP-SCSS ===
Contributors: connectthink
Donate link: http://example.com/
Tags: sass, scss, css
Plugin URI: https://github.com/ConnectThink/WP-SCSS
Requires at least: 3.0.1
Tested up to: 3.6
Stable tag: 1.0
License: GPLv3 or later
License URI: http://www.gnu.org/copyleft/gpl.html

Compiles .scss files to .css and enqueues them.

== Description ==

Compiles .scss files on your wordpress install using [lefo's scssphp](https://github.com/leafo/scssphp). Includes settings page for configuring directories, error reporting, compiling options, and auto enqueuing.

The plugin only compiles when changes have been made to the scss files. Compiles are made to the matching css file, so disabling this plugin will not take down your stylesheets. In the instance where a matching css file does not exist yet, the plugin will create the appropriate css file in the css directory. 

[Get detailed instructions on github](https://github.com/ConnectThink/WP-SCSS)

== Installation ==

1. Upload plugin to plugins directory
2. Active plugin through the 'Plugins' menu in Wordpress
3. Configure plugin options through settings page `settings -> WP-SCSS`.

== Frequently Asked Questions ==

= How do I @import subfiles =

You can import other scss files into parent files and compile them into a single css file. To do this, use @import as normal in your scss file. All imported file names *must* start with an underscore. Otherwise they will be compiled into their own css file.

When importing in your scss file, you can leave off the underscore.
    
> `@import 'subfile';`
    

= Does this plugin support Compass? = 
Currently there isn't a way to fully support [compass](https://github.com/chriseppstein/compass) with a php compiler. If you want limited support, you can manually import the compass framework. You'll need both the _compass.scss and compass directory.
    
    
> `compass / frameworks / compass / stylesheets /
> `@import 'compass';`


Alternatively, you can include [Bourbon](https://github.com/thoughtbot/bourbon) in a similar fashion. 

= Can I use .sass syntax with this Plugin? =
This plugin will only work with .scss format.

= It's not updating my css, what's happening? = 
Do you have errors printing to the front end? If not, check your log file in your scss directory. The css will not be updated if there are errors in your sass file(s).

Make sure your directories are properly defined in the settings. Paths are defined from the root of the theme.

= I'm having other issues and need help =
If you are having issues with the plugin, create an issue on [github](https://github.com/ConnectThink/WP-SCSS), and we'll do our best to help.

== Changelog ==

= 1.0 =
* Initial Build