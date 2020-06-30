# Ubuntu Configuration UI Customisation

This snap allows the UI of the [device-config](https://github.com/CanonicalLtd/device-config) snap to be customised via a 
content interface.

## Using the snap
The `device-config-ui` is intended to be forked and customised with a company's own branding.
The `custom` folder contains the files for customisation:

- `custom.css`: CSS file to override the web page styles
- `custom.yaml`: override the text in the title and footer
- `logo.png`: the logo that appears in the header
- `favicon.png`: web app favicon
- `banner.png`: the background banner on the home page

## Building the application
The application is packaged as a [snap](https://snapcraft.io/docs) and can be
built using the `snapcraft` command. The [snapcraft.yaml](snap/snapcraft.yaml)
is the source for building the application and the name of the snap needs to be
modified in that file.

Both the `device-config` and `device-config-ui` snaps are intended to be forked
and renamed with a company's own branding.

## Connecting the interface
The snap can be connected to the device-config snap via:

```bash
sudo snap connect device-config-demo:web-resources device-config-ui:web-resources
```
(assuming that the device-config snap is called `device-config-demo`)
