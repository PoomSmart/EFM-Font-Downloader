# EFM Font Downloader

A script to download [EmojiFontManager](https://github.com/PoomSmart/EmojiFontManager)-compatible emoji fonts directly from [EmojiFonts GitHub repository](https://github.com/PoomSmart/EmojiFonts) onto your jailbroken iOS device.

## Important Notes

- The device must support TLS 1.2 authentication (minimum support for downloading files off of GitHub). This translates into supporting OpenSSL 1.0.1 or newer.
- If `wget` is used and the device is jailbroken with XinaA15 (a.k.a deprecated and abandoned jailbreak), `.wgetrc` must be correctly configured. You may run this command once to configure it correctly: `echo "ca_certificate = /var/jb/etc/ssl/cert.pem" >> /var/mobile/.wgetrc && ln -s /var/mobile/.wgetrc /var/root/.wgetrc`

## Known issues

On iOS 11 Electra jailbreak, the script will fail to download the files from GitHub Releases due to failure to verify GitHub's certificate. The reason is that the jailbreak bootstrap has long been outdated and no longer maintained. The current workaround is to use the insecure counterpart of this package: `EFM Font Downloader (Insecure)`. This one skips the certificate verification step and downloads the files directly.

# Usage

```bash
# Install
efmdl AppleColorEmoji-HD AppleColorEmoji_HD 15.0.0

# Uninstall
efmrm AppleColorEmoji_HD
```
