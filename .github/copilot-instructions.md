# Anton Horodchuk's Personal Portfolio Website

This is a GitHub Pages personal portfolio website built with static HTML and CSS using the Tailwind CSS framework. The site displays Anton Horodchuk's professional skills, experience, and contact information in a modern, professional design.

Always reference these instructions first and fallback to search or bash commands only when you encounter unexpected information that does not match the info here.

## Working Effectively

### Quick Start - Serving the Website Locally
- Serve the website locally: `cd /path/to/repository && python3 -m http.server 8000`
- Takes less than 1 second to start - NEVER CANCEL
- Open browser to: `http://localhost:8000`
- Alternative servers: `npx serve .` (if Node.js available) or any static file server

### No Build Process Required
- This is a pure static HTML/CSS/JS website
- **DO NOT** look for package.json, npm install, or build scripts - they do not exist
- **DO NOT** try to install dependencies - there are none to install
- All files are pre-built and ready to serve directly

### Making Changes
- Edit content directly in `index.html`
- Styling is provided via Tailwind CSS CDN and comprehensive fallback CSS
- All styles are contained within the HTML file for simplicity
- No external CSS or JavaScript files needed

### Testing Changes
- Start local server: `python3 -m http.server 8000`
- Navigate to `http://localhost:8000` in browser
- Verify page loads correctly with modern Tailwind CSS styling
- Check that all sections display: Technical Skills (Programming Languages & Tools), Get In Touch
- Ensure LinkedIn link works and opens in new tab
- Test responsive design by resizing browser window

## Validation

### Manual Validation Requirements
ALWAYS run these validation steps after making any changes:

1. **Serve locally and visually inspect**:
   ```bash
   cd /path/to/repository
   python3 -m http.server 8000
   ```
   - Opens instantly (< 1 second) - NEVER CANCEL
   - Open `http://localhost:8000` in browser

2. **Check page loads correctly**:
   ```bash
   curl -I http://localhost:8000  # Should return 200 OK
   ```

3. **Verify complete page content**:
   - Professional hero section with gradient background and user icon
   - Skills section displays as modern cards: Programming Languages & Tools/Technologies
   - Programming skills show: Perl (5 years), JavaScript (3 years), Java (2 years), Groovy (2 years), Delphi (1 year)
   - Tools section shows: Git, Gradle, SQL, HTML, CSS, Bootstrap, Agile
   - "Get In Touch" section with LinkedIn call-to-action button

4. **Test responsive design**:
   - Resize browser window to test mobile-first responsive layout
   - Content should stack properly on smaller screens (single column on mobile)
   - Hero section, cards, and buttons should adapt seamlessly across screen sizes

### No Linting or Testing Tools
- There are no linting tools configured (eslint, prettier, etc.)
- There are no automated tests
- **DO NOT** add new linting or testing tools unless specifically requested
- Manual validation through browser testing is the primary validation method

## Deployment

### GitHub Pages Auto-Deployment
- This repository uses GitHub Pages for hosting
- **Automatic deployment**: Any push to the main branch automatically deploys to `https://horodchukanton.github.io`
- No manual deployment steps required
- Deployment takes 1-3 minutes after push to GitHub
- Live site URL: `https://horodchukanton.github.io`

### Deployment Validation
After pushing changes:
1. Wait 1-3 minutes for GitHub Pages deployment
2. Visit `https://horodchukanton.github.io`
3. Verify changes appear correctly on live site
4. Test functionality matches local testing results

## Repository Structure

### Complete File Inventory
```
/
├── .git/                          # Git repository metadata
├── .github/
│   └── copilot-instructions.md    # This file
├── .gitignore                     # JetBrains IDE ignores
└── index.html                     # Main website content (contains all HTML, CSS, and styling)
```

### Key Files to Know
- **`index.html`**: Main content file - contains all HTML, Tailwind CSS classes, and fallback styles
- **`.gitignore`**: Configured for JetBrains IDEs - safe to modify if needed

### Legacy Files (No Longer Used)
The following directories may exist from previous Bootstrap implementation but are no longer needed:
- **`css/`**: Previously contained Bootstrap CSS - not used with Tailwind implementation
- **`js/`**: Previously contained Bootstrap JavaScript - not used with Tailwind implementation  
- **`fonts/`**: Previously contained Glyphicons fonts - not used with Tailwind implementation

## External Dependencies

### CDN Resources
The website uses these external CDN resources:
- Tailwind CSS: `https://cdn.tailwindcss.com`
- Google Fonts (Inter): `https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap`

**Important**: The site includes comprehensive fallback CSS that provides the complete design even if external CDN resources are blocked. The fallback styles replicate the entire Tailwind-based layout using vanilla CSS.

### No Package Managers
- **DO NOT** run `npm install` - there is no package.json
- **DO NOT** run `pip install` - there are no Python dependencies
- **DO NOT** look for composer.json, requirements.txt, or similar - they do not exist

## Common Tasks Reference

### Quick Command Reference
```bash
# Serve website locally (choose one):
python3 -m http.server 8000        # Python (recommended)
npx serve .                        # Node.js alternative (if available)

# Test page availability:
curl -I http://localhost:8000       # HTML page should return 200 OK

# View repository status:
git status                         # Check current changes
git log --oneline -5              # View recent commits
```

### Development Workflow
1. Make changes to `index.html`
2. Start local server: `python3 -m http.server 8000`
3. Open `http://localhost:8000` and verify changes
4. Test responsive design by resizing browser
5. Commit and push changes
6. Wait 1-3 minutes for GitHub Pages deployment
7. Verify changes on live site: `https://horodchukanton.github.io`

### Expected Timing
- **Local server startup**: < 1 second - NEVER CANCEL
- **Page load time**: < 1 second locally
- **GitHub Pages deployment**: 1-3 minutes after push
- **Total change-to-live time**: 2-4 minutes

## Troubleshooting

### Common Issues
- **Tailwind styles not applied**: Check that `https://cdn.tailwindcss.com` is accessible; fallback CSS should still provide complete styling
- **Modern design not displaying**: Verify the page content matches the new card-based layout with gradient header
- **Local server not starting**: Ensure Python 3 is installed and port 8000 is available
- **Changes not appearing on GitHub Pages**: Wait 3-5 minutes for deployment, check GitHub Actions

### Emergency Fixes
- **Broken styling**: Revert `index.html` changes: `git checkout HEAD~1 -- index.html`
- **Site completely broken**: Revert to last working commit: `git reset --hard HEAD~1`
- **Server won't start**: Try alternative port: `python3 -m http.server 3000`

## CRITICAL REMINDERS
- **NEVER CANCEL** the local server - it starts in less than 1 second
- **DO NOT** look for build processes that don't exist
- **ALWAYS** test changes locally before pushing  
- **ALWAYS** validate the live GitHub Pages site after deployment
- The site uses Tailwind CSS via CDN with comprehensive fallback styles for reliability