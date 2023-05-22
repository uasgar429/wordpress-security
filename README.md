# wordpress-security

**Disable file editing in WordPress admin **

Add below code in wp-config.php
define( 'DISALLOW_FILE_EDIT', true );

**Disable XML-RPC for WordPress **

Add below code in .htaccess file 
<Files xmlrpc.php>
Order Allow,Deny
Deny from all
</Files>****


**Hide Wp Version **

Add below code in your theme's function.php file
function mani_remove_wp_version_rss() {
 return'';
 }
add_filter('the_generator','mani_remove_wp_version_rss');
