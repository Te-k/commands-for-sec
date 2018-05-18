# Wordpress

Wordpress CLI :
* Verify Wordpress checksums : `wp core verify-checksums`
* Get Wordpress version : `wp core version`
* List users : `wp user list`
* List plugins : `wp plugin list`
* List posts : `wp post list`
* List deleted posts : `wp post list --post_status=trash`
* Update uptions : `wp option update home 'http://example.com'`
* Search and replace in db : `wp search-replace 'example.dev' 'example.com' --skip-columns=guid`

