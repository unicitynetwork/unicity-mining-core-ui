# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Build/Deployment Commands
- Serve locally: Use any static HTTP server (Python: `python -m http.server`, Node: `npx serve`)
- No build process required (static HTML/CSS/JS files)
- Production: Deploy files to a web server supporting static content

## Code Style Guidelines
- HTML: Use standard HTML5 semantic markup with consistent indentation (4 spaces)
- CSS: Follow BEM naming convention for custom classes
- JavaScript:
  - Use camelCase for variables and function names
  - Prefix private functions with underscore (e.g., `_formatter`)
  - Format numbers with formatter utility functions
  - Handle API errors with the standardized notify pattern
  - Use jQuery for DOM manipulation and AJAX requests
  - Maintain consistent error handling using the `.fail()` pattern
  
## API Integration
- Base API URL defined in `miningcore-ui.js`
- API endpoints follow RESTful patterns (`/pools`, `/pools/{id}/miners`, etc.)
- All API calls should include error handling with user notification

## Templating Approach
- Dynamic content populated via jQuery selectors (`$('#elementId').text()`)
- Charts rendered using Chartist.js
- Use existing notification system for alerts/messages