# WebAssembly Outside the Browser

This presentation explores WebAssembly's potential beyond web browsers, covering WIT/WASI interfaces, cloud computing applications, plugin systems, and a real-world industrial automation case study using WASM as a soft-PLC platform.

## Prerequisites

This presentation is built using [Marp](https://marp.app/), a Markdown presentation ecosystem. You'll need:

- **Node.js** (16+ recommended)
- **npm** or **yarn**
- **Chromium/Chrome** (for PDF export)

### Quick Setup (Ubuntu/Debian)
```bash
# Install Node.js and npm
sudo apt update && sudo apt install nodejs npm

# Install Marp CLI
npm install -g @marp-team/marp-cli

# Install Chromium (for PDF export)
sudo apt install chromium-browser
```

### Quick Setup (macOS)
```bash
# Using Homebrew
brew install node
npm install -g @marp-team/marp-cli
```

### Quick Setup (Windows)
```bash
# Using Chocolatey
choco install nodejs
npm install -g @marp-team/marp-cli
```

## Building the Presentation

### Generate HTML (for web viewing)
```bash
marp presentation.md -o presentation.html
```

### Generate PDF (for sharing/printing)
```bash
marp presentation.md --pdf -o presentation.pdf
```

### Development Mode (live preview)
```bash
marp --server .
# Open http://localhost:8080 in your browser
```

## Content Overview

The presentation covers:

1. **WebAssembly Fundamentals** - What WASM is and why it matters
2. **WIT & WASI** - Interface types and system APIs
3. **Cloud Computing** - WASM vs containers comparison
4. **Plugin Systems** - Building safe, sandboxed applications
5. **Industrial Case Study** - Soft-PLC implementation using WASM

## Customization

- **Edit content**: Modify `presentation.md`
- **Add images**: Place in `./static/` directory
- **Styling**: Presentation uses default Marp theme with custom CSS
- **Slides**: Separated by `---` markers

