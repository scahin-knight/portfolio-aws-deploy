# Premium DevOps & AI Portfolio Website

A modern, responsive, and animated personal portfolio website tailored for a Cloud/DevOps and AI Engineering student. Built entirely with Vanilla web technologies for maximum performance and easy deployment.

## Features
- **Pure Vanilla Stack**: HTML5, CSS3, JavaScript (No frameworks, No Bootstrap, No Tailwind).
- **Design Philosophy**: Premium glassmorphism aesthetic with an elegant dark theme default.
- **Theme Support**: Integrated Dark/Light mode toggle with `localStorage` persistence.
- **Interactivity**: Smooth scrolling, custom animated cursor, intersection observer animations, typing effects.
- **Responsiveness**: Mobile-first media queries ensuring perfect layout across desktops, tablets, and phones.
- **Sections Included**: Hero, About, Skills (animated progress bars), Projects (glass cards), Experience timeline, Certifications, Achievements, GitHub stats, and a Contact form.
- **Custom 404**: Styled "Not Found" error page.

## File Structure
```
portfolio/
├── index.html       # Main portfolio page
├── style.css        # All styling, variables, glassmorphism, and animations
├── script.js        # Vanilla JS interactivity
├── 404.html         # Custom error page
├── README.md        # Documentation
└── assets/          # Directory for images, icons, and PDF resume
    ├── images/
    └── icons/
```

## Setup & Deployment Instructions

### Local Development
Since this project uses pure vanilla HTML/CSS/JS, it runs entirely in the browser without any build steps or node modules required.
1. Clone or download this repository.
2. Open `index.html` in your favorite browser.
   - *Note: Some modern browsers may block specific local JS capabilities (like fetching local files). For the best experience, run a local server (e.g., using VS Code Live Server extension or `python -m http.server`).*

### Deployment
This static site is ready to be hosted on any platform supporting static files:

**GitHub Pages (Recommended & Free)**
1. Create a new GitHub repository and push these files.
2. Go to your repository **Settings** > **Pages**.
3. Select the `main` branch as your source and hit Save.
4. Your site will be live at `https://<yourusername>.github.io/<repository-name>/`.

**Vercel / Netlify**
1. Sign in to [Vercel](https://vercel.com/) or [Netlify](https://netlify.com/).
2. Select "Add New Project" or "Import from Git".
3. Point to your repository. They will auto-detect a static site and deploy it instantly.

## Customization Checklist

Before going live, please ensure you update the placeholders with your actual data:

- [ ] Add your actual profile image to `assets/images/profile.jpg` (Update the `<div class="profile-img-placeholder">` in `index.html` with an `<img>` tag).
- [ ] Add your actual resume PDF to `assets/resume.pdf`.
- [ ] Update project descriptions, repository links, and live demo links.
- [ ] Connect the GitHub Stats section to the actual GitHub API or hardcode your latest stats.
- [ ] Verify social media links (LinkedIn, GitHub) point exactly to your profiles.
- [ ] Update the contact email in the "Get In Touch" section and ensure your backend endpoint is configured if you want the form to actually send emails (e.g., using Formspree or Netlify Forms).

## Connecting the Contact Form
Currently, the form simulates a submission. To receive actual emails:
1. Sign up for a free service like [Formspree](https://formspree.io/).
2. In `index.html`, add the `action` attribute to your form:
   ```html
   <form id="contact-form" class="contact-form" action="https://formspree.io/f/YOUR_ENDPOINT" method="POST">
   ```
3. Remove or modify the `preventDefault` behavior in `script.js` to allow the form submission to post to Formspree.

## Connecting GitHub API (Optional)
To replace the animated placeholder stats with real GitHub API data, you can use the `fetch` API in `script.js`:
```javascript
fetch('https://api.github.com/users/sachin2008')
  .then(response => response.json())
  .then(data => {
    // Update DOM elements with data.public_repos, data.followers, etc.
  });
```

---
*Built with passion and pure code.*
