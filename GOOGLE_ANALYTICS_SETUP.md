# Google Analytics Setup Guide for Your Portfolio

## Overview

Your portfolio website now has **Google Analytics** integrated! This will track:
- Total visitors
- Page views
- Time spent on site
- Click-through rates on projects
- Device/browser information
- Geographic location of visitors
- And much more!

## How to Set Up Google Analytics

### Step 1: Create a Google Analytics Account

1. Go to [analytics.google.com](https://analytics.google.com)
2. Click **Start Measuring** or **Sign In** if you have a Google account
3. Create a Google account if you don't have one

### Step 2: Create a New Property

1. Click **Create** or **New Property**
2. Fill in the details:
   - **Property Name:** `Yuqi Lin Portfolio` (or similar)
   - **Timezone:** Select your timezone (or UTC)
   - **Currency:** USD (or your preference)
3. Click **Next**

### Step 3: Create a Data Stream

1. Select **Web** as your platform
2. Enter your website details:
   - **Website URL:** `https://linyu-qi.github.io`
   - **Stream Name:** `Portfolio Website`
3. Click **Create Stream**

### Step 4: Get Your Measurement ID

After creating the stream, you'll see a screen with:
- **Measurement ID:** This looks like `G-XXXXXXXXXX`
- Copy this ID

### Step 5: Update Your Portfolio HTML

1. Open your `index.html` file
2. Find this section at the top (after `<title>`):

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

3. **Replace `G-XXXXXXXXXX` with your actual Measurement ID** (from Step 4)
4. Save the file
5. Upload to GitHub

### Step 6: Verify It Works

1. Wait 1-2 minutes after uploading
2. Visit your website: `https://linyu-qi.github.io`
3. Go back to Google Analytics
4. Check the **Real-time** section (usually on the left sidebar)
5. You should see your visit appear!

---

## What You'll See in Google Analytics

### Real-time Dashboard
Shows visitors currently on your site, pages they're viewing, and their locations.

### Key Reports
- **Users:** Total unique visitors
- **Sessions:** Number of visits
- **Bounce Rate:** % of visitors who leave without interaction
- **Average Session Duration:** How long visitors stay
- **Top Pages:** Which sections are most visited
- **Traffic Sources:** Where visitors come from (direct, search, social, etc.)

### Custom Events
We can also track:
- Downloads of your CV
- Clicks on project links
- Clicks on social media links (LinkedIn, GitHub, etc.)

---

## Visitor Counter on Your Site

Your portfolio also displays a simple **visitor counter** at the bottom of the page showing how many times the page has been visited in the browser.

**Note:** This counter uses browser storage and resets if the user clears their cache. Google Analytics provides more accurate tracking.

---

## Email Reports (Optional)

1. In Google Analytics, go to **Admin** → **Data Streams**
2. Click your stream
3. Enable **Email reports**
4. Google will send you weekly/monthly summaries of your traffic

---

## Troubleshooting

**Issue:** Real-time data not showing

- **Solution:** It can take 1-2 minutes for data to appear. Also make sure:
  - Correct Measurement ID is in your HTML
  - File was uploaded to GitHub
  - You're visiting the published URL (not localhost)

**Issue:** Seeing your own visits

- **Solution:** Create a filter in Google Analytics to exclude your IP address from reports

---

## Next Steps

- Monitor your analytics weekly
- Track which projects get the most clicks
- See where your visitors come from
- Optimize your portfolio based on visitor behavior

---

**Questions?** The official Google Analytics help center: [support.google.com/analytics](https://support.google.com/analytics)
