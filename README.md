# PlayQ Documentation

Official documentation for **PlayQ** - An AI-powered Test Automation Framework built on Playwright and TypeScript.

## 🌐 Live Documentation

Visit the documentation site: [https://github.com/NcsQ/playq-docs](https://github.com/NcsQ/playq-docs)

## 📖 About PlayQ

**PlayQ** is a test automation framework that combines the power of Playwright with intelligent automation capabilities. It provides:

- **PatternIQ** – Self-healing, pattern-based locators
- **SmartAI** – DOM intelligence engine for stable selectors
- **DataGenIQ** – Synthetic data generation for realistic test data

Built for complex platforms like Microsoft Dynamics 365 CRM, Salesforce, and iValua.

## 🚀 Features

- Comprehensive API documentation
- Step-by-step tutorials
- Code examples for both Playwright and Cucumber
- Session recordings and training materials
- Search functionality across all documentation

## 🛠️ Built With

- [Docusaurus](https://docusaurus.io/) - Documentation framework
- [TypeScript](https://www.typescriptlang.org/) - Type-safe development
- [GitHub Pages](https://pages.github.com/) - Hosting

## 💻 Local Development

### Prerequisites

- Node.js (v18 or higher)
- npm

### Installation

```bash
git clone https://github.com/thusitha-bandara/PlayQ-Docs.git
cd PlayQ-Docs
npm install
```

### Running Locally

```bash
npm run start
```

This command starts a local development server and opens a browser window. Most changes are reflected live without restarting the server.

### Build

```bash
npm run build
```

This command generates static content into the `build` directory.

### Deploy

```bash
npm run deploy
```

This command builds and deploys the documentation to GitHub Pages.

## 📁 Project Structure

```
PlayQ-Docs/
├── docs/               # Documentation markdown files
│   ├── Introduction.md
│   └── tutorials/      # Tutorial guides
├── src/
│   ├── css/           # Custom styles
│   └── pages/         # Custom pages (Sessions, etc.)
├── static/            # Static assets (images, files)
│   └── img/
├── docusaurus.config.ts
├── sidebars.ts
└── package.json
```

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 Documentation Guidelines

- Use clear, concise language
- Include code examples for both Playwright and Cucumber
- Add screenshots or diagrams where helpful
- Follow the existing markdown structure
- Test locally before submitting

## 📧 Contact

For questions or support, please contact the PlayQ team.

## 📄 License

Copyright © 2025 PlayQ. Built with Docusaurus.

---

**Note:** This is the documentation repository. For the main PlayQ framework, visit [NcsQ/PlayQ](https://github.com/NcsQ/PlayQ).