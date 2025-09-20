# Copilot Instructions for DORA Health & Wellbeing Codebase

## Project Overview
This is a static HTML/CSS/JS website for DORA Health & Wellbeing, focused on presenting services, team, testimonials, and contact information. The codebase is organized for maintainability and ease of updates, using Bootstrap and Font Awesome for layout and icons.

## Key Structure
- **HTML files**: Each major page (e.g., `index.html`, `service cards.html`, `team.html`) is a standalone HTML file. Shared UI elements (navbar, footer) are in `-navbar.html` and `-footer.html`.
- **CSS**: All styles are in the `css/` directory. `style.css` is the main custom stylesheet. Bootstrap and Font Awesome are included locally.
- **JS**: All scripts are in the `js/` directory. Custom interactivity (e.g., flip cards) is in `flip-card.js` and others. jQuery is included locally.
- **Images & Assets**: All images are in the `images/` directory, with subfolders for organization. Fonts are in `fonts/`.

## Patterns & Conventions
- **No build step**: This is a static site. No npm/yarn build or test commands are required.
- **Page structure**: Each HTML file is self-contained, but may include shared nav/footer via copy-paste (no templating engine).
- **Responsiveness**: Bootstrap grid is used for layout. Custom classes may override Bootstrap defaults in `style.css`.
- **Icons**: Use `<i class="fas ..."></i>` for Font Awesome icons. Both local and CDN versions are included for compatibility.
- **Flip Cards**: Service cards use a `.flip-card` pattern with front/back faces. See `service cards.html` and `js/flip-card.js` for implementation.

## Developer Workflows
- **Preview**: Open HTML files directly in a browser. No server required.
- **Debugging**: Use browser dev tools. No source maps or advanced debugging setup.
- **Adding Services**: Duplicate a `.flip-card` block in `service cards.html` and update content/icons as needed.
- **Updating Styles**: Edit `css/style.css` for customizations. Avoid editing Bootstrap directly.

## External Dependencies
- Bootstrap (local in `css/`)
- Font Awesome (local in `css/`, fonts in `fonts/`)
- jQuery (local in `js/`)

## Examples
- To add a new service card: Copy an existing `.flip-card` div in `service cards.html`, change the icon and text, and update the back face.
- To update the navbar: Edit `-navbar.html` and copy changes to all HTML files as needed.

## Limitations
- No dynamic content or backend integration.
- No automated tests or CI/CD.

---
For any unclear conventions or missing documentation, ask the user for clarification or examples from the codebase.
