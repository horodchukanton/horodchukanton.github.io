# Anton Horodchuk's Personal Portfolio Website

This is a GitHub Pages personal portfolio website built with static HTML, CSS, and JavaScript using the Bootstrap framework. The site displays Anton Horodchuk's professional skills, experience, and contact information.

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
- CSS framework is provided via `css/bootstrap.min.css` (Bootstrap 3.x)
- JavaScript is provided via `js/bootstrap.min.js`
- Font files are in the `fonts/` directory (Glyphicons)

### Testing Changes
- Start local server: `python3 -m http.server 8000`
- Navigate to `http://localhost:8000` in browser
- Verify page loads correctly with Bootstrap styling
- Check that all sections display: Skills, Additional, My Contacts
- Ensure LinkedIn link works and opens in new tab

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

2. **Check all assets load correctly**:
   ```bash
   curl -I http://localhost:8000/css/bootstrap.min.css  # Should return 200 OK
   curl -I http://localhost:8000/js/bootstrap.min.js    # Should return 200 OK
   ```

3. **Verify complete page content**:
   - User icon displays next to "Horodchuk Anton" heading
   - Skills section lists: Perl, Java, Delphi, JavaScript, Groovy
   - Additional section shows: Git, Gradle, SQL, HTML, CSS, Bootstrap, Agile
   - LinkedIn link in "My Contacts" section works

4. **Test responsive design**:
   - Resize browser window to test Bootstrap responsive layout
   - Content should remain readable and well-formatted at different screen sizes

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
├── index.html                     # Main website content
├── css/
│   └── bootstrap.min.css          # Bootstrap 3.x CSS framework
├── js/
│   └── bootstrap.min.js           # Bootstrap 3.x JavaScript
└── fonts/                         # Bootstrap Glyphicons fonts
    ├── glyphicons-halflings-regular.eot
    ├── glyphicons-halflings-regular.svg
    ├── glyphicons-halflings-regular.ttf
    ├── glyphicons-halflings-regular.woff
    └── glyphicons-halflings-regular.woff2
```

### Key Files to Know
- **`index.html`**: Main content file - edit this to change website content
- **`css/bootstrap.min.css`**: Bootstrap framework styles - **DO NOT** modify
- **`js/bootstrap.min.js`**: Bootstrap framework JavaScript - **DO NOT** modify
- **`.gitignore`**: Configured for JetBrains IDEs - safe to modify if needed

## External Dependencies

### CDN Resources
The website uses these external CDN resources:
- jQuery: `https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js`
- HTML5 Shiv: `https://oss.maxcdn.com/html5shiv/3.7.2/html5shiv.min.js`
- Respond.js: `https://oss.maxcdn.com/respond/1.4.2/respond.min.js`

**Note**: Bootstrap JavaScript requires jQuery, but the site's styling works without it.

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

# Test asset availability:
curl -I http://localhost:8000                        # HTML page
curl -I http://localhost:8000/css/bootstrap.min.css  # CSS file
curl -I http://localhost:8000/js/bootstrap.min.js    # JS file

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
- **Bootstrap styling not applied**: Check that `css/bootstrap.min.css` is accessible
- **Icons not displaying**: Verify fonts directory and files are present
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
- **NEVER** modify Bootstrap framework files (css/, js/, fonts/)
- **ALWAYS** validate the live GitHub Pages site after deployment