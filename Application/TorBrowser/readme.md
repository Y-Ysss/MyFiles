# TorBrowser

## Change pinned Start Menu icon

Tor Browser is a Firefox based browser and the execute file name is "firefox.exe".
Default tile icon is Firefox.
Tor Browser uses the wrong icon because it uses the same manifest as Firefox.

To fix it, go to your Tor Browser directory, where "firefox.exe" is placed. There is "firefox.VisualElementsManifest.xml".

### Default

**Files**
- ManifestFile : ` TorBrowser\Browser\firefox.VisualElementsManifest.xml ` 
- Default icon-1 : ` TorBrowser\Browser\browser\VisualElements\VisualElements_70.png `
- Default icon-2 : ` TorBrowser\Browser\browser\VisualElements\VisualElements_150.png `

**ManifestFile**
``` xml
<Application xmlns:xsi='http://www.w3.org/2001/XMLSchema-instance'>
  <VisualElements
      ShowNameOnSquare150x150Logo='on'
      Square150x150Logo='browser\VisualElements\VisualElements_150.png'
      Square70x70Logo='browser\VisualElements\VisualElements_70.png'
      ForegroundText='light'
      BackgroundColor='#000f40'/>
</Application>
```

### Customize
Tile icon : [Firefox] -> [Original icon]
**Files**
- ManifestFile : ` TorBrowser\Browser\firefox.VisualElementsManifest.xml ` 
- icon-1 : ` TorBrowser\Browser\browser\VisualElements\FoxTorBrowser-350.png `
- icon-2 : ` TorBrowser\Browser\browser\VisualElements\FoxTorBrowser-127.png `

**ManifestFile**
```xml
<Application xmlns:xsi='http://www.w3.org/2001/XMLSchema-instance'>
  <VisualElements
      ShowNameOnSquare150x150Logo='on'
      Square150x150Logo='browser\VisualElements\FoxTorBrowser-350.png'
      Square70x70Logo='browser\VisualElements\FoxTorBrowser-127.png'
      ForegroundText='light'
      BackgroundColor='#30232D'/>
</Application>

```

### Reload icon command
PowerShell : ` (ls "$env:appdata\microsoft\windows\start menu\programs\Tor Browser.lnk").lastwritetime = get-date `