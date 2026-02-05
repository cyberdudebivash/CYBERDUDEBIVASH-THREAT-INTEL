# 📱 BLOGGER INTEGRATION GUIDE

**CYBERDUDEBIVASH® THREAT-INTEL LIVE FEED for Blogger**

© 2026 CyberDudeBivash Pvt Ltd

---

## 🎯 EMBED WIDGET IN BLOGGER SIDEBAR

### Step 1: Get Your GitHub Pages URL

After deploying to GitHub Pages, your URLs will be:

```
Dashboard: https://YOUR_USERNAME.github.io/threat-intel/frontend/dashboard/
Widget CSS: https://YOUR_USERNAME.github.io/threat-intel/frontend/assets/css/widget.css
Widget JS: https://YOUR_USERNAME.github.io/threat-intel/frontend/assets/js/widget.js
```

Replace `YOUR_USERNAME` with your actual GitHub username.

---

### Step 2: Add Widget to Blogger

1. **Go to Blogger Dashboard**
2. **Layout → Add a Gadget**
3. **Choose "HTML/JavaScript"**
4. **Title:** `🛡️ THREAT-INTEL LIVE`
5. **Content:** Paste this code:

```html
<!-- CYBERDUDEBIVASH THREAT-INTEL Widget -->
<link rel="stylesheet" href="https://YOUR_USERNAME.github.io/threat-intel/frontend/assets/css/widget.css">
<div id="cyberdudebivash-threat-widget"></div>
<script src="https://YOUR_USERNAME.github.io/threat-intel/frontend/assets/js/widget.js"></script>

<!-- Copyright Notice (Required) -->
<style>
.cdb-copyright-notice {
    font-size: 10px;
    color: #8b92a8;
    text-align: center;
    margin-top: 8px;
    padding: 8px;
    background: #0a0e27;
    border-radius: 6px;
}
</style>
<div class="cdb-copyright-notice">
Powered by <a href="https://www.cyberdudebivash.com" style="color: #00ff88;" target="_blank">CyberDudeBivash®</a>
</div>
```

6. **Save**

---

### Step 3: Verify

1. Visit your blog
2. Widget should appear in sidebar
3. Shows live threat feed
4. Auto-updates every 5 minutes

---

## 🎨 CUSTOMIZATION OPTIONS

### Option 1: Adjust Widget Width

Add this before the widget code:

```html
<style>
#cyberdudebivash-threat-widget {
    max-width: 100% !important; /* Full sidebar width */
}
</style>
```

### Option 2: Change Max Height

Add this CSS:

```html
<style>
.cdb-widget-threats {
    max-height: 300px !important; /* Shorter widget */
}
</style>
```

### Option 3: Hide Copyright (NOT RECOMMENDED)

**Warning:** Removing copyright violates license terms.

If you have commercial license, you can add:

```html
<style>
.cdb-copyright { display: none; }
</style>
```

---

## 📄 EMBED FULL DASHBOARD AS PAGE

### Method 1: iFrame (Easiest)

1. **Create New Page** in Blogger
2. **HTML View**
3. **Paste:**

```html
<iframe 
    src="https://YOUR_USERNAME.github.io/threat-intel/frontend/dashboard/" 
    width="100%" 
    height="1200px" 
    frameborder="0"
    style="border: 2px solid #00ff88; border-radius: 12px;">
</iframe>
```

### Method 2: Direct HTML (Advanced)

1. **Create New Page**
2. **Paste entire `frontend/dashboard/index.html` content**
3. **Update CSS/JS paths** to absolute URLs

---

## 🔗 MULTIPLE BLOGS SETUP

If you have multiple Blogger blogs:

### Blog 1 (cyberdudebivash-news.blogspot.com)
```html
<link rel="stylesheet" href="https://YOUR_USERNAME.github.io/threat-intel/frontend/assets/css/widget.css">
<div id="cyberdudebivash-threat-widget"></div>
<script src="https://YOUR_USERNAME.github.io/threat-intel/frontend/assets/js/widget.js"></script>
```

### Blog 2 (cyberbivash.blogspot.com)
```html
<!-- Same code works everywhere! -->
<link rel="stylesheet" href="https://YOUR_USERNAME.github.io/threat-intel/frontend/assets/css/widget.css">
<div id="cyberdudebivash-threat-widget"></div>
<script src="https://YOUR_USERNAME.github.io/threat-intel/frontend/assets/js/widget.js"></script>
```

### Blog 3 (cryptobivash.code.blog)
```html
<!-- WordPress also supported -->
<link rel="stylesheet" href="https://YOUR_USERNAME.github.io/threat-intel/frontend/assets/css/widget.css">
<div id="cyberdudebivash-threat-widget"></div>
<script src="https://YOUR_USERNAME.github.io/threat-intel/frontend/assets/js/widget.js"></script>
```

**Same widget, multiple blogs!** 🔥

---

## ⚡ ADVANCED: CUSTOM POSITIONING

### Sticky Sidebar Widget

```html
<style>
#cyberdudebivash-threat-widget {
    position: sticky;
    top: 20px;
    z-index: 100;
}
</style>
```

### Floating Bottom-Right

```html
<style>
#cyberdudebivash-threat-widget {
    position: fixed;
    bottom: 20px;
    right: 20px;
    max-width: 350px;
    z-index: 9999;
    box-shadow: 0 10px 40px rgba(0, 255, 136, 0.4);
}
</style>
```

---

## 🐛 COMMON ISSUES

### Widget not loading?

**Check:**
1. ✅ Correct GitHub username in URLs
2. ✅ GitHub Pages enabled
3. ✅ Files deployed properly
4. ✅ No typos in embed code

### Styling broken?

**Check:**
1. ✅ CSS file URL is correct
2. ✅ HTTPS (not HTTP)
3. ✅ No conflicting Blogger theme CSS

### Not auto-updating?

**Check:**
1. ✅ GitHub Actions running (see workflow logs)
2. ✅ Backend generating new data
3. ✅ Browser cache cleared

---

## 📊 PERFORMANCE

**Widget Load Time:** <500ms  
**Page Impact:** Minimal (<50KB total)  
**Auto-Refresh:** Every 5 minutes  
**Browser Support:** All modern browsers  

---

## 🔒 SECURITY

✅ No tracking scripts  
✅ No cookies  
✅ No user data collection  
✅ Pure client-side JavaScript  
✅ Served via HTTPS  

---

## 📞 SUPPORT

**Issues with Blogger integration?**

Email: iambivash@cyberdudebivash.com  
Subject: "Threat-Intel Blogger Integration Help"

Include:
- Blog URL
- Screenshot of issue
- Browser console errors

---

## ✅ CHECKLIST

Before going live:

- [ ] GitHub Pages enabled
- [ ] Backend generating data (check Actions)
- [ ] Widget URLs updated with your username
- [ ] Tested on desktop
- [ ] Tested on mobile
- [ ] Copyright notice present
- [ ] Dashboard accessible

---

**© 2026 CyberDudeBivash Pvt Ltd**  
**All Rights Reserved**

**Happy Deploying! 🚀**
