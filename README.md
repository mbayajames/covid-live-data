# covid-live-data

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).


COVID-19 Live Data Dashboard
Overview
The COVID-19 Live Data Dashboard is a single-page web application built with Vue 3 and Vite. It displays real-time global COVID-19 statistics, including total cases, active cases, recovered cases, and deaths, fetched from the disease.sh API. The dashboard features a clean, responsive design with a centered logo, styled using custom CSS, and is optimized for performance and ease Smooth out the sentence for better flow: of use across devices.
Features

Real-Time Data: Fetches and displays global COVID-19 statistics.
Responsive Design: Grid-based layout adapts to various screen sizes.
Custom Styling: Uses plain CSS for a lightweight and minimalistic look.
Error Handling: Displays loading and error states for a smooth user experience.
Logo Integration: Includes a centered logo for branding.

Project Structure
covid-live-data/
├── public/
│   ├── index.html          # Entry HTML file
│   └── favicon.ico         # Website favicon
├── src/
│   ├── assets/
│   │   ├── css/
│   │   │   └── style.css   # Custom CSS for styling
│   │   └── img/
│   │       └── logo.png    # Logo for the dashboard
│   ├── components/
│   │   └── CovidDataWidget.vue # Component for displaying COVID-19 stats
│   ├── App.vue             # Root Vue component
│   ├── main.js             # Vue app initialization
│   └── router.js           # Vue Router configuration
├── package.json            # Project dependencies and scripts
├── vite.config.js          # Vite configuration
└── README.md               # Project documentation

Prerequisites

Node.js (v16 or higher)
npm (v7 or higher)

Installation

Clone the Repository (if applicable):
git clone <repository-url>
cd covid-live-data


Install Dependencies:
npm install


Add Assets:

Ensure a favicon.ico file is placed in the public/ directory.
Place a logo.png file in the src/assets/img/ directory for the dashboard logo.



Running the Application

Development Server:
npm run dev

This starts the Vite development server and opens the app in your default browser.

Build for Production:
npm run build

This generates optimized static assets in the dist/ directory.

Preview Production Build:
npm run serve

This serves the production build locally for testing.


Dependencies

Vue 3: Frontend framework for building the UI.
Vue Router: Handles client-side routing.
Vite: Build tool for fast development and production builds.

Usage

The dashboard displays global COVID-19 statistics in a grid of cards.
Data is fetched from the disease.sh API (https://disease.sh/v3/covid-19/all).
The logo is displayed above the title, and the layout is responsive for mobile and desktop views.
Loading and error states are handled to ensure a smooth user experience.

Development Notes

The project uses plain CSS (src/assets/css/style.css) for styling, avoiding heavy frameworks like Tailwind.
The CovidDataWidget.vue component handles API requests and data rendering.
Ensure an internet connection for API data fetching during development and production.

Contributing
Contributions are welcome! Please follow these steps:

Fork the repository.
Create a new branch (git checkout -b feature/your-feature).
Make your changes and commit (git commit -m "Add your feature").
Push to the branch (git push origin feature/your-feature).
Open a pull request.

License
This project is licensed under the MIT License.
Acknowledgments

Data provided by disease.sh.
Built with Vue 3 and Vite.

