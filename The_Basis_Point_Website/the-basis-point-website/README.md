# The Basis Point - Setup Instructions

A professional financial intelligence website showcasing daily market briefings.

**Live URL:** `https://premalsprojects.github.io`

---

## 📋 Table of Contents
1. [Setup GitHub Pages](#setup-github-pages)
2. [Adding New Briefings](#adding-new-briefings)
3. [Customizing the Site](#customizing-the-site)
4. [File Structure](#file-structure)

---

## 🚀 Setup GitHub Pages

### Step 1: Create GitHub Repository

1. Go to [GitHub.com](https://github.com) and log in with username **PremalsProjects**
2. Click the **"+"** button (top right) → "New repository"
3. Repository name: **`premalsprojects.github.io`** (must be exactly this!)
4. Description: "Daily market intelligence and financial briefings"
5. Make it **Public**
6. **DO NOT** check "Initialize with README" (we already have files)
7. Click **"Create repository"**

### Step 2: Upload Your Files

**Option A: Via GitHub Website (Easiest)**

1. On your new repository page, click **"uploading an existing file"**
2. Drag and drop ALL these files:
   - `index.html`
   - `archive.html`
   - `about.html`
   - `style.css`
   - `README.md`
3. Create folder: Click "Create new file", type `briefings/.gitkeep`, commit
4. Upload your first briefing to the `briefings` folder
5. Commit changes

**Option B: Via Git Command Line (Advanced)**

```bash
# In your terminal
cd /path/to/basis-point-site
git init
git add .
git commit -m "Initial commit - The Basis Point launch"
git branch -M main
git remote add origin https://github.com/PremalsProjects/premalsprojects.github.io.git
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repository → **Settings**
2. Scroll to **"Pages"** in the left sidebar
3. Under "Source", select **main** branch
4. Keep folder as **/ (root)**
5. Click **Save**
6. Wait 2-3 minutes

### Step 4: Visit Your Live Site!

Your site will be live at: **`https://premalsprojects.github.io`**

---

## 📝 Adding New Briefings (Daily Process)

### Quick Method (2 minutes)

1. **Create your daily briefing** (Word doc format)
2. Name it: `Daily_Finance_Briefing_[DATE].docx`
   - Example: `Daily_Finance_Briefing_Feb17_2026.docx`
3. **Upload to GitHub:**
   - Go to your repository
   - Navigate to `briefings` folder
   - Click "Add file" → "Upload files"
   - Upload your .docx file
   - Commit changes
4. **Update the homepage:**
   - Open `index.html` in GitHub (click the file, then pencil icon to edit)
   - Find the "Latest Briefing" section
   - Update:
     - Date
     - Title
     - Key highlights
     - Download link path
   - Commit changes
5. **Update archive page:**
   - Open `archive.html`
   - Copy the existing briefing card template
   - Add new card at the top with your new briefing info
   - Commit changes

### Detailed Example

**In `index.html`, find this section and update:**

```html
<div class="card-date">
    <span class="date-day">Tuesday</span>  <!-- Change day -->
    <span class="date-full">February 17, 2026</span>  <!-- Change date -->
</div>

<h3 class="card-title">YOUR NEW TITLE HERE</h3>  <!-- Update title -->

<!-- Update download link -->
<a href="briefings/Daily_Finance_Briefing_Feb17_2026.docx" class="btn btn-primary" download>
```

**In `archive.html`, add new card:**

```html
<article class="briefing-card archive-item" data-date="2026-02-17" data-keywords="add relevant keywords">
    <div class="card-date-compact">
        <span class="date-number">17</span>
        <span class="date-month">Feb</span>
    </div>
    <div class="card-content">
        <h3>Your New Briefing Title</h3>
        <div class="card-tags">
            <span class="tag">Tag1</span>
            <span class="tag">Tag2</span>
        </div>
        <p class="card-excerpt">Brief description...</p>
        
        <div class="card-footer-compact">
            <a href="briefings/Daily_Finance_Briefing_Feb17_2026.docx" class="btn btn-sm" download>Download</a>
            <span class="file-meta">DOCX • 12 pages</span>
        </div>
    </div>
</article>
```

---

## 🎨 Customizing the Site

### Change Colors

Open `style.css` and modify the `:root` section:

```css
:root {
    --primary-blue: #1E3A8A;  /* Main brand color */
    --secondary-blue: #3B82F6;  /* Accent color */
    /* Change these hex codes to your preferred colors */
}
```

### Update About Section

1. Open `about.html`
2. Find the "About the Author" section
3. Edit your bio, add links, customize content

### Add Your Photo (Optional)

1. Add your photo to the repository (e.g., `author.jpg`)
2. In `about.html`, add to the author section:
```html
<img src="author.jpg" alt="Your Name" style="width: 150px; border-radius: 50%;">
```

---

## 📁 File Structure

```
premalsprojects.github.io/
├── index.html              # Homepage
├── archive.html            # All briefings archive
├── about.html              # About page
├── style.css               # All styling
├── README.md               # This file
└── briefings/              # Folder for all .docx files
    ├── Daily_Finance_Briefing_Feb16_2026.docx
    ├── Daily_Finance_Briefing_Feb17_2026.docx
    └── ...
```

---

## 🔧 Troubleshooting

### Site not showing after 10 minutes?
- Check Settings → Pages → make sure "main" branch is selected
- Make sure repository name is exactly `premalsprojects.github.io`

### Download links not working?
- Make sure briefing files are in the `briefings/` folder
- Check file names match exactly (case-sensitive)
- Path should be: `briefings/filename.docx`

### Styling looks broken?
- Make sure `style.css` is in the root directory (same level as index.html)
- Check browser console for errors (F12)

### Want to add custom domain later?
- Buy domain (e.g., `thebasispoint.com`)
- In GitHub Settings → Pages → Custom domain
- Follow GitHub's instructions to configure DNS

---

## 💡 Tips for Success

1. **Consistency:** Upload briefings at the same time each day
2. **SEO:** Use descriptive titles and keywords in your briefings
3. **Social:** Share your briefings on LinkedIn with the URL
4. **Backups:** Keep local copies of all briefings
5. **Analytics:** Add Google Analytics to track visitors (optional)

---

## 📞 Need Help?

- **GitHub Pages Docs:** https://docs.github.com/en/pages
- **Git Basics:** https://git-scm.com/doc
- **HTML/CSS Help:** https://developer.mozilla.org/

---

## 📈 Next Steps (Optional Upgrades)

After your site is live and you're comfortable:

1. **Add email signup** (using Mailchimp embed)
2. **Custom domain** ($12/year for `.com`)
3. **RSS feed** for automatic updates
4. **Google Analytics** to track visitors
5. **SEO optimization** for search engines

---

**Built with ❤️ by PremalsProjects**

Good luck with your daily briefings! 🚀
