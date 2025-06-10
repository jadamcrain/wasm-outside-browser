# Marp Presentation Template

This repository contains a Marp presentation template for creating slide presentations using Markdown.

## Installation (Ubuntu)

### Install Node.js and npm
```bash
# Update package list
sudo apt update

# Install Node.js and npm
sudo apt install nodejs npm

# Verify installation
node --version
npm --version
```

### Install Marp CLI
```bash
# Install Marp CLI globally
npm install -g @marp-team/marp-cli

# Verify installation
marp --version
```

### Install Puppeteer dependencies (for PDF export)
```bash
# Install Chromium and required dependencies
sudo apt install chromium-browser

# Or install required libraries for Puppeteer
sudo apt install libnss3 libatk-bridge2.0-0 libdrm2 libxcomposite1 libxdamage1 libxrandr2 libgbm1 libxss1 libasound2
```

## Building the Presentation

### Build to HTML
```bash
# Build single HTML file
marp presentation.md -o presentation.html

# Build with custom theme
marp presentation.md --theme path/to/theme.css -o presentation.html

# Serve locally for development
marp presentation.md --server
```

### Build to PDF
```bash
# Build PDF
marp presentation.md --pdf -o presentation.pdf

# Build PDF with custom page size
marp presentation.md --pdf --pdf-notes -o presentation.pdf
```

### Build Multiple Formats
```bash
# Build both HTML and PDF
marp presentation.md -o presentation.html --pdf
```

## Usage

1. Edit `presentation.md` with your content
2. Use `---` to separate slides
3. Add Marp directives in the frontmatter (between `---` at the top)
4. Run build commands to generate your presentation

## Marp Syntax Highlights

- `<!-- _class: lead -->` - Center content on slide
- `![bg right:40%](image.jpg)` - Background image positioning
- `marp: true` - Enable Marp processing
- `theme: default` - Set presentation theme
- `paginate: true` - Add page numbers

For more information, visit the [Marp documentation](https://marp.app/).
