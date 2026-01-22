# Creating a Chrome DMG Installer

## Prerequisites
Verify Chrome is installed:
```bash
test -d "/Applications/Google Chrome.app" && echo FOUND || echo MISSING
```

## Create Basic DMG
```bash
hdiutil create -volname "Google Chrome" -srcfolder "/Applications/Google Chrome.app" -ov -format UDZO "GoogleChrome.dmg"
```

## Create Installer-Style DMG (Recommended)
```bash
mkdir -p /tmp/chrome_dmg && cp -R "/Applications/Google Chrome.app" /tmp/chrome_dmg/ && ln -s /Applications /tmp/chrome_dmg/Applications && hdiutil create -volname "Google Chrome Installer" -srcfolder /tmp/chrome_dmg -ov -format UDZO "GoogleChromeInstaller.dmg" && rm -rf /tmp/chrome_dmg
```

The installer-style DMG includes:
- Chrome application
- Applications folder shortcut for drag-and-drop installation
- Standard macOS installer convention
