# Honda Blade 2018 Sales Website

A single-page landing page designed to list a 2018 Honda Blade motorcycle for sale in Vietnam. Built using the HTML5 UP "Story" template framework.

## Directory Structure
```text
├── assets/
│   ├── css/
│   └── js/
│       ├── jquery.min.js
│       ├── browser.min.js
│       ├── breakpoints.min.js
│       ├── util.js
│       └── main.js
├── images/
│   ├── honda/
│   │   ├── IMG_1348.webp to IMG_1391.webp (Trip photos)
│   │   ├── IMG_3115.webp to IMG_3124.webp (Inspection photos part 1)
│   │   ├── IMG_3125.mp4 to IMG_3128.mp4 (Demonstration videos)
│   │   └── IMG_3129.webp to IMG_3136.webp (Inspection photos part 2)
│   └── banner.jpg
└── index.html

## Modifications to Core Template Files

### 1. WebP Lightbox Support
* **File modified:** `assets/js/main.js` (Line 12)
* **Description:** The image extension validation check was updated to allow `.webp` files to load natively inside the template lightbox.

```javascript
if (!href.match(/\.(jpg|gif|png|mp4|webp)$/))
    return;

### 2. Scroll-to-Play Video Automation
* **File modified:** `assets/js/main.js` (Bottom of file)
* **Description:** A custom Intersection Observer script handles video behavior on scroll.
* **Requirements:**
  * Target elements must use the class `class="autoplay-video"`.
  * Videos must include `muted` and `loop` properties in the HTML to bypass browser autoplay restrictions.
  * Playback triggers automatically when a video occupies 60% or more of the current viewport. The video pauses instantly when scrolled out of view to avoid overlapping audio tracks.

  ### 3. Smooth-Scroll Anchor Animations
* **File modified:** `index.html`
* **Description:** Buttons linking to the contact section (`href="#contact"`) have been assigned the `smooth-scroll-middle` class to invoke the custom jQuery scroll animation instead of an instant browser jump.