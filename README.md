# QR Studio

A self-contained QR code generator for GitHub Pages. All HTML, CSS, JavaScript, icons, and the QR encoder are included in `index.html`. No API key, CDN, npm install, or build step is needed.

## Use it

1. Enter a complete website address, such as `https://example.com`, or any text. The content is encoded exactly as entered, including whitespace.
2. Choose a PNG size: 1024, 2048, or 4096 pixels square.
3. Click **Generate QR code**. You can also use Ctrl+Enter or Command+Enter while typing.
4. **Download PNG** saves the actual QR image, without page styling or branding.
5. **Save / share** opens your device's native share menu when file sharing is available, with an image-saving dialog as a fallback. On a phone, choose **Save Image**, **Add to Photos**, or the equivalent if offered. You can also touch and hold the image in the dialog.

Browsers cannot silently write into a phone's Photos library. Available share and save actions depend on the browser and operating system. A downloaded PNG may go to Files/Downloads instead of Photos; open it there and use the device's share/save controls to add it to Photos. Native web sharing normally requires HTTPS, which GitHub Pages provides. Regular QR generation and PNG downloads also work when you open the HTML locally.

Web Share reference: https://developer.mozilla.org/en-US/docs/Web/API/Navigator/share

## Included

- Staggered fade/slide animation when the page opens.
- Lift, glow, and light sweep when hovering over Generate.
- Press, ripple, loading, and QR reveal animations when generating.
- Responsive layout, keyboard controls, labeled inputs, and accessible status messages.
- Reduced-motion support using the device's accessibility preference.
- Real PNG export with black modules, a white background, and at least a four-module quiet zone.
- UTF-8 support for non-Latin text and emoji, with medium-or-better error correction.
- Input validation and stale-result protection: edit the text or size, then generate again before saving.
- Local generation, no analytics, no external requests, and no stored input history.

The input is limited to 2,000 UTF-8 bytes. Non-Latin characters and emoji use multiple bytes. Shorter content produces less-dense codes that are generally easier to scan. The QR image itself has no expiry; a linked website may still change or stop working.
QR encoder: Project Nayuki's QR Code generator library, used under its MIT license. The full copyright and license notice is retained in the HTML.

https://www.nayuki.io/page/qr-code-generator-library

This package contains website files; it has not been published to a GitHub repository automatically.
