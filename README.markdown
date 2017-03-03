# Vagrant Wordpress Examples

An example of how to set up a Wordpress install on a Vagrant virtual machine.

## Environment Variables

You may customize the install with a few environment variables:

- ``VAGRANT_WP_DOMAIN_NAME``: The domain name to use for the site. To access it locally, you'll need to edit your hosts file. Defaults to ``example.site``.
- ``VAGRANT_WP_PASS``: The password for the admin user. Defaults to ``vagrant``.
- ``VAGRANT_WP_SITE_TITLE``: The site title. Defaults to "Example Site".
- ``VAGRANT_WP_USER``: The admin user name. Defaults to ``webmaster``.

## Plugins

Plugins listed in the ``deploy/plugins.csv`` will be installed automatically.

## Settings

The ``deploy/config.csv`` file is loaded into WP options.
