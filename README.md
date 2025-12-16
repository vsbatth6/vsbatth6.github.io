# Personal CV Website

A clean, one-page static website for your CV/resume, hosted free on GitHub Pages.

## 📁 File Structure

```
your-repo/
├── index.md              # Your CV content (edit this!)
├── _config.yml           # Jekyll configuration
├── _layouts/
│   └── default.html      # HTML template
├── assets/
│   └── css/
│       └── style.css     # Custom styles (edit this for styling!)
└── README.md             # This file
```

## 🚀 How to Host on GitHub Pages

### Step 1: Create a GitHub Repository

1. Go to [github.com](https://github.com) and sign in (or create an account)
1. Click the **+** icon in the top right → **New repository**
1. Name it `your-username.github.io` for a personal site, or any name for a project site
1. Keep it **Public**
1. Click **Create repository**

### Step 2: Upload Your Files

**Option A: Using GitHub Web Interface (Easiest)**

1. In your new repo, click **Add file** → **Upload files**
1. Drag and drop all the files from this folder
1. Click **Commit changes**

**Option B: Using Git Command Line**

```bash
# Navigate to the folder with these files
cd path/to/your/cv-files

# Initialize git and push
git init
git add .
git commit -m "Initial CV website"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
1. Click **Settings** → **Pages** (in the left sidebar)
1. Under "Source", select **Deploy from a branch**
1. Select **main** branch and **/ (root)** folder
1. Click **Save**

### Step 4: Access Your Site

Your site will be live at:

- `https://your-username.github.io` (if repo is named `your-username.github.io`)
- `https://your-username.github.io/repo-name` (for other repo names)

It may take 1-2 minutes for the first deployment.

-----

## 🎨 How to Customize Styling

Edit `assets/css/style.css` to change the appearance. The file is well-commented with sections for:

### Quick Color Changes

Find the `:root` section at the top and change the color variables:

```css
:root {
  --primary-color: #1a365d;      /* Change this for headers/accents */
  --secondary-color: #2d3748;    /* Change this for subheaders */
  --accent-color: #3182ce;       /* Change this for links */
  --background: #ffffff;         /* Change this for page background */
}
```

### Popular Color Schemes

**Ocean Blue (Default)**

```css
--primary-color: #1a365d;
--accent-color: #3182ce;
```

**Forest Green**

```css
--primary-color: #1a4731;
--accent-color: #38a169;
```

**Elegant Purple**

```css
--primary-color: #44337a;
--accent-color: #805ad5;
```

**Warm Coral**

```css
--primary-color: #c53030;
--accent-color: #e53e3e;
```

**Minimalist Gray**

```css
--primary-color: #1a202c;
--accent-color: #4a5568;
```

### Enable Dark Mode

Uncomment the dark mode section at the bottom of `style.css` to automatically switch to dark theme for users who prefer it.

### Change Fonts

In `_layouts/default.html`, change the Google Fonts link, then update `style.css`:

```css
body {
  font-family: 'Your Font Name', sans-serif;
}
```

-----

## ✏️ How to Edit Your CV Content

Edit `index.md` using Markdown syntax:

- `# Heading 1` for your name
- `## Heading 2` for section titles
- `### Heading 3` for job titles
- `**bold text**` for emphasis
- `- item` for bullet points
- `[link text](url)` for links
- `| col1 | col2 |` for tables

-----

## 🔄 Updating Your Site

After making changes:

**GitHub Web:**

1. Navigate to the file you want to edit
1. Click the pencil icon to edit
1. Make your changes
1. Click **Commit changes**

**Git Command Line:**

```bash
git add .
git commit -m "Updated CV"
git push
```

Changes typically appear within 1-2 minutes.

-----

## 📱 Features

- ✅ Mobile responsive
- ✅ Print-friendly (Ctrl/Cmd + P)
- ✅ SEO optimized
- ✅ Fast loading
- ✅ Dark mode ready (optional)
- ✅ Free hosting on GitHub Pages

-----

## 🆘 Troubleshooting

**Site not showing up?**

- Check that GitHub Pages is enabled in Settings → Pages
- Wait 2-3 minutes for initial deployment
- Ensure `index.md` exists in the root directory

**Styling not applying?**

- Check file paths are correct
- Clear browser cache (Ctrl/Cmd + Shift + R)
- Verify `_layouts/default.html` references the CSS correctly

**Build errors?**

- Check `_config.yml` for YAML syntax errors
- Ensure no special characters in file names
- Look at the Actions tab for detailed build logs

**Changes not showing up?**

- Wait 1-2 minutes for GitHub Pages to rebuild
- Hard refresh your browser (Ctrl/Cmd + Shift + R)
- Check the Actions tab to ensure build completed successfully

-----

## 📄 License

This project is open source and available for personal use.

-----

## 💡 Additional Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Markdown Guide](https://www.markdownguide.org/)
- [Google Fonts](https://fonts.google.com/)

-----

Built with ❤️ using Jekyll and GitHub Pages
