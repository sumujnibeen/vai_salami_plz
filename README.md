<div align="center">

# Eid Salami

### A Playful Eid Salami Request Website

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3.3-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white)

</div>

A simple and interactive Eid-themed website created to ask for Eid Salami in a fun way. The website starts with an animated greeting and Windows-style notification popups, then presents payment options for bKash, Nagad and Rocket.

## Features

* Animated Eid greeting intro
* Sequential Windows-style notification popups
* Responsive design for mobile, tablet and desktop
* Personal profile section
* bKash, Nagad and Rocket payment options
* Payment account number copy functionality
* QR code support
* Direct payment app launch using deep links
* Google Play fallback for payment applications
* Toast notification after copying the payment number
* Bengali typography using Hind Siliguri and Noto Serif Bengali
* Dark blue glass-inspired interface
* Lightweight CSS animations and optimized visual effects

## Technologies Used

* HTML5
* CSS3
* JavaScript
* Bootstrap 5.3.3
* Google Fonts

## Project Structure

```text
Eid-Salami/
│
├── index.html
│
├── image/
│   ├── bg.png
│   ├── fav.png
│   ├── shafi.png
│   ├── blogo.png
│   ├── nlogo.png
│   ├── rlogo.jpg
│   ├── bikash.JPEG
│   ├── ng.png
│   └── rc.png
│
└── README.md
```

## How It Works

### 1. Intro Animation

When the website loads, an introductory greeting appears:

```text
আস্-সালামু আলাইকুম ভাই
ঈদ মোবারক
```

After the greeting, several animated notification windows appear with different messages requesting Eid Salami.

### 2. Payment Section

After the intro sequence, the main website appears with three payment methods:

* bKash
* Nagad
* Rocket

Each payment card contains:

* Payment service logo
* Account number
* Copy button
* QR code
* Send Money button

### 3. Copy Account Number

Clicking a payment card or the copy button copies the account number to the clipboard.

A confirmation message is then displayed to the user.

### 4. Payment App

The Send Money button attempts to open the corresponding payment application using a deep link.

If the application is unavailable, the website redirects the user toward the corresponding Google Play application page.

## Customization

The payment number can be changed directly inside `index.html`.

Search for:

```javascript
copyNumber('01303021166', this)
```

and replace the number with the desired account number.

The same number should also be updated in the visible payment number:

```html
<span class="pay-num">01303021166</span>
```

## Changing Intro Messages

Intro popup messages are stored inside the `POPUPS` JavaScript array:

```javascript
const POPUPS = [
    {
        icon: '⚠️',
        title: 'সালামি অনুরোধ',
        body: 'সালামি প্রদান করুন।'
    }
];
```

Additional messages can be added or existing messages can be modified from this section.

## Performance Optimization

The website uses several optimizations to reduce unnecessary rendering cost:

* Reduced number of intro popups
* Reduced animation duration
* Removed expensive backdrop blur effects
* Reduced box-shadow intensity
* Limited simultaneous animations
* Used a single `requestAnimationFrame` for popup animation
* Removed `will-change` after popup animation
* Responsive popup positioning

For even faster loading, the background image can be converted from PNG to WebP and preloaded.

## Running Locally

No server or database is required.

Simply open:

```text
index.html
```

in a modern web browser.

## Deployment

The website can be deployed using static hosting services such as GitHub Pages.

Upload the project files while preserving the directory structure, especially the `image` folder.

## Browser Support

The website is designed for modern browsers including:

* Google Chrome
* Microsoft Edge
* Mozilla Firefox
* Safari

Payment deep links depend on the device and whether the corresponding payment application is installed.

## Disclaimer

This project is a personal Eid-themed web project created for entertainment and personal use. Payment information should always be verified before sending money.

## Author

### Shafiul Mujnibeen

CSE Undergraduate
Developer and Designer

---

If you received this website during Eid, you already know what to do.

**Eid Mubarak.**
