# Dropbox Adapter Plugin

Dropbox filesystem adapter plugin for OctoberCMS.

## Installation

There are couple ways to install this plugin.

1. Use October [Marketplace](http://octobercms.com/help/site/marketplace) and __Add to project__ button.
2. Use October backend area *Settings > System > Updates & Plugins > Install Plugins* and type __Renatio.DropboxAdapter__.
3. Use `php artisan plugin:install Renatio.DropboxAdapter` command.
4. Use `composer require renatio/dropboxadapter-plugin` in project root.

## Configuration

Add new filesystem disk in `disks` array in `config/filesystems.php`:

```
'dropbox' => [
    'driver' => 'dropbox',
    'app' => '',
    'authorizationToken' => '',
],
```

Create new app and generate authorization token on the [App Console](https://www.dropbox.com/developers/apps) at Dropbox.

In this configuration file you can also set default filesystem and cloud disk.

To use Dropbox as default uploads/media storage for October installation update `config/cms.php`:

```
'storage' => [

    'uploads' => [
        'disk'   => 'dropbox',
        'folder' => 'uploads',
        'path'   => '/storage/app/uploads',
    ],

    'media' => [
        'disk'   => 'dropbox',
        'folder' => 'media',
        'path'   => '/storage/app/media',
    ],

],
```

## Support

Please use [GitHub Issues Page](https://github.com/mplodowski/dropboxadapter-plugin/issues) to report any issues with plugin.

> Reviews should not be used for getting support or reporting bugs, if you need support please use the Plugin support link.

## Like this plugin?

If you like this plugin, give this plugin a Like or Make donation with [PayPal](https://www.paypal.me/mplodowski).