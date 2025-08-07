# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview
This is a Jekyll-based personal blog ("Guan Blog") derived from the Clean Blog Jekyll Theme. It's a bilingual (Chinese/English) blog with Progressive Web App (PWA) features, multilingual support, and modern web capabilities.

## Architecture & Structure

### Core Technologies
- **Jekyll 4.x**: Static site generator with Liquid templating
- **Bootstrap**: Frontend framework for responsive design
- **Grunt**: Build system for LESS compilation and JS minification
- **Service Worker**: PWA functionality for offline access
- **Valine**: Comment system using LeanCloud
- **MathJax**: Mathematical formula rendering
- **Font Awesome**: Icon library

### Key Directories
- `_layouts/`: Jekyll templates (default.html, post.html, page.html, archive.html, keynote.html)
- `_includes/`: Reusable components (nav.html, footer.html, search.html, etc.)
- `_posts/`: Blog posts in Markdown format
- `less/`: LESS source files for styling (guan-blog.less, variables.less, mixins.less)
- `js/`: JavaScript files (bootstrap, jquery, custom blog scripts)
- `css/`: Compiled CSS files (both unminified and minified versions)
- `pwa/`: Progressive Web App manifest and icons

### Build & Development

#### Local Development
```bash
# Install Ruby dependencies
bundle install

# Start development server (localhost:4000)
bundle exec jekyll serve
# OR
npm start

# Development with file watching and auto-rebuild
npm run dev
```

#### Build Process (Grunt)
```bash
# Install Node.js dependencies
npm install

# Run full build (minify JS, compile LESS, add banners)
grunt

# Watch for changes during development
grunt watch
```

#### Windows Setup
1. Install Ruby+Devkit from rubyinstaller.org
2. `gem install bundler`
3. `bundle install`
4. Copy `start.bat.example` to `start.bat`
5. Configure LeanCloud credentials in `start.bat`
6. Run `start.bat` to start with environment variables

### Configuration Files

#### Jekyll Configuration (`_config.yml`)
- Site metadata and SEO settings
- Social media links
- Valine comment system configuration
- Pagination settings (10 posts per page)
- Exclusions for build process
- PWA settings and theme colors

#### Build Configuration
- `Gemfile`: Ruby dependencies (jekyll, jekyll-paginate, webrick)
- `package.json`: Node.js dependencies and scripts
- `Gruntfile.js`: Build tasks for LESS compilation and JS minification

### Key Features

#### Progressive Web App (PWA)
- Service worker (`sw.js`) with offline support
- Manifest file (`pwa/manifest.json`)
- Pre-cached static assets
- Cache-first strategy for static resources

#### Multilingual Support
- Content in both Chinese and English
- Language-specific includes in `_includes/`
- Multilingual selection component

#### Comment System
- Valine integration with LeanCloud backend
- Environment variable configuration for credentials
- Automatic setup via `start.bat` script

#### SEO & Social
- Open Graph meta tags
- Structured data for social sharing
- Google site verification
- Baidu Analytics ready (commented out)

### Environment Variables
Required for Valine comments:
- `LEANCLOUD_APP_ID`: Your LeanCloud application ID
- `LEANCLOUD_APP_KEY`: Your LeanCloud application key

### Deployment
- GitHub Pages compatible (current deployment)
- Static site - no server-side processing required
- CDN-ready with cache-busting for static assets

### Common Tasks
- **Add new post**: Create `.markdown` file in `_posts/` with YAML frontmatter
- **Modify styling**: Edit `.less` files in `less/` directory, then run `grunt`
- **Update navigation**: Edit `_includes/nav.html`
- **Modify footer**: Edit `_includes/footer.html`
- **Add new page**: Create `.html` or `.md` file with appropriate layout
- **Update PWA**: Modify `sw.js` and `pwa/manifest.json`