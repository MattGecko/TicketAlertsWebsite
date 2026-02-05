# Football Ticket Alerts - Marketing Website

Clean, bold marketing website for the Football Ticket Alerts iOS app. Black and yellow brand colors matching the app design.

## 🎨 Design

- **Colors**: Black background (#000000) with yellow accents (#FFD700)
- **Typography**: System fonts for native feel
- **Style**: Bold, minimal, conversion-optimized

## 📄 Pages

1. **index.html** - Main landing page
   - Hero section with CTA
   - Supported clubs
   - Features showcase
   - Pricing
   - FAQ
   - Download section

2. **privacy.html** - Privacy Policy
   - GDPR compliant
   - CCPA compliant
   - Covers Firebase, OpenAI, Apple services

3. **terms.html** - Terms of Service
   - Subscription terms
   - Service limitations
   - Liability disclaimers
   - Refund policy

4. **contact.html** - Contact Form
   - Email form (requires backend setup)
   - Support categories
   - Response time info

## 🚀 Deployment

### Option 1: Netlify (Recommended - Free)

1. Create account at [netlify.com](https://netlify.com)
2. Drag and drop the `TicketAlertsWebsite` folder
3. Done! You'll get a free `.netlify.app` domain
4. (Optional) Add custom domain in settings

### Option 2: GitHub Pages (Free)

```bash
cd /Users/mattcowlin/Documents/GitHub/TicketAlertsWebsite
git init
git add .
git commit -m "Initial website"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/ticketalerts-website.git
git push -u origin main
```

Then enable GitHub Pages in repository settings.

### Option 3: Vercel (Free)

1. Create account at [vercel.com](https://vercel.com)
2. Import from git or drag/drop folder
3. Deploy automatically

## 📝 Setup Required

### 1. Update Contact Form

The contact form uses Formspree (free tier available). To set it up:

1. Go to [formspree.io](https://formspree.io)
2. Create free account
3. Create new form
4. Replace `YOUR_FORM_ID` in `contact.html` line 81:

```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

### 2. Update App Store Link

Once your app is live on the App Store, update the download link in `index.html` (line 135):

```html
<a href="https://apps.apple.com/YOUR_APP_URL" class="btn btn-primary btn-large">
```

### 3. Add Contact Email

Update contact email in:
- `contact.html` line 120
- `privacy.html` section 9
- `terms.html` section 17

### 4. Add Analytics (Optional)

Add Google Analytics or Plausible tracking code before `</head>` in all HTML files.

## 🔗 Important Links to Update in iOS App

Once deployed, update your app's `PaywallView.swift` with the website URLs:

```swift
// Line 164 (Privacy button)
Button("Privacy") {
    if let url = URL(string: "https://yourwebsite.com/privacy.html") {
        UIApplication.shared.open(url)
    }
}

// Line 174 (Terms button)
Button("Terms") {
    if let url = URL(string: "https://yourwebsite.com/terms.html") {
        UIApplication.shared.open(url)
    }
}
```

## 📱 App Store Connect

Add these URLs in App Store Connect:

- **Privacy Policy URL**: `https://yourwebsite.com/privacy.html`
- **Terms of Service URL**: `https://yourwebsite.com/terms.html`
- **Marketing URL**: `https://yourwebsite.com`
- **Support URL**: `https://yourwebsite.com/contact.html`

## 🎯 SEO Optimization (Optional)

Add to `<head>` of `index.html`:

```html
<meta property="og:title" content="Football Ticket Alerts">
<meta property="og:description" content="Never miss a ticket release again">
<meta property="og:image" content="https://yourwebsite.com/og-image.jpg">
<meta name="twitter:card" content="summary_large_image">
```

## 📊 Features

- ✅ Fully responsive (mobile, tablet, desktop)
- ✅ Fast loading (no dependencies)
- ✅ SEO optimized
- ✅ GDPR/CCPA compliant legal pages
- ✅ Contact form ready
- ✅ Black and yellow brand colors
- ✅ Clean, conversion-optimized design

## 🛠 Customization

### Change Colors

Edit `styles.css`:

```css
/* Yellow accent */
#FFD700 -> Your color

/* Black background */
#000000 -> Your color
```

### Add More Clubs

Edit `index.html` teams section:

```html
<div class="team-card">🔴 New Team</div>
```

### Update Pricing

Edit pricing section in `index.html` and `terms.html`

## 📝 Notes

- No frameworks or build tools required
- Pure HTML/CSS/minimal JavaScript
- Can be edited with any text editor
- Deploys anywhere that serves static files
- Free to host on Netlify, Vercel, or GitHub Pages

## 🚨 Before Launch

- [ ] Set up contact form with Formspree
- [ ] Add App Store link
- [ ] Add contact email addresses
- [ ] Deploy to hosting service
- [ ] Update iOS app with website URLs
- [ ] Add URLs to App Store Connect
- [ ] Test all forms and links
- [ ] Test on mobile devices

## 📄 License

This website is part of the Football Ticket Alerts project.
