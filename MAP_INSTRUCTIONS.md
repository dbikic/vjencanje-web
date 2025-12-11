# How to Add a Google Maps Embed

## Step-by-Step Instructions:

### Method 1: Using Google Maps Website (Easiest)

1. **Open Google Maps** in your browser
   - Go to [maps.google.com](https://maps.google.com)

2. **Search for your venue**
   - Type the address or name of your wedding venue in the search box
   - Press Enter

3. **Get the embed code**
   - Click on the **"Share"** button (usually on the left sidebar or in the info panel)
   - Click on the **"Embed a map"** tab
   - Choose your map size (Small, Medium, Large, or Custom)
   - Copy the **iframe code** that appears

4. **Add it to your website**
   - Open `index.html` in a text editor
   - Find the location section (around line 668)
   - Look for the `<iframe>` tag inside `<div class="location-map">`
   - Replace the `src` attribute with the `src` from your copied iframe code

### Example:
```html
<iframe 
    src="YOUR_COPIED_SRC_URL_HERE"
    allowfullscreen="" 
    loading="lazy" 
    referrerpolicy="no-referrer-when-downgrade">
</iframe>
```

### Method 2: Direct Embed URL Format

If you have the coordinates or address, you can use this format:

```
https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d[LATITUDE]!2d[LONGITUDE]!3d[ZOOM]!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2z[COORDINATES]!5e0!3m2!1sen!2sus!4v[TIMESTAMP]!5m2!1sen!2sus
```

### Alternative: Use a Static Map Image

If you prefer a static image instead of an interactive map:

1. Go to [Google Maps Static API](https://developers.google.com/maps/documentation/maps-static/overview)
2. Or use this simple URL format:
   ```
   https://maps.googleapis.com/maps/api/staticmap?center=[LATITUDE],[LONGITUDE]&zoom=15&size=600x400&markers=color:red%7C[LATITUDE],[LONGITUDE]
   ```

### Tips:
- **Test the map** after adding it to make sure it displays correctly
- The map will be **responsive** and work on mobile devices
- You can **customize the zoom level** in the embed URL
- Make sure the venue address in your location info matches the map location

### Need Help?
If you're having trouble, you can also:
- Use a different map service (like OpenStreetMap)
- Add a link to Google Maps instead of embedding
- Use a custom map image

