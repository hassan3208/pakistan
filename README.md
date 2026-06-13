# PakVista - Pakistan Tourism Guide

PakVista is a modern web application designed to showcase Pakistan's most beautiful tourist destinations. Discover historic cities, lush valleys, and vibrant coastal areas through an intuitive and visually appealing interface.

## 🌍 Live Demo

**Development Environment:** [https://pakistan-dev.onrender.com/](https://pakistan-dev.onrender.com/)

## ✨ Features

- **Top Destinations**: Explore Pakistan's five most iconic tourist spots
- **Destination Details**: Information about:
  - **Lahore** - Punjab's historic city known for Badshahi Mosque, Lahore Fort, and renowned cuisine
  - **Hunza Valley** - Gilgit-Baltistan's scenic paradise with Rakaposhi and Attabad Lake
  - **Karachi** - Sindh's coastal gem featuring Clifton Beach and Mohatta Palace
  - **Swat** - KPK's adventure hub with Malam Jabba and Mahodand Lake
- **Responsive Design** - Optimized for desktop, tablet, and mobile devices
- **Clean UI** - Modern and professional design with Pakistan-inspired color scheme

## 🛠️ Tech Stack

- **Frontend**: HTML5, CSS3, JavaScript
- **Deployment**: Render (https://render.com/)
- **CI/CD**: GitHub Actions
- **Containerization**: Docker

## 📁 Project Structure

```
.
├── index.html              # Main landing page
├── style.css               # Styling (CSS custom properties for theming)
├── README.md               # Project documentation
├── .github/
│   └── workflows/
│       ├── ci-dev.yml      # Development CI pipeline
│       └── cd-prod.yml     # Production CD pipeline
└── Dockerfile              # Docker container configuration
```

## 🚀 Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- For local development: Node.js (optional, for local testing)

### Running Locally

1. Clone the repository:
   ```bash
   git clone https://github.com/hassan3208/pakistan.git
   cd pakistan
   ```

2. Open `index.html` in your browser or use a local server:
   ```bash
   # Using Python
   python -m http.server 8000
   
   # Using Node.js (http-server)
   npx http-server
   ```

3. Navigate to `http://localhost:8000` (or the port shown in your terminal)

## 🐳 Docker

Build and run with Docker:

```bash
# Build the image
docker build -t pakvista .

# Run the container
docker run -p 8000:80 pakvista
```

Then visit `http://localhost:8000`

## 📋 CI/CD Pipelines

### Development Pipeline (`ci-dev.yml`)
- Triggered on pull requests to the `develop` branch
- Runs HTML linting with htmlhint
- Builds and tests Docker image
- Pushes to DockerHub with `dev-latest` and `dev-{sha}` tags

### Production Pipeline (`cd-prod.yml`)
- Triggered on pushes to `main` branch
- Checks out code
- Deploys to Render production environment
- Requires `RENDER_DEPLOY_HOOK_PROD_URL` secret configured

## 🔐 Environment Variables

For CI/CD to work, configure the following secrets in GitHub:
- `DOCKERHUB_USERNAME` - DockerHub account username
- `DOCKERHUB_TOKEN` - DockerHub authentication token
- `RENDER_DEPLOY_HOOK_PROD_URL` - Render deployment webhook URL

## 🎨 Color Scheme

- **Navy Blue** (`#1F3864`) - Primary color
- **Blue** (`#2E5FA3`) - Secondary color
- **Green** (`#1D6A39`) - Accent color
- **Light** (`#F0F4F8`) - Background
- **White** (`#FFFFFF`) - Text backgrounds

## 📱 Responsive Breakpoints

- Desktop: Full layout with navigation bar
- Tablet: Flexible navigation and content
- Mobile (≤600px): Vertical navigation menu, optimized spacing

## 🤝 Contributing

Contributions are welcome! Please:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is part of the DevOps Fundamentals Term Project at UCP (University of Central Punjab).

## 👨‍💼 Author

**Hassan** - [GitHub Profile](https://github.com/hassan3208)

## 📧 Contact

For questions or feedback, please open an issue on the [GitHub repository](https://github.com/hassan3208/pakistan/issues).

---

**Last Updated:** June 13, 2026  
**Version:** 1.0.0
