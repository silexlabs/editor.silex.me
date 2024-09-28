## Silex instances by Silex Labs

This repo holds the code for the [public Silex instance hosted for free by Silex Labs foundation](https://editor.silex.me) and [The v3 instance too](https://v3.silex.me).

This is also a good example on how to customize Silex. And it has a Dockerfile for easy deployment

## Features

This code adds features to the editor specific to our instance (in `index.js` and `index.pug`):

* [x] Multi-site with the Dashboard plugin
* [x] Automatic deployment to [CapRover](https://caprover.com/) (see the captain-definition file and the file `.github/workflows/caprover.yml`)
* [x] Onboarding: Send an email with [brevo the 1st time we see a user](https://brevo.co/) + use Silex notification system to guide users through the first steps
* [x] Enable or disable cloud services and hosting providers with env vars
* [ ] Analytics: add a tag in Silex editor

## Environment variables

You can set the following environment variables to customize the instance:

| Name | Description | Type | Default value |
|------|-------------| ---- |---------------|
| `STORAGE_CONNECTORS` | List of storage connectors to enable | `ftp` or `gitlab` or `gitlab2` or `fs` | `ftp` |
| `HOSTING_CONNECTORS` | List of hosting connectors to enable | `ftp` or `gitlab` or `gitlab2` or `fs` or `download` | `ftp,download` |
| `SILEX_FS_ROOT` | Root folder for the file system storage | string | current directory + `/silex/storage/` |
| `SILEX_FS_HOSTING_ROOT` | Root folder for the file system hosting | string | current directory + `/silex/hosting/` |
| `FTP_STORAGE_PATH` | Path to the FTP storage | string | `` |
| `FTP_HOSTING_PATH` | Path to the FTP hosting | string | `` |
| `GITLAB_DISPLAY_NAME` | Display name for the Gitlab storage | string | `Gitlab` |
| `GITLAB_DOMAIN` | Domain of the Gitlab server, e.g `https://gitlab.com` | string | required with gitlab connector |
| `GITLAB_CLIENT_ID` | Client ID for the Gitlab OAuth | string | required with gitlab connector |
| `GITLAB_CLIENT_SECRET` | Client secret for the Gitlab OAuth | string | required with gitlab connector |
| `GITLAB2_DISPLAY_NAME` | Display name for the 2nd Gitlab storage | string | `Gitlab2` |
| `GITLAB2_DOMAIN` | Domain of the 2nd Gitlab server, e.g `https://gitlab.com` | string | required |
| `GITLAB2_CLIENT_ID` | Client ID for the 2nd Gitlab OAuth | string | required |
| `GITLAB2_CLIENT_SECRET` | Client secret for the 2nd Gitlab OAuth | string | required |

## Support

[Please use the main Silex repository](https://github.com/silexlabs/Silex/) for docs and issues
