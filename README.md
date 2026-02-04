# Data Visualization Portfolio

A professional portfolio website showcasing data visualization and quantitative analysis skills, built with Quarto.

## 📁 Project Structure

```
portfolio/
├── _quarto.yml          # Quarto configuration
├── styles.css           # Custom CSS styling
├── index.qmd            # Homepage
├── about.qmd            # About page
├── images/              # Visualization images
│   ├── Pic1.png
│   ├── Pic2.png
│   ├── Pic3.png
│   └── Pic4.png
├── viz-*.qmd            # Static visualization pages
├── app-*.qmd            # Interactive dashboard pages
└── docs/                # Generated website (after render)
```

## 🚀 Quick Start

### Prerequisites

1. **Install Quarto**: Download from [quarto.org](https://quarto.org/docs/get-started/)
2. **R** (for any embedded R code)

### Build the Website

```bash
cd portfolio
quarto render
```

This generates the website in the `docs/` folder.

### Preview Locally

```bash
quarto preview
```

Opens a live preview at `http://localhost:4000`

## 🌐 Deployment Options

### Option 1: GitHub Pages (Recommended - Free)

1. Create a GitHub repository
2. Push the `portfolio` folder
3. Go to Settings → Pages → Source: "Deploy from a branch"
4. Select `main` branch and `/docs` folder
5. Your site will be live at `https://yourusername.github.io/repo-name`

### Option 2: Netlify (Free)

1. Connect your GitHub repo to Netlify
2. Set build command: `quarto render`
3. Set publish directory: `docs`

### Option 3: Quarto Pub (Free)

```bash
quarto publish quarto-pub
```

### Option 4: Custom Domain

Add a `CNAME` file in the `docs` folder with your domain.

## 🎨 Customization

### Update Personal Info

Edit these files to add your details:
- `about.qmd` - Your bio, education, experience
- `_quarto.yml` - Update GitHub/LinkedIn links
- `index.qmd` - Update contact email

### Add New Visualizations

1. Add image to `images/` folder
2. Create new `viz-*.qmd` file
3. Add to navigation in `_quarto.yml`

### Change Theme

Edit `_quarto.yml`:
```yaml
format:
  html:
    theme: 
      light: cosmo  # Try: flatly, lumen, sandstone, etc.
```

## 📊 Shiny App Deployment

The interactive dashboards (Shiny apps) need separate hosting:

### ShinyApps.io (Free tier available)

```r
# Install rsconnect
install.packages("rsconnect")

# Configure your account
rsconnect::setAccountInfo(
  name = "your-account",
  token = "your-token",
  secret = "your-secret"
)

# Deploy the app
rsconnect::deployApp("path/to/app.R")
```

Then update the portfolio pages with the live app URLs.

### Embed Shiny Apps

Once deployed, you can embed them in the Quarto pages:

```html
<iframe src="https://your-account.shinyapps.io/app-name/" 
        class="shiny-embed"></iframe>
```

## 📝 License

© 2026 Teodor Nikolaev Nikolov
# Personal-Website-Data-Visualization-Portfolio
