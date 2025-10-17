# Academic Portfolio Website

A personal academic portfolio website built with SvelteKit, featuring a clean design with dark mode support and serif typography.

## Prerequisites

### Install Node.js and npm

**macOS (using Homebrew):**
```bash
# Install Homebrew if you don't have it
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Install Node.js (includes npm)
brew install node
```

**Windows:**
1. Download the installer from [nodejs.org](https://nodejs.org/)
2. Run the installer and follow the prompts
3. npm is included with Node.js

**Linux (Ubuntu/Debian):**
```bash
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
sudo apt-get install -y nodejs
```

Verify installation:
```bash
node --version
npm --version
```

### Install pnpm (Package Manager)

```bash
npm install -g pnpm
```

## Getting Started

1. **Clone the repository:**
   ```bash
   git clone <your-repo-url>
   cd website_temp
   ```

2. **Install dependencies:**
   ```bash
   pnpm install
   ```

3. **Start the development server:**
   ```bash
   pnpm run dev
   ```

4. **Open your browser:**
   Navigate to `http://localhost:5173`

## Build for Production

```bash
# Create a production build
pnpm run build

# Preview the production build locally
pnpm run preview
```

## Project Structure

```
website_temp/
├── src/
│   ├── lib/
│   │   ├── assets/          # Images and static assets
│   │   └── components/      # Svelte components
│   ├── routes/              # SvelteKit routes
│   │   ├── +page.svelte     # Main page
│   │   └── +layout.svelte   # Global layout and styles
│   └── app.html             # HTML template
├── static/                  # Static files (CV, etc.)
└── package.json
```

## Features

- **Dark Mode**: Toggle between light and dark themes
- **Responsive Design**: Mobile-friendly navigation
- **Typography**: Crimson Text (serif) for body, Inter (sans-serif) for headings
- **Sections**: About, Research, Experience, Publications, Presentations

## Customization

### Update Content
- Edit components in `src/lib/components/`
- Update personal info in `Hero.svelte`
- Add research, publications, etc. in respective component files

### Update Styles
- Global styles in `src/routes/+layout.svelte`
- Component-specific styles in each `.svelte` file

### Add CV
- Place your CV as `cv.pdf` in the `static/` folder

## Troubleshooting

**Port already in use:**
```bash
pnpm run dev -- --port 3000
```

**Clear cache and reinstall:**
```bash
rm -rf node_modules pnpm-lock.yaml
pnpm install
```
