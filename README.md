# LaunchStream - Running the Application Locally

This repository contains the production build of the LaunchStream web application. Below are instructions for running the app locally on your machine.

## About This Repository

This repository contains **static production files** (HTML, CSS, JavaScript bundles) that are ready to be served by any web server. It does not contain source code or a development environment.

## Prerequisites

You'll need one of the following installed on your system:
- Node.js (for using `npx serve` or `http-server`)
- Python 3 (comes pre-installed on most systems)
- Any other static file server of your choice

## Method 1: Using npx serve (Recommended)

The easiest way to run the app locally is using `npx serve`, which requires Node.js:

```bash
# Navigate to the project directory
cd /path/to/LaunchStreamXYZ

# Serve the static files (no installation needed)
npx serve -s . -l 3000
```

The app will be available at: **http://localhost:3000**

Options:
- `-s` flag enables single-page application (SPA) mode, redirecting all 404s to index.html
- `-l 3000` sets the port to 3000 (you can change this to any available port)

## Method 2: Using http-server (Node.js)

If you prefer `http-server`:

```bash
# Install http-server globally (one-time installation)
npm install -g http-server

# Navigate to the project directory
cd /path/to/LaunchStreamXYZ

# Start the server
http-server . -p 3000
```

The app will be available at: **http://localhost:3000**

## Method 3: Using Python

If you have Python installed, you can use its built-in HTTP server:

### Python 3:
```bash
# Navigate to the project directory
cd /path/to/LaunchStreamXYZ

# Start the server
python3 -m http.server 3000
```

### Python 2:
```bash
# Navigate to the project directory
cd /path/to/LaunchStreamXYZ

# Start the server
python -m SimpleHTTPServer 3000
```

The app will be available at: **http://localhost:3000**

## Method 4: Using PHP

If you have PHP installed:

```bash
# Navigate to the project directory
cd /path/to/LaunchStreamXYZ

# Start the server
php -S localhost:3000
```

The app will be available at: **http://localhost:3000**

## Accessing the Application

Once you've started a server using any of the methods above:

1. Open your web browser
2. Navigate to **http://localhost:3000** (or whatever port you specified)
3. The LaunchStream application will load and be fully functional

## Troubleshooting

### Port Already in Use
If you get an error that the port is already in use, either:
- Stop the process using that port, or
- Use a different port number (e.g., 3001, 8000, 8080)

### Application Not Loading
- Make sure you're in the correct directory (the one containing `index.html`)
- Check your browser console for any errors
- Ensure your firewall isn't blocking the local server

## About the Production Build

The files in this repository are:
- **index.html**: The main HTML file
- **static/**: Directory containing CSS, JavaScript bundles, and media files
- **manifest.json**: Web app manifest for PWA support
- **asset-manifest.json**: Build asset mapping
- Various image files (favicon, logos, features)

This is a Create React App production build, optimized and minified for deployment.

## Need the Source Code?

If you're looking to modify or develop the application, you'll need access to the source code repository, which would typically include:
- `src/` directory with React components
- `package.json` with dependencies and scripts
- Development configuration files

Contact the repository maintainers if you need access to the development source code.
