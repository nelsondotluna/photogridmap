# 🎨 How to Embed Your Flickr Gallery in Framer# Flickr Gallery for Framer



## 📋 **Step-by-Step Instructions:**This is a lightweight, self-contained photo gallery that uses Flickr as an image host. Perfect for embedding in Framer or any website.



### **1. Get Your Gallery URL**## 🚀 Quick Setup

Your gallery is now hosted at:

```1. **Get Flickr API credentials**:

https://nelsondotluna.github.io/photogridmap/framer-embed-gallery.html   - Go to [Flickr App Garden](https://www.flickr.com/services/apps/create/apply/)

```   - Create an app to get your API key

   - Find your User ID and Album ID

### **2. Add Embed Component in Framer**

2. **Configure the gallery**:

1. **Open your Framer project**   - Open `flickr-gallery.html`

2. **From the Insert Menu** (or press `I`):   - Replace these values in the JavaScript:

   - Look for **"Embed"** component     ```javascript

   - Or search for **"Code Component"**     this.apiKey = 'YOUR_FLICKR_API_KEY';

   - Drag it onto your canvas     this.albumId = 'YOUR_ALBUM_ID'; 

     this.userId = 'YOUR_USER_ID';

3. **Configure the Embed:**     ```

   - **URL Field**: Paste your gallery URL:

     ```3. **Use in Framer**:

     https://nelsondotluna.github.io/photogridmap/framer-embed-gallery.html   - Upload the HTML file to your web server

     ```   - In Framer, add an "Embed" component

   - **Width**: Set to `100%` or your desired width   - Use the URL to your hosted HTML file

   - **Height**: Set to at least `600px` (adjust based on your needs)

## 📱 Features

### **3. Framer Component Settings**

- **Responsive grid layout** that adapts to any screen size

#### **Size & Layout:**- **Lightbox viewer** for full-size images

- **Width**: `Fill` or specific pixels- **Tag-based filtering** from your Flickr photo tags

- **Height**: `600px` minimum (or `Auto` if supported)- **Hover effects** with smooth animations

- **Responsive**: Enable for mobile compatibility- **Mobile optimized** with touch-friendly interactions

- **Zero dependencies** - just one HTML file

#### **Advanced Settings:**

- **Overflow**: Set to `Visible` ## 🎨 Customization

- **Background**: `Transparent` (let your site theme show through)

The CSS is organized and easy to customize:

### **4. Alternative: Custom Code Component**

- **Colors**: Change the color scheme in the CSS variables

If the Embed component doesn't work, try the **Code Component**:- **Grid**: Adjust `grid-template-columns` for different layouts

- **Animations**: Modify transition durations and effects

1. **Insert → Code Component**- **Sizing**: Change `aspect-ratio` and `min-width` values

2. **Paste this code** in the component:

## 📋 For Framer Integration

```jsx

export default function FlickrGallery() {### Option 1: Embed Component

  return (```html

    <iframe<iframe src="your-gallery-url.html" width="100%" height="600px"></iframe>

      src="https://nelsondotluna.github.io/photogridmap/framer-embed-gallery.html"```

      style={{

        width: "100%",### Option 2: Custom Code Component

        height: "600px",Copy the CSS and JavaScript into Framer's custom code components.

        border: "none",

        borderRadius: "8px"### Option 3: External Link

      }}Host the file and link to it from your Framer site.

      title="Photo Gallery"

    />## 🔧 API Configuration

  )

}To use real Flickr data, uncomment the `fetchFlickrPhotos()` method and replace the mock data call:

```

```javascript

### **5. Mobile Responsive Setup**// Replace this line:

const photos = this.getMockPhotos();

The gallery automatically adapts:

- **Desktop**: 4 columns// With this line:

- **Tablet**: 3 columns  const photos = await this.fetchFlickrPhotos();

- **Mobile**: 2 columns```



In Framer, make sure your embed component is set to:## 🖼️ Image Sizes

- **Responsive Breakpoints**: Enable

- **Mobile Height**: Increase to `800px+` for mobile viewingThe gallery uses:

- **Medium (400px)** for grid thumbnails

## 🎨 **Customization Options**- **Large (1024px)** for lightbox display

- Automatically falls back if sizes aren't available

You can customize colors to match your Framer theme by editing the CSS in your hosted file:

## 📱 Mobile Support

### **Key Style Changes:**

```css- Touch-friendly lightbox controls

.filter-tag.active {- Responsive grid that works on all devices  

    color: #YOUR_BRAND_COLOR;  /* Change active filter color */- Optimized image loading for mobile connections

}

This approach gives you all the benefits of using Flickr as your image CDN while keeping the gallery lightweight and easily embeddable in Framer!
.gallery-grid {
    grid-template-columns: repeat(3, 1fr);  /* Change to 3 columns */
}

.photo-item {
    border-radius: 12px;  /* More rounded corners */
}
```

## 🔧 **Configuration Changes**

To use different Flickr albums, edit the JavaScript in your file:

```javascript
this.apiKey = 'YOUR_API_KEY';     // Your Flickr API key
this.albumId = 'YOUR_ALBUM_ID';   // Different album
this.userId = 'YOUR_USER_ID';     // Your Flickr user ID
```

## 📱 **Testing Your Setup**

1. **Preview in Framer**: Use the preview mode to test
2. **Check Mobile**: Test responsive behavior 
3. **Test Filters**: Make sure tag filtering works
4. **Test Lightbox**: Click photos to open full view

## 🚀 **Going Live**

When you publish your Framer site, the gallery will work automatically. The embed pulls live data from Flickr, so new photos will appear when you add them to your album!

---

**Need help?** The gallery inherits Framer's fonts and colors automatically, so it should blend seamlessly with your site design.