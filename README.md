# scarp-spec

This template should help get you started developing with Vue 3 in Vite.

## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur) + [TypeScript Vue Plugin (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.vscode-typescript-vue-plugin).

## Customize configuration

See [Vite Configuration Reference](https://vitejs.dev/config/).

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```

### Lint with [ESLint](https://eslint.org/)

```sh
npm run lint
```



### Scrap data from https://www.gsmarena.com/

if you have this type data

```
<div id="specs-list">
   <table cellspacing="0" style="max-height: 238px;">
      <tbody>
         <tr class="tr-hover">
            <th rowspan="15" scope="row">Network</th>
            <td class="ttl"><a href="network-bands.php3">Technology</a></td>
            <td class="nfo"><a href="#" class="link-network-detail" data-spec="nettech">GSM / HSPA / LTE / 5G</a></td>
         </tr>
         <tr class="tr-toggle">
            <td class="ttl"><a href="network-bands.php3">2G bands</a></td>
            <td class="nfo" data-spec="net2g">GSM 850 / 900 / 1800 / 1900 </td>
         </tr>
         <tr class="tr-toggle">
            <td class="ttl"><a href="network-bands.php3">3G bands</a></td>
            <td class="nfo" data-spec="net3g">HSDPA 800 / 850 / 900 / 1700(AWS) / 1900 / 2100 </td>
         </tr>
         <tr class="tr-toggle">
            <td class="ttl"><a href="network-bands.php3">4G bands</a></td>
            <td class="nfo" data-spec="net4g">1, 2, 3, 4, 5, 7, 8, 12, 13, 14, 17, 18, 19, 20, 25, 26, 28, 29, 30, 38, 39, 40, 41, 46, 48, 66, 71 - G1MNW</td>
         </tr>
         <tr class="tr-toggle" data-spec-optional="">
            <td class="ttl">&nbsp;</td>
            <td class="nfo">1, 2, 3, 4, 5, 7, 8, 12, 13, 14, 17, 18, 19, 20, 25, 26, 28, 30, 32, 38, 40, 41, 42, 46, 48, 66, 71 - GC3VE</td>
         </tr>
         <tr class="tr-toggle">
            <td class="ttl"><a href="network-bands.php3">5G bands</a></td>
            <td class="nfo" data-spec="net5g">1, 2, 3, 5, 7, 8, 12, 20, 25, 26, 28, 29, 30, 38, 40, 41, 48, 66, 70, 71, 77, 78, 257, 258, 260, 261 SA/NSA/Sub6/mmWave - G1MNW</td>
         </tr>
         <tr class="tr-toggle" data-spec-optional="">
            <td class="ttl">&nbsp;</td>
            <td class="nfo">1, 2, 3, 5, 7, 8, 12, 20, 25, 28, 30, 38, 40, 41, 66, 71, 75, 76, 77, 78 SA/NSA/Sub6 - GC3VE</td>
         </tr>
         <tr class="tr-toggle">
            <td class="ttl"><a href="glossary.php3?term=3g">Speed</a></td>
            <td class="nfo" data-spec="speed">HSPA, LTE-A (CA), 5G</td>
         </tr>
      </tbody>
   </table>
   <table cellspacing="0">
      <tbody>
         <tr>
            <th rowspan="2" scope="row">Launch</th>
            <td class="ttl"><a href="glossary.php3?term=phone-life-cycle">Announced</a></td>
            <td class="nfo" data-spec="year">2023, October 04</td>
         </tr>
         <tr>
            <td class="ttl"><a href="glossary.php3?term=phone-life-cycle">Status</a></td>
            <td class="nfo" data-spec="status">Available. Released 2023, October 12</td>
         </tr>
      </tbody>
   </table>
   <table cellspacing="0">
      <tbody>
         <tr>
            <th rowspan="6" scope="row">Body</th>
            <td class="ttl"><a href="#" onclick="helpW('h_dimens.htm');">Dimensions</a></td>
            <td class="nfo" data-spec="dimensions">162.6 x 76.5 x 8.8 mm (6.40 x 3.01 x 0.35 in)</td>
         </tr>
         <tr>
            <td class="ttl"><a href="#" onclick="helpW('h_weight.htm');">Weight</a></td>
            <td class="nfo" data-spec="weight">213 g (7.51 oz)</td>
         </tr>
         <tr>
            <td class="ttl"><a href="glossary.php3?term=build">Build</a></td>
            <td class="nfo" data-spec="build">Glass front (Gorilla Glass Victus 2), glass back (Gorilla Glass Victus 2), aluminum frame</td>
         </tr>
         <tr>
            <td class="ttl"><a href="glossary.php3?term=sim">SIM</a></td>
            <td class="nfo" data-spec="sim">Nano-SIM and eSIM</td>
         </tr>
         <tr>
            <td class="ttl">&nbsp;</td>
            <td class="nfo" data-spec="bodyother">IP68 dust/water resistant (up to 1.5m for 30 min)</td>
         </tr>
      </tbody>
   </table>
   <table cellspacing="0">
      <tbody>
         <tr>
            <th rowspan="5" scope="row">Display</th>
            <td class="ttl"><a href="glossary.php3?term=display-type">Type</a></td>
            <td class="nfo" data-spec="displaytype">LTPO OLED, 120Hz, HDR10+, 1600 nits (HBM), 2400 nits (peak)</td>
         </tr>
         <tr>
            <td class="ttl"><a href="#" onclick="helpW('h_dsize.htm');">Size</a></td>
            <td class="nfo" data-spec="displaysize">6.7 inches, 108.7 cm<sup>2</sup> (~87.4% screen-to-body ratio)</td>
         </tr>
         <tr>
            <td class="ttl"><a href="glossary.php3?term=resolution">Resolution</a></td>
            <td class="nfo" data-spec="displayresolution">1344 x 2992 pixels, 20:9 ratio (~489 ppi density)</td>
         </tr>
         <tr>
            <td class="ttl"><a href="glossary.php3?term=screen-protection">Protection</a></td>
            <td class="nfo" data-spec="displayprotection">Corning Gorilla Glass Victus 2</td>
         </tr>
         <tr>
            <td class="ttl">&nbsp;</td>
            <td class="nfo" data-spec="displayother">Always-on display</td>
         </tr>
      </tbody>
   </table>
   <table cellspacing="0">
      <tbody>
         <tr>
            <th rowspan="4" scope="row">Platform</th>
            <td class="ttl"><a href="glossary.php3?term=os">OS</a></td>
            <td class="nfo" data-spec="os">Android 14</td>
         </tr>
         <tr>
            <td class="ttl"><a href="glossary.php3?term=chipset">Chipset</a></td>
            <td class="nfo" data-spec="chipset">Google Tensor G3 (4 nm)</td>
         </tr>
         <tr>
            <td class="ttl"><a href="glossary.php3?term=cpu">CPU</a></td>
            <td class="nfo" data-spec="cpu">Nona-core (1x3.0 GHz Cortex-X3 &amp; 4x2.45 GHz Cortex-A715 &amp; 4x2.15 GHz Cortex-A510)</td>
         </tr>
         <tr>
            <td class="ttl"><a href="glossary.php3?term=gpu">GPU</a></td>
            <td class="nfo" data-spec="gpu">Immortalis-G715s MC10</td>
         </tr>
      </tbody>
   </table>
   <table cellspacing="0">
      <tbody>
         <tr>
            <th rowspan="5" scope="row">Memory</th>
            <td class="ttl"><a href="glossary.php3?term=memory-card-slot">Card slot</a></td>
            <td class="nfo" data-spec="memoryslot">No</td>
         </tr>
         <tr>
            <td class="ttl"><a href="glossary.php3?term=dynamic-memory">Internal</a></td>
            <td class="nfo" data-spec="internalmemory">128GB 12GB RAM, 256GB 12GB RAM, 512GB 12GB RAM, 1TB 12GB RAM</td>
         </tr>
         <tr>
            <td class="ttl">&nbsp;</td>
            <td class="nfo" data-spec="memoryother">UFS 3.1</td>
         </tr>
      </tbody>
   </table>
   <table cellspacing="0">
      <tbody>
         <tr>
            <th rowspan="4" scope="row" class="small-line-height">Main Camera</th>
            <td class="ttl"><a href="glossary.php3?term=camera">Triple</a></td>
            <td class="nfo" data-spec="cam1modules">50 MP, f/1.7, 25mm (wide), 1/1.31", 1.2µm, multi-directional PDAF, multi-zone Laser AF, OIS<br>
               48 MP, f/2.8, 113mm (telephoto), 1/2.55", 0.7µm, dual pixel PDAF, OIS, 5x optical zoom<br>
               48 MP, f/2.0, 126˚ (ultrawide), 0.8µm, dual pixel PDAF
            </td>
         </tr>
         <tr>
            <td class="ttl"><a href="glossary.php3?term=camera">Features</a></td>
            <td class="nfo" data-spec="cam1features">Dual-LED flash, Pixel Shift, Ultra-HDR, panorama, Best Take</td>
         </tr>
         <tr>
            <td class="ttl"><a href="glossary.php3?term=camera">Video</a></td>
            <td class="nfo" data-spec="cam1video">4K@30/60fps, 1080p@24/30/60/120/240fps; gyro-EIS, OIS, 10-bit HDR</td>
         </tr>
      </tbody>
   </table>
   <table cellspacing="0">
      <tbody>
         <tr>
            <th rowspan="4" scope="row" class="small-line-height">Selfie camera</th>
            <td class="ttl"><a href="glossary.php3?term=secondary-camera">Single</a></td>
            <td class="nfo" data-spec="cam2modules">10.5 MP, f/2.2, 20mm (ultrawide), 1/3.1", 1.22µm, PDAF</td>
         </tr>
         <tr>
            <td class="ttl"><a href="glossary.php3?term=secondary-camera">Features</a></td>
            <td class="nfo" data-spec="cam2features">Auto-HDR, panorama</td>
         </tr>
         <tr>
            <td class="ttl"><a href="glossary.php3?term=secondary-camera">Video</a></td>
            <td class="nfo" data-spec="cam2video">4K@24/30/60fps, 1080p@30/60fps</td>
         </tr>
      </tbody>
   </table>
   <table cellspacing="0">
      <tbody>
         <tr>
            <th rowspan="3" scope="row">Sound</th>
            <td class="ttl"><a href="glossary.php3?term=loudspeaker">Loudspeaker</a> </td>
            <td class="nfo">Yes, with stereo speakers</td>
         </tr>
         <tr>
            <td class="ttl"><a href="glossary.php3?term=audio-jack">3.5mm jack</a> </td>
            <td class="nfo">No</td>
         </tr>
      </tbody>
   </table>
   <table cellspacing="0">
      <tbody>
         <tr>
            <th rowspan="9" scope="row">Comms</th>
            <td class="ttl"><a href="glossary.php3?term=wi-fi">WLAN</a></td>
            <td class="nfo" data-spec="wlan">Wi-Fi 802.11 a/b/g/n/ac/6e/7, tri-band, Wi-Fi Direct</td>
         </tr>
         <tr>
            <td class="ttl"><a href="glossary.php3?term=bluetooth">Bluetooth</a></td>
            <td class="nfo" data-spec="bluetooth">5.3, A2DP, LE, aptX HD</td>
         </tr>
         <tr>
            <td class="ttl"><a href="glossary.php3?term=gnss">Positioning</a></td>
            <td class="nfo" data-spec="gps">GPS (L1+L5), GLONASS (G1), GALILEO (E1+E5a), QZSS (L1+L5)</td>
         </tr>
         <tr>
            <td class="ttl"><a href="glossary.php3?term=nfc">NFC</a></td>
            <td class="nfo" data-spec="nfc">Yes</td>
         </tr>
         <tr>
            <td class="ttl"><a href="glossary.php3?term=fm-radio">Radio</a></td>
            <td class="nfo" data-spec="radio">No</td>
         </tr>
         <tr>
            <td class="ttl"><a href="glossary.php3?term=usb">USB</a></td>
            <td class="nfo" data-spec="usb">USB Type-C 3.2</td>
         </tr>
      </tbody>
   </table>
   <table cellspacing="0">
      <tbody>
         <tr>
            <th rowspan="9" scope="row">Features</th>
            <td class="ttl"><a href="glossary.php3?term=sensors">Sensors</a></td>
            <td class="nfo" data-spec="sensors">Fingerprint (under display, optical), accelerometer, gyro, proximity, compass, barometer, thermometer (skin temperature)</td>
         </tr>
         <tr>
            <td class="ttl">&nbsp;</td>
            <td class="nfo" data-spec="featuresother">Ultra Wideband (UWB) support</td>
         </tr>
      </tbody>
   </table>
   <table cellspacing="0">
      <tbody>
         <tr>
            <th rowspan="7" scope="row">Battery</th>
            <td class="ttl"><a href="glossary.php3?term=rechargeable-battery-types">Type</a></td>
            <td class="nfo" data-spec="batdescription1">Li-Ion 5050 mAh, non-removable</td>
         </tr>
         <tr>
            <td class="ttl"><a href="glossary.php3?term=battery-charging">Charging</a></td>
            <td class="nfo">30W wired, PD3.0, PPS, 50% in 30 min (advertised)<br>
               23W wireless<br>
               Reverse wireless
            </td>
         </tr>
      </tbody>
   </table>
   <table cellspacing="0">
      <tbody>
         <tr>
            <th rowspan="6" scope="row">Misc</th>
            <td class="ttl"><a href="glossary.php3?term=build">Colors</a></td>
            <td class="nfo" data-spec="colors">Obsidian, Porcelain, Bay</td>
         </tr>
         <tr>
            <td class="ttl"><a href="glossary.php3?term=models">Models</a></td>
            <td class="nfo" data-spec="models">GC3VE, G1MNW</td>
         </tr>
         <tr>
            <td class="ttl"><a href="glossary.php3?term=price">Price</a></td>
            <td class="nfo" data-spec="price"><a href="google_pixel_8_pro-price-12545.php">$ 999.00 / € 1,099.00 / £ 924.48</a></td>
         </tr>
      </tbody>
   </table>
</div>
```

*** But you want something like this ***

```
<h2><span style="color: #0170dc;">Network</span></h2>
<table>
   <tbody>
      <tr>
         <td><span style="color: #555555;"><strong>Technology</strong></span></td>
         <td>GSM / HSPA / LTE / 5G</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>2G bands</strong></span></td>
         <td>GSM 850 / 900 / 1800 / 1900 - SIM 1 &amp; SIM 2</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>3G bands</strong></span></td>
         <td>HSDPA 850 / 900 / 1700(AWS) / 1900 / 2100</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>4G bands</strong></span></td>
         <td>1, 2, 3, 4, 5, 7, 8, 12, 17, 20, 26, 28, 38, 40, 41, 66</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>5G bands</strong></span></td>
         <td>1, 3, 5, 7, 8, 28, 40, 41, 77, 78 SA/NSA/Sub6</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>Speed</strong></span></td>
         <td>HSPA, LTE-A, 5G</td>
      </tr>
   </tbody>
</table>
<h2><span style="color: #0170dc;">Launch</span></h2>
<table>
   <tbody>
      <tr>
         <td><span style="color: #555555;"><strong>Announced</strong></span></td>
         <td>2023, June 06</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>Status</strong></span></td>
         <td>Available. Released 2023, June 13</td>
      </tr>
   </tbody>
</table>
<h2><span style="color: #0170dc;">Body</span></h2>
<table>
   <tbody>
      <tr>
         <td><span style="color: #555555;"><strong>Dimensions</strong></span></td>
         <td>164.9 x 77.3 x 8.4 mm (6.49 x 3.04 x 0.33 in)</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>Weight</strong></span></td>
         <td>202 g (7.13 oz)</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>Build</strong></span></td>
         <td>Glass front (Gorilla Glass 5), glass back (Gorilla Glass 5), plastic frame</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>SIM</strong></span></td>
         <td>Single SIM (Nano-SIM, eSIM) or Hybrid Dual SIM (Nano-SIM, dual stand-by)
            IP67 dust/water resistant (up to 1m for 30 min)
         </td>
      </tr>
   </tbody>
</table>
<h2><span style="color: #0170dc;">Display</span></h2>
<table>
   <tbody>
      <tr>
         <td><span style="color: #555555;"><strong>Type</strong></span></td>
         <td>Super AMOLED, 120Hz, HDR10+, 1000 nits (HBM)</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>Size</strong></span></td>
         <td>6.4 inches, 100.5 cm2 (~82.9% screen-to-body ratio)</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>Resolution</strong></span></td>
         <td>1080 x 2340 pixels, 19.5:9 ratio (~403 ppi density)</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>Protection</strong></span></td>
         <td>Corning Gorilla Glass 5</td>
      </tr>
   </tbody>
</table>
<h2><span style="color: #0170dc;">Platform</span></h2>
<table>
   <tbody>
      <tr>
         <td><span style="color: #555555;"><strong>Os</strong></span></td>
         <td>Android 13, One UI 5.1</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>Chipset</strong></span></td>
         <td>Exynos 1380 (5 nm)</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>CPU</strong></span></td>
         <td>Octa-core (4x2.4 GHz Cortex-A78 &amp; 4x2.0 GHz Cortex-A55)</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>GPU</strong></span></td>
         <td>Mali-G68 MP5</td>
      </tr>
   </tbody>
</table>
<h2><span style="color: #0170dc;">Memory</span></h2>
<table>
   <tbody>
      <tr>
         <td><span style="color: #555555;"><strong>Card Slot</strong></span></td>
         <td>microSDXC (uses shared SIM slot)</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>Internal</strong></span></td>
         <td>128GB 6GB RAM, 128GB 8GB RAM, 256GB 6GB RAM, 256GB 8GB RAM</td>
      </tr>
   </tbody>
</table>
<h2><span style="color: #0170dc;">Main Camera</span></h2>
<table>
   <tbody>
      <tr>
         <td><span style="color: #555555;"><strong>Triple</strong></span></td>
         <td>50 MP, f/1.8, (wide), 1/1.56", 1.0µm, PDAF, OIS
            12 MP, f/2.2, 123˚ (ultrawide), 1.12µm
            5 MP, f/2.4, (macro)
         </td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>Features</strong></span></td>
         <td>LED flash, panorama, HDR</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>Video</strong></span></td>
         <td>4K@30fps, 1080p@30/60fps, 720p@480fps</td>
      </tr>
   </tbody>
</table>
<h2><span style="color: #0170dc;">Selfie Camera</span></h2>
<table>
   <tbody>
      <tr>
         <td><span style="color: #555555;"><strong>Single</strong></span></td>
         <td>32 MP, f/2.2, 26mm (wide), 1/2.8", 0.8µm</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>Features</strong></span></td>
         <td>❌</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>Video</strong></span></td>
         <td>4K@30fps, 1080p@30/60fps</td>
      </tr>
   </tbody>
</table>
<h2><span style="color: #0170dc;">Sound</span></h2>
<table>
   <tbody>
      <tr>
         <td><span style="color: #555555;"><strong>Loudspeaker</strong></span></td>
         <td>Yes, with stereo speakers</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>3.5mm jack</strong></span></td>
         <td>❌</td>
      </tr>
   </tbody>
</table>
<h2><span style="color: #0170dc;">Comms</span></h2>
<table>
   <tbody>
      <tr>
         <td><span style="color: #555555;"><strong>WLAN</strong></span></td>
         <td>Wi-Fi 802.11 a/b/g/n/ac/6, dual-band, Wi-Fi Direct</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>Bluetooth</strong></span></td>
         <td>5.3, A2DP, LE</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>Positioning</strong></span></td>
         <td>GPS, GLONASS, GALILEO, BDS</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>NFC</strong></span></td>
         <td>✅ (market/region dependent)</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>Radio</strong></span></td>
         <td>❌</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>USB</strong></span></td>
         <td>USB Type-C 2.0, OTG</td>
      </tr>
   </tbody>
</table>
<h2><span style="color: #0170dc;">Features</span></h2>
<table>
   <tbody>
      <tr>
         <td><span style="color: #555555;"><strong>Sensors</strong></span></td>
         <td>Fingerprint (under display, optical), accelerometer, gyro, compass, barometer (USA only)
            Virtual proximity sensing
         </td>
      </tr>
   </tbody>
</table>
<h2><span style="color: #0170dc;">Battary</span></h2>
<table>
   <tbody>
      <tr>
         <td><span style="color: #555555;"><strong>Type</strong></span></td>
         <td>Li-Po 5000 mAh, non-removable</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>Charging</strong></span></td>
         <td>25W wired</td>
      </tr>
   </tbody>
</table>
<h2><span style="color: #0170dc;">Misc</span></h2>
<table>
   <tbody>
      <tr>
         <td><span style="color: #555555;"><strong>Colors</strong></span></td>
         <td>Virtual proximity sensing</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>Models</strong></span></td>
         <td>SM-A546V, SM-A546U, SM-A546U1, SM-A546B, SM-A546B/DS, SM-A546E, SM-A546E/DS, SM-A5460</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>SAR</strong></span></td>
         <td>0.81 W/kg (head) 0.67 W/kg (body)</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>SAR EU</strong></span></td>
         <td>0.69 W/kg (head) 1.34 W/kg (body)</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>Price</strong></span></td>
         <td><strong>Worldwide: $ 299.00 / € 349.92 / £ 264.00 / ₹ 36,186</strong>
            <strong>Bangladesh: </strong>
            <strong>Official (8GB+128GB) ৳63,999</strong>
            <strong>Unofficial (8GB+128GB) ৳37,000 | (8GB+256GB) ৳40,000</strong>
         </td>
      </tr>
   </tbody>
</table>
<h2><span style="color: #0170dc;">Tests</span></h2>
<table>
   <tbody>
      <tr>
         <td><span style="color: #555555;"><strong>Performance</strong></span></td>
         <td>AnTuTu: 506678 (v9)
            GeekBench: 2703 (v5.1), 2797 (v6)
            GFXBench: 25fps (ES 3.1 onscreen)
         </td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>Display</strong></span></td>
         <td>Contrast ratio: Infinite (nominal)</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>Camera</strong></span></td>
         <td>Photo / Video</td>
      </tr>
      <tr>
         <td><strong><span style="color: #555555;">Loudspeaker</span></strong></td>
         <td> -26.6 LUFS (Good)</td>
      </tr>
      <tr>
         <td><span style="color: #555555;"><strong>Battery Life</strong></span></td>
         <td>Endurance rating 119h</td>
      </tr>
   </tbody>
</table>
<h6>Disclaimer. We can not guarantee that the information on this page is 100% correct.</h6>
```


Then you can use this app or source code and you are free to chnage anything you want