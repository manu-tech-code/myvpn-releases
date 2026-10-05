# MyVPN

MyVPN is a free VPN for the Mac. It connects through [VPN Gate](https://www.vpngate.net/)'s free volunteer servers,
so websites see you in Japan, South Korea, the US or wherever volunteers are online, and you pick the country on a
world map. This repository holds its **releases** - the app and the feed it updates from. Its source is kept elsewhere.

## Install

On a Mac with Apple silicon and macOS 14 or later, paste this into Terminal:

```bash
curl -fsSL https://github.com/manu-tech-code/myvpn-releases/releases/latest/download/install.sh | bash
```

It puts MyVPN in Applications and opens it. MyVPN then asks for your Mac password once, to install the helper that
creates the tunnel. Running the command again updates MyVPN to the latest version.

### Or with the disk image

1. Download `MyVPN-<version>.dmg` from [Releases](https://github.com/manu-tech-code/myvpn-releases/releases) and drag
   MyVPN to Applications.
2. MyVPN isn't notarized, so macOS won't open it the first time. Open **System Settings › Privacy & Security** and
   click **Open Anyway** next to MyVPN.
3. MyVPN asks for your Mac password once, to install the helper that creates the tunnel.

There's nothing else to install: OpenVPN, the engine that does the encryption, comes inside MyVPN.

## Updates

MyVPN updates itself: once a day it reads `appcast.xml` from the latest release, and **Settings › Updates › Check for
Updates…** shows what's new with **Update Now**. Every download's EdDSA signature is checked before it's installed.

## Good to know

The servers are run by volunteers: fine for testing and changing your location, not for banking. The app is ad-hoc
signed, so it's meant for its developer's own Macs.

## Open-source parts

MyVPN includes [OpenVPN](https://github.com/OpenVPN/openvpn) (GPL-2.0), [OpenSSL](https://github.com/openssl/openssl)
(Apache-2.0), [LZO](https://www.oberhumer.com/opensource/lzo/) (GPL-2.0), [LZ4](https://github.com/lz4/lz4) (BSD) and
[pkcs11-helper](https://github.com/OpenSC/pkcs11-helper) (BSD/GPL), unmodified. Their licenses are inside the app, in
`MyVPN.app/Contents/Resources/OpenVPN-licenses`.
