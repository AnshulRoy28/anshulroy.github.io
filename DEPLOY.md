# Deploy to GitHub Pages

## Quick Setup

1. **Create a new GitHub repository**
   ```bash
   # In your terminal
   git init
   git add index.html guideline.json README.md
   git commit -m "Initial portfolio commit"
   ```

2. **Push to GitHub**
   ```bash
   # Replace YOUR_USERNAME with your GitHub username
   git remote add origin https://github.com/YOUR_USERNAME/portfolio.git
   git branch -M main
   git push -u origin main
   ```

3. **Enable GitHub Pages**
   - Go to your repository on GitHub
   - Click **Settings** → **Pages**
   - Under "Source", select **main** branch
   - Click **Save**
   - Your site will be live at: `https://YOUR_USERNAME.github.io/portfolio/`

## Files to Deploy

Only these files are needed for GitHub Pages:
- ✅ `index.html` (your main portfolio file)
- ✅ `README.md` (optional, for repo description)
- ✅ `guideline.json` (optional, for reference)

You DON'T need:
- ❌ `sections/` folder (content is already in index.html)
- ❌ `styles.css` (styles are inline in index.html)
- ❌ `script.js` (JavaScript is inline in index.html)
- ❌ `portfolio.html` (duplicate file)

## Custom Domain (Optional)

If you want to use a custom domain like `anshulroy.com`:

1. Buy a domain from Namecheap, GoDaddy, etc.
2. Add a `CNAME` file to your repo with your domain:
   ```
   anshulroy.com
   ```
3. Configure DNS settings at your domain provider:
   - Add A records pointing to GitHub's IPs:
     - `185.199.108.153`
     - `185.199.109.153`
     - `185.199.110.153`
     - `185.199.111.153`
   - Or add a CNAME record: `YOUR_USERNAME.github.io`

## Testing Locally

To test the horizontal scroll functionality locally, you need a local server:

**Option 1: Python**
```bash
python -m http.server 8000
# Visit: http://localhost:8000
```

**Option 2: Node.js**
```bash
npx serve
# Visit: http://localhost:3000
```

**Option 3: VS Code**
- Install "Live Server" extension
- Right-click `index.html` → "Open with Live Server"

## Troubleshooting

**Horizontal scroll not working?**
- Make sure JavaScript is enabled in your browser
- Check browser console for errors (F12)
- The scroll works with:
  - Mouse wheel (scroll horizontally with vertical wheel)
  - Click and drag
  - Touch gestures on mobile

**Page not updating on GitHub Pages?**
- Wait 1-2 minutes for changes to deploy
- Hard refresh: Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac)
- Clear browser cache

## Next Steps

After deployment:
1. Update your GitHub profile README with the portfolio link
2. Add the link to your LinkedIn profile
3. Share it in your resume
4. Update the "Download Resume" link in the portfolio

---

Need help? Check the [GitHub Pages documentation](https://docs.github.com/en/pages)
