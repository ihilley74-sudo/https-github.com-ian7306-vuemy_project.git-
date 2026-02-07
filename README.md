# My Portfolio

A modern, responsive portfolio website built with Vue.js 3 and Vite.

## Features

- **Responsive Design**: Works seamlessly across desktop, tablet, and mobile devices
- **Modern UI**: Clean and professional interface with smooth animations
- **Sections**:
  - Hero section with call-to-action buttons
  - About Me with skills showcase
  - Projects gallery with multiple portfolio items
  - Contact form with social links
  - Sticky navigation header
  - Footer with current year

## Tech Stack

- Vue.js 3 (Composition API)
- Vite (Build tool)
- CSS3 (with animations)
- ES6+ JavaScript

## Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn

### Installation

1. Clone the repository
```bash
git clone <repository-url>
cd <repository-directory>
```

2. Install dependencies
```bash
npm install
```

3. Start the development server
```bash
npm run dev
```

The application will be available at `http://localhost:3000`

### Build for Production

```bash
npm run build
```

The built files will be in the `dist` directory.

### Preview Production Build

```bash
npm run preview
```

## Project Structure

```
.
├── src/
│   ├── components/
│   │   ├── Header.vue      # Navigation header
│   │   ├── Hero.vue        # Hero section
│   │   ├── About.vue       # About section
│   │   ├── Projects.vue    # Projects gallery
│   │   ├── Contact.vue     # Contact form
│   │   └── Footer.vue      # Footer
│   ├── App.vue             # Main app component
│   └── main.js             # Application entry point
├── index.html              # HTML template
├── vite.config.js          # Vite configuration
└── package.json            # Dependencies and scripts
```

## Customization

To personalize the portfolio:

1. Update the content in each component (`src/components/`)
2. Modify the skills in `About.vue`
3. Add your projects in `Projects.vue`
4. Update contact information in `Contact.vue`
5. Change colors and styles in the component `<style>` sections

## License

This project is open source and available under the MIT License.