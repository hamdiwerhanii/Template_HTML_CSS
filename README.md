# Leon — Creative Agency Landing Page Template

A single-page, responsive agency landing page built with pure HTML5 and CSS3, with no JavaScript and no build step.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![Font Awesome](https://img.shields.io/badge/Font%20Awesome-6.5.1-528DD7?logo=fontawesome&logoColor=white)
![normalize.css](https://img.shields.io/badge/normalize.css-8.0.1-lightgrey)
![Google Fonts](https://img.shields.io/badge/Google%20Fonts-Work%20Sans-4285F4?logo=googlefonts&logoColor=white)

![Landing section background](Images/landing.jpg)

## Overview

**Leon** is a minimal, creative-agency style one-page website template. I built it as a front-end practice project to work on core layout techniques: CSS Grid, Flexbox, custom properties (CSS variables), pseudo-element decorations, media queries, and a menu that works without JavaScript.

The page uses placeholder copy (lorem ipsum, a sample agency name and email), so you can use it as a starting point for a portfolio or small-agency site.

## Features

- **Header with a CSS-only dropdown menu.** A three-bar "hamburger" icon opens the navigation on hover, with an animated middle bar, an arrow made from CSS borders, and a link hover animation.
- **Smooth in-page navigation.** Anchor links to Services, Portfolio, About and Contact, using `scroll-behavior: smooth`.
- **Full-height landing section.** A hero image covers the viewport, with an intro heading and text centered on top.
- **Features strip.** Three feature cards with Font Awesome icons in a responsive auto-fill grid.
- **Services section.** Four services (Graphic Design, UI & UX, Web Design, Web Development) with icons, plus a decorative image column that is hidden below 1200px.
- **Portfolio section.** Three project cards with an image, title and description.
- **About section.** An image framed by decorative `::before` and `::after` shapes, with two text blocks separated by an accent rule.
- **Contact section.** A `mailto:` link and social network icons (YouTube, Facebook, Twitter).
- **Footer** with copyright text.
- **Reusable "special heading" component.** Large faded section titles with an overlapping subtitle.
- **Theme variables.** The main color, secondary color, section padding and background are set in one place in `:root`.
- **Responsive layout.** A Bootstrap-like fixed-width container at 768, 992 and 1200px breakpoints, `auto-fill`/`minmax()` grids, and layout changes for mobile and tablet.

## Tech Stack

| Category       | Technology                                                    |
| -------------- | ------------------------------------------------------------- |
| Markup         | HTML5                                                         |
| Styling        | CSS3 (Flexbox, Grid, custom properties, media queries)       |
| CSS reset      | [normalize.css](https://github.com/necolas/normalize.css) v8.0.1 (bundled locally) |
| Icons          | [Font Awesome Free](https://fontawesome.com) 6.5.1 (bundled locally with webfonts) |
| Typography     | [Work Sans](https://fonts.google.com/specimen/Work+Sans) via Google Fonts |

## Project Structure

```
Template_HTML_CSS/
├── Template1.html        # The single page (entry point)
├── Css/
│   ├── Template1.css     # Main stylesheet: variables, components, sections
│   ├── normalize.css     # normalize.css v8.0.1
│   └── all.min.css       # Font Awesome 6.5.1 (minified)
├── Images/               # Logo, landing, services, portfolio and about images
├── webfonts/             # Font Awesome font files (.ttf / .woff2)
└── README.md
```

## Page Sections

| Section    | Anchor       | Description                                           |
| ---------- | ------------ | ----------------------------------------------------- |
| Header     | —            | Logo and hover dropdown navigation                    |
| Landing    | —            | Full-screen hero with intro text                      |
| Features   | —            | Three icon cards                                      |
| Services   | `#services`  | Four services and a decorative image                  |
| Portfolio  | `#portfolio` | Three project cards                                   |
| About      | `#about`     | Image with decorative shapes and descriptive text     |
| Contact    | `#contact`   | Email link and social icons                           |
| Footer     | —            | Copyright line                                        |

## Getting Started

### Prerequisites

You only need a modern web browser. There are no dependencies to install and no build tools.

### Run locally

```bash
git clone https://github.com/hamdiwerhanii/Template_HTML_CSS.git
cd Template_HTML_CSS
```

Then use one of these options:

- Open `Template1.html` directly in your browser.
- Or use the **Live Server** extension in VS Code: right-click `Template1.html` and choose **Open with Live Server**.
- Or start any static server, for example:

  ```bash
  npx serve .
  # or
  python -m http.server 8000
  ```

  Then open `http://localhost:8000/Template1.html` (adjust the port to match your server).

> An internet connection is needed to load the Work Sans font from Google Fonts. All other assets are stored locally.

## Customization

- **Colors and spacing:** edit the variables at the top of `Css/Template1.css`:

  ```css
  :root {
      --main-color: #10cab7;
      --secondry-color: #2c4755;
      --section-padding: 60px;
      --section-background: #f6f6f6;
      --main-duration: 0.3s;
  }
  ```

- **Content:** replace the placeholder text, the agency name ("Leon") and the email address in `Template1.html`.
- **Images:** swap the files in `Images/`, keeping the same names or updating the `src` paths. The landing background is set in CSS (`.landing { background-image: ... }`).

## Known Issues and Roadmap

This is a learning project. Reviewing the code shows a few things that could be fixed or improved:

- [ ] The viewport meta tag is split across two lines (`content="width=\n, initial-scale=1.0"`). It should be `width=device-width, initial-scale=1.0` so mobile rendering works correctly.
- [ ] `@media (max-width: 767)` in the Services styles has no unit (it should be `767px`), so the rule never applies.
- [ ] `calc(var(--section-padding) +60px)` in the About section needs a space after `+` to be valid CSS.
- [ ] `Template1.css` is loaded before `normalize.css`. It should be loaded after, so the custom styles take precedence.
- [ ] The dropdown menu opens only on hover, which does not work well on touch devices. A click toggle (with a small script or the checkbox technique) would fix this.
- [ ] Images have empty `alt` attributes, and the social icons are not links yet.
- [ ] The contact block has a duplicate `class` attribute (`class="social" class="link"`).
- [ ] The `--main-duration` variable is defined but not used, and `.parent` is an unused rule.
- [ ] Possible next steps: a working contact form, real portfolio content, and deployment to GitHub Pages.

## Contributing

Contributions, suggestions and bug reports are welcome. Fork the repository, create a branch for your change, and open a pull request.

## License

No license file is currently included; all rights reserved by the author.
Third-party assets keep their own licenses: Font Awesome Free (icons CC BY 4.0, fonts SIL OFL 1.1, code MIT) and normalize.css (MIT).

## Author

**Hamdi Werhani** — GitHub [@hamdiwerhanii](https://github.com/hamdiwerhanii)
