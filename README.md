[![dependencies](https://david-dm.org/PragmaticClub/ngx-qrcode.svg)](https://david-dm.org/PragmaticClub/ngx-qrcode)
# ngx-qrcode
ngx-qrcode is a simple Angular4 Component for generating QRCode It uses [QRCode.js](https://davidshimjs.github.io/qrcodejs/). QRCode.js supports Cross-browser with HTML5 Canvas and table tag in DOM.

## Install

    npm install ngx-qrcode

## Basic Usage

### Include the component and declare it as Directive

```
import {Component, OnInit} from '@angular/core';
import {QRCodeComponent} from 'ngx-qrcode'

@Component({
  selector: 'YourMainComponent',
  directives: [QRCodeComponent],
  template: `
    <div>
      <qrcode [qrdata]="'My QR code data string'" [size]="256" [level]="'M'"></qrcode>
    </div>
  `
})
```

## Parameters

| Attribute        | Type           | Default | Description  |
| ------------- |-------------| -----|------------|
| qrdata      | String | '' | String to encode |
| size      | Number | 256     | Height / Width |
| level | String | 'M'    | QR Correction level ('L', 'M', 'Q', 'H') |
| colorlight      | String | '#ffffff'     | Dark color |
| colordark      | String | '#000000'     | Light Color |
| usesvg      | Boolean | false     | SVG Output |

## Note

Depending on the size of the *qrdata* to encode, a minimum *size* might be required.

## License
MIT License
