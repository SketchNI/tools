Tools
=====

## new-cert
A simple wrapper around easyrsa to help me quickly generate a certificate.

This script assumes `easyrsa` in your home folder `$HOME`.

## create-nginx
**Note: This requires sudo access**
Copies the contents of `/etc/nginx/stub` into a new config.

See the file `stub` for contents.

## new-project
**Note: This requires sudo access**

Arguments
- `name`: The name/domain of the site with no tld.

Generates the cert using `new-cert`.
Creates the new nginx config using the stub.
Creates a new Laravel project in `$HOME/<name>` and installs Laravel Breeze, Laravel Dusk, Laravel Telescope and Barry V. D. H.s Laravel IDE Helper as dev dependancies and Laravel Horizon as a regular dependancy.

It will also run the artisan commands to install breeze, dusk and telescope and copy the contents of `config/ide-helper.php` to the project and restart nginx.
