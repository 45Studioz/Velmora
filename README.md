# VELMORA MODEL HUB — FIXED v2

## What was fixed

### 1. Images not loading
The actual Velmora logo and Fredrick Ngugi photo are included in the website package, in the exact locations used by the HTML:

- `assets/velmora-logo.png`
- `assets/models/fredrick-ngugi.jpeg`

The HTML uses relative paths beginning with `./`, so the images work when the **whole project folder** is deployed.

### 2. Adding models
Models are now controlled by `models.js`. You no longer need to redesign the HTML for every new model.

### Add a new model

1. Put the model's photo in `assets/models/`.
2. Open `models.js`.
3. Copy the commented model template and fill in:
   - id
   - name
   - gender
   - specialties
   - socialLabel
   - socialUrl
   - image
   - bio
4. Save and redeploy.

Example:

{
  id: "jane-wanjiku",
  name: "Jane Wanjiku",
  gender: "Female Model",
  specialties: ["Runway", "Commercial"],
  socialLabel: "@jane_wanjiku",
  socialUrl: "https://www.instagram.com/jane_wanjiku/",
  image: "assets/models/jane-wanjiku.jpg",
  bio: "Professional runway and commercial model."
},

### Important
The image filename must exactly match the filename in `models.js`.

## Why there isn't an "upload model" button

A normal static website cannot permanently store new uploads on its public server from a browser. That requires a backend/database or a CMS.

This version is therefore built to make manual updates easy and reliable. If Velmora later wants a real admin dashboard:

`Velmora Admin → Add Model → Upload Photo → Save`

the site can be upgraded to a CMS/database-backed system.

## Deployment

Deploy the entire project, not only `index.html`.

No build command is required. It is a static site and is ready for Vercel or another static host.

## Contact

WhatsApp/Phone: +254 788 504 540
Email: velmoramodelhub@gmail.com
Location: Thika, Kiambu County, Kenya

## Social

TikTok: @velmora_254
Instagram: @velmora_254
Fredrick: @mr_kiambu_county
