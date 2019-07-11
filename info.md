# Introduction
This is a custom component that enables communication with a Ziggo Mediabox Next within Home Assistant.

![Example of using the Mediabox Next](https://raw.githubusercontent.com/IIStevowII/ziggo-mediabox-next/master/screenshot.PNG)

# Installation
During early development it is only possible to install this component manually.

# Usage
Inside your configuration.yaml add the following lines:
```yaml
media_player:
  - platform: ziggo-mediabox-next
    username: !secret ziggo_username
    password: !secret ziggo_password
```

The username and password need to correspond with the credentials used to login on mijn.ziggo.nl or the Ziggo app.
It is highly recommend to use secrets for these values, as you definitely not want these credentials to become public. These credentials will ONLY be used to retrieve a special token, which is used for communication with the Ziggo Mediabox Next.

## Current features
- Start / stop the device
- Play / pause the screen
- Previous / next channel
- Switch to a specific channel
- Display the current channel name including a snapshot*

* It is not yet possible to retrieve the current channel, so this will only work with channels that are set using this component

## Credits
This entire component is based on a proof of concept published here: https://github.com/basst85/NextRemoteJs/
and forked from: https://raw.githubusercontent.com/IIStevowII/ziggo-mediabox-next

Ziggo Mediabox XL used for certain development choices: https://github.com/b10m/ziggo_mediabox_xl/
