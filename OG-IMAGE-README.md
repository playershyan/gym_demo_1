# Generating OG Image for Social Media Sharing

To generate an OG image that shows your homepage preview:

## Option 1: Using Puppeteer (Recommended)

1. Install dependencies:
```bash
npm install puppeteer
```

2. Run the generation script:
```bash
node generate-og-image.js
```

3. This will create `og-image.png` in the root directory. Upload this to your `public` folder or root directory.

## Option 2: Using Screenshot Service

You can use a screenshot API service like:
- https://screenshotapi.io
- https://urlbox.io
- https://www.screenshotone.com

Set the OG image URL to:
```
https://api.screenshotapi.io/v1/screenshot?url=https://gym-demo-1-tau.vercel.app&width=1200&height=630
```

## Option 3: Manual Screenshot

1. Open your deployed site: https://gym-demo-1-tau.vercel.app
2. Use browser dev tools to set viewport to 1200x630
3. Take a screenshot
4. Save as `og-image.png` in your public/root folder

## Update HTML

Once you have the image, make sure the meta tags point to it:
```html
<meta property="og:image" content="https://gym-demo-1-tau.vercel.app/og-image.png">
```

