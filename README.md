# MyVPN

MyVPN is a free VPN for the Mac. It connects through [VPN Gate](https://www.vpngate.net/)'s free volunteer servers,
so websites see you in Japan, South Korea, the US or wherever volunteers are online, and you pick the country on a
world map. This repository holds its **releases** - the app and the feed it updates from. Its source is kept elsewhere.

## Install

On a Mac with macOS 14 or later:

1. Install OpenVPN, the engine MyVPN uses: `brew install openvpn`
2. Download `MyVPN-<version>.dmg` from [Releases](https://github.com/manu-tech-code/myvpn-releases/releases) and drag
   MyVPN to Applications.
3. The app isn't notarized, so the first time, right-click MyVPN and choose **Open**.
4. MyVPN asks for your Mac password once, to install the helper that creates the tunnel.

## Updates

MyVPN updates itself: once a day it reads `appcast.xml` from the latest release, and **Settings › Updates › Check for
Updates…** shows what's new with **Update Now**. Every download's EdDSA signature is checked before it's installed.

## Good to know

The servers are run by volunteers: fine for testing and changing your location, not for banking. The app is ad-hoc
signed, so it's meant for its developer's own Macs.
