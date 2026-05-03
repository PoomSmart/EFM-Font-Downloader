# EFM Font Downloader

A script to download [EmojiFontManager](https://github.com/PoomSmart/EmojiFontManager)-compatible emoji fonts directly from [EmojiFonts GitHub repository](https://github.com/PoomSmart/EmojiFonts) onto your jailbroken iOS device.

## Important Notes

- The device must support TLS 1.2 authentication (minimum support for downloading files off of GitHub). This translates into supporting OpenSSL 1.0.1 or newer.
    - This requires the device to have the up-to-date jailbreak bootstrap.
    - Alternatively, the device must use `cURL` version `7.58.0-2` or higher, and has `USERTrust ECC Certification Authority` certificate installed. The user can add `https://repo.bingner.com` repository and upgrade `cURL` if they are on iOS 10 or lower.
- If `wget` is used and the device is jailbroken with XinaA15, `.wgetrc` must be correctly configured. You may run this command once to configure it correctly: `echo "ca_certificate = /var/jb/etc/ssl/cert.pem" >> /var/mobile/.wgetrc && ln -s /var/mobile/.wgetrc /var/root/.wgetrc`

## Insecure fallback

If for any reasons you still cannot download the emoji font from GitHub, use the insecure counterpart of this package: `EFM Font Downloader (Insecure)`. This one skips the certificate verification step and downloads the files directly.

# Usage

```bash
# Install
efmdl AppleColorEmoji-HD AppleColorEmoji_HD 15.0.0

# Uninstall
efmrm AppleColorEmoji_HD
```
