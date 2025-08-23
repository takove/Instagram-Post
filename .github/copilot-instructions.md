# Instagram Post Clone - HTML/CSS Project

Always reference these instructions first and fallback to search or bash commands only when you encounter unexpected information that does not match the info here.

## Project Overview
This is a static HTML/CSS Instagram post clone that displays a single Instagram-style post with interactive elements. The project uses:
- Pure HTML5 and CSS3 (no build tools required)
- Flask development server for local testing
- FontAwesome icons for UI elements
- Responsive design with hover/focus states
- Interactive like button with CSS animations

## Working Effectively

### Initial Setup
- Install Flask: `pip3 install flask` -- takes 1-2 seconds when cached, up to 30 seconds on first install
- Start development server: `python3 server.py` -- takes 2-3 seconds to start
- NEVER CANCEL the server startup - it runs immediately but stays active for development

### Running the Application
- ALWAYS install Flask first before starting the server
- Server runs on `http://localhost:3000` (port 3000, not the typical 5000)
- Access the Instagram post at: `http://localhost:3000/Instagram%20Post/` (note the URL-encoded space)
- Alternative: Copy files to root with `cp "Instagram Post/index.html" index.html && cp "Instagram Post/style.css" style.css` to access at `http://localhost:3000/`

### Development Workflow
- Main project files are in the `Instagram Post/` directory (note the space in the name)
- `Instagram Post/index.html` - Main HTML structure with semantic markup
- `Instagram Post/style.css` - All styling including responsive design and animations
- `server.py` - Flask development server (no modifications needed)
- No build process required - changes are immediately visible on page refresh

## Validation
- ALWAYS test the like button functionality - it should change the heart icon color when clicked
- ALWAYS verify the responsive design by resizing the browser window
- Test external resources load (FontAwesome icons and Picsum image)
- Ensure proper accessibility with keyboard navigation (Tab through interactive elements)
- Validate the server serves files correctly from both root and subdirectory paths

## Common Tasks

### Starting Fresh
```bash
# Install dependencies (if not already installed)
pip3 install flask

# Start the development server  
python3 server.py

# Access the application
# Visit http://localhost:3000/Instagram%20Post/ in your browser
```

### Making Changes
- Edit `Instagram Post/index.html` for structure changes
- Edit `Instagram Post/style.css` for styling changes  
- Refresh browser to see changes (no build step needed)
- Server automatically reloads when files change (Flask debug mode enabled)

### Testing Interactive Features
- Click the heart icon to test the like button animation
- Test keyboard navigation with Tab key
- Verify hover states on interactive elements
- Test responsive design by resizing browser window

## Project Structure

```
├── README.md (and localized versions)
├── server.py (Flask development server)
└── Instagram Post/
    ├── index.html (Main Instagram post HTML)
    └── style.css (All styling and animations)
```

## Key Features to Test
- **Like Button**: Clicking the heart changes color with heartbeat animation
- **Responsive Design**: Layout adapts to mobile screens (test at 480px and 375px widths)
- **Accessibility**: Proper ARIA labels and keyboard navigation
- **External Resources**: FontAwesome icons and placeholder image from Picsum
- **Hover Effects**: Interactive elements have hover states
- **Semantic HTML**: Proper use of header, main, article, footer elements

## Common File Contents Reference

### Repository Root Files
```bash
ls -la
total 32
drwxr-xr-x 4 runner docker 4096 Instagram Post/
-rw-r--r-- 1 runner docker 1114 README.md
-rw-r--r-- 1 runner docker 1207 README.es.md  
-rw-r--r-- 1 runner docker 1148 README.cn.md
-rw-r--r-- 1 runner docker 1614 server.py
```

### Instagram Post Directory
```bash
ls -la "Instagram Post/"
total 16
-rw-r--r-- 1 runner docker 2853 index.html
-rw-r--r-- 1 runner docker 3888 style.css
```

### Server Startup Output
```
* Serving Flask app 'server'
* Debug mode: on
* Running on all addresses (0.0.0.0)
* Running on http://127.0.0.1:3000
* Running on http://10.1.0.52:3000
Press CTRL+C to quit
* Restarting with stat
* Debugger is active!
```

## Troubleshooting

### Common Issues
- **"No module named 'flask'"** - Run `pip3 install flask`
- **"404 Missing index.html"** - Access `http://localhost:3000/Instagram%20Post/` or copy files to root
- **Icons not showing** - FontAwesome CDN may be blocked, this is normal in some environments
- **Image not loading** - Picsum image may be blocked, this is normal in some environments
- **Server not starting** - Check if port 3000 is already in use

### Manual Testing Checklist
After making changes, always verify:
- [ ] Flask server starts without errors
- [ ] Instagram post loads at correct URL
- [ ] Like button is clickable and shows animation
- [ ] Layout is responsive (test mobile view)
- [ ] All interactive elements are keyboard accessible
- [ ] Hover states work on desktop
- [ ] No console errors in browser developer tools

## External Dependencies
- **FontAwesome 6**: `https://kit.fontawesome.com/b1602be2ba.js` (for icons)
- **Picsum Photos**: `https://i.picsum.photos/id/237/536/354.jpg` (for post image)
- **Flask**: Python web framework for development server

Note: External resources may be blocked in some environments, but the application structure and CSS animations will still function correctly.