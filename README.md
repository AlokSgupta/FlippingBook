# Flipping Book Webpage

A beautiful, responsive flipping book webpage that can be hosted and embedded into Google Sites.

## 📋 Setup Instructions

### Step 1: Convert PowerPoint to Images

1. Open your PowerPoint presentation
2. Go to **File → Export → Change File Type → PNG** (or JPEG)
3. Click **Save As** and select a folder
4. Choose "Every Slide" when prompted
5. Your slides will be saved as individual image files

### Step 2: Organize Your Images

1. Create a folder named `slides` in the same directory as `index.html`
2. Rename your exported images to: `slide1.jpg`, `slide2.jpg`, `slide3.jpg`, etc.
3. Place all images in the `slides` folder

Your folder structure should look like:
```
flipping-book/
├── index.html
├── README.md
└── slides/
    ├── slide1.jpg
    ├── slide2.jpg
    ├── slide3.jpg
    └── ...
```

### Step 3: Configure the Book

1. Open `index.html` in a text editor
2. Find the `slides` array (around line 170)
3. Update the configuration:

```javascript
const slides = [
    { type: 'cover', title: 'My Presentation Title', subtitle: 'Your Subtitle Here' },
    { type: 'image', src: 'slides/slide1.jpg' },
    { type: 'image', src: 'slides/slide2.jpg' },
    { type: 'image', src: 'slides/slide3.jpg' },
    // Add more slides as needed
];
```

Add or remove slide entries to match the number of slides you have.

### Step 4: Test Locally

1. Open `index.html` in a web browser
2. Use the **Next** and **Previous** buttons to navigate
3. You can also use **arrow keys** (← →) on your keyboard

### Step 5: Host Online

Choose one of these free hosting options:

#### Option A: GitHub Pages (Recommended)
1. Create a GitHub account (if you don't have one)
2. Create a new repository
3. Upload the `flipping-book` folder contents
4. Go to Settings → Pages
5. Select the main branch and save
6. Your site will be available at: `https://yourusername.github.io/repository-name`

#### Option B: Netlify Drop
1. Go to [app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag and drop the entire `flipping-book` folder
3. Get your instant URL

#### Option C: Vercel
1. Go to [vercel.com](https://vercel.com)
2. Sign up and import your project
3. Deploy with one click

### Step 6: Embed in Google Sites

1. Copy your hosted URL (from Step 5)
2. In Google Sites, click **Insert → Embed**
3. Paste this code:

```html
<iframe src="YOUR_HOSTED_URL" width="100%" height="800" frameborder="0"></iframe>
```

Replace `YOUR_HOSTED_URL` with your actual URL.

## 🎨 Customization

### Change Colors

In `index.html`, find the `<style>` section and modify:

```css
body {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}
```

Change the color codes to your preferred colors.

### Change Book Size

Modify these values in the CSS:

```css
.book {
    width: 800px;
    height: 600px;
}
```

### Add Text Content Instead of Images

You can add text-based slides:

```javascript
{ 
    type: 'text', 
    content: '<h2>Chapter 1</h2><p>Your content here...</p>' 
}
```

## 🎯 Features

- ✅ Responsive design (works on mobile, tablet, desktop)
- ✅ Smooth page-turning animation
- ✅ Keyboard navigation (arrow keys)
- ✅ Page counter display
- ✅ Automatic fallback for missing images
- ✅ Easy to customize

## 🆘 Troubleshooting

**Images not showing:**
- Check that image paths are correct
- Ensure images are in the `slides` folder
- Verify image file names match exactly (case-sensitive)

**Book looks weird on mobile:**
- The design is responsive and should adapt automatically
- Try viewing in landscape mode for better experience

**Can't navigate:**
- Make sure JavaScript is enabled in your browser
- Check browser console for errors (F12)

## 📱 Browser Support

- ✅ Chrome, Edge, Firefox, Safari (latest versions)
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

## 📄 License

Free to use for personal and commercial projects.
