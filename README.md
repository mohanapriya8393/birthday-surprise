# birthday-surprise
# Luxury Birthday QR Website

This is a mobile-first interactive birthday webpage.

## What it does

The opening screen has a baby in the center holding four balloons:

1. Full-name balloon -> pops -> plays the name-reveal video.
2. Little-surprise balloon -> pops -> plays the AI baby invitation video.
3. Venue balloon -> opens the celebration/location page.
4. 12-month balloon -> opens the first-year journey.

The baby's actual name is intentionally NOT written anywhere in the HTML.

## 1. Add your baby photo

Create this folder:

assets

Put your photo inside it as:

assets/baby.jpg

Then find this block in index.html:

<div class="baby" aria-label="Birthday boy">
  <div class="placeholder">
    YOUR BABY PHOTO
    <small>Replace this with your image</small>
  </div>
</div>

Replace it with:

<div class="baby" aria-label="Birthday boy">
  <img src="assets/baby.jpg" alt="Birthday boy">
</div>

For best results, use a clear portrait/full-body photo with the baby already cut out from the background if possible.

## 2. Add your YouTube videos

Open index.html and find:

const CONFIG = {
  NAME_REVEAL_VIDEO_ID: "PASTE_NAME_REVEAL_YOUTUBE_ID",
  SURPRISE_VIDEO_ID: "PASTE_BABY_INVITATION_YOUTUBE_ID",
  GOOGLE_MAPS_LINK: "PASTE_YOUR_GOOGLE_MAPS_LINK"
};

For a YouTube URL like:

https://www.youtube.com/watch?v=ABC123XYZ

use only:

ABC123XYZ

The two videos can be Unlisted on YouTube.

## 3. Add your venue

Replace:
YOUR VENUE NAME
YOUR TIME
YOUR VENUE ADDRESS

Also replace the Google Maps link in CONFIG.

## 4. Add your 12-month photos

The current journey shows elegant numbered placeholders.

You can later replace each:

<div class="ph">01</div>

with:

<img src="assets/month-01.jpg" alt="Month 1">

and similarly for month-02 through month-12.

## 5. Important mobile behavior

The video opens only after the guest taps a balloon. This is intentional: mobile browsers generally allow video playback after a real user interaction.

## 6. Free hosting

The easiest free hosting option is GitHub Pages.

Upload:
- index.html
- assets folder

Then enable GitHub Pages for the repository.

The final Pages URL can be used to create the QR code on the physical invitation.

## 7. Before printing

Test the published URL on:
- Android Chrome
- iPhone Safari
- another phone not logged into your accounts

Test all four balloons, both videos, the map button and all 12 months.
