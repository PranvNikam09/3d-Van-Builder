# Big Bear Vans 3D Configurator

A high-performance, interactive 3D web application designed for customizing Sprinter 144 camper vans. This tool allows users to visualize their dream van in real-time, configure interior and exterior components, and request professional quotes.

## 🚀 Overview

The **Big Bear Vans 3D Configurator** provides a seamless user experience for van enthusiasts to build and customize their vehicles. Built with modern web technologies and 3D rendering engines, it bridges the gap between imagination and reality.

### Key Features

- **Interactive 3D Visualization**: Real-time 3D rendering of the van using Three.js and React Three Fiber.
- **Color Customization**: Choose from 7+ professional van colors (Black, Blue Grey, Graphite Grey, Pebble, Silver Grey, Stone Grey, White).
- **Multi-Step Configuration**:
  - **Interior**: Customize the driver's area, bed/dinette, shower, and storage solutions.
  - **Exterior**: Select roof racks, windows, and panels.
  - **System**: Configure climate control, power sources, and ventilation.
- **3D Scene Export**: Export your final configuration as a `.glb` file, automatically uploaded to AWS S3.
- **Quote Generation**: Integrated form to submit your configuration for a professional price estimate.
- **User Authentication**: Secure Login/Registration and Google OAuth integration to save and manage configurations.
- **Rendering Library**: Access and manage your previously saved 3D models from your personal dashboard.

## 🛠️ Tech Stack

- **Frontend**: [React](https://reactjs.org/) + [Vite](https://vitejs.dev/)
- **3D Engine**: [Three.js](https://threejs.org/) via [@react-three/fiber](https://github.com/pmndrs/react-three-fiber) & [@react-three/drei](https://github.com/pmndrs/drei)
- **UI Framework**: [React Bootstrap](https://react-bootstrap.github.io/) & [FontAwesome](https://fontawesome.com/)
- **State Management**: React Context API
- **Cloud Services**: [AWS S3](https://aws.amazon.com/s3/) (Model Storage), Google OAuth (Authentication)
- **Styling**: Vanilla CSS with modern HSL palettes and glassmorphism elements.
- **Testing**: [Jest](https://jestjs.io/) & [React Testing Library](https://testing-library.com/)

## 📂 Project Structure

```text
src/
├── components/      # Reusable UI and Protected Route components
├── context/         # AuthContext for state management
├── pages/           # Page components (Home, Profile, Login, etc.)
├── routes/          # Application routing (React Router)
├── utils/           # Helper functions and Quote form logic
├── ModelData.jsx    # Centralized data for 3D components
├── MultiStepForm.jsx# The core configurator logic
└── [Color]Van.jsx   # Specific 3D viewer components for each van color
```

## ⚙️ Getting Started

### Prerequisites

- Node.js (v18 or higher recommended)
- npm or yarn

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/PranvNikam09/3d-Van-Builder.git
   cd 3d-Van-Builder
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Environment Variables**:
   Create a `.env` file in the root directory and add the following:
   ```env
   VITE_REACT_APP_API_URL=your_api_url
   VITE_REACT_APP_AWS_ACCESS_KEY_ID=your_aws_key
   VITE_REACT_APP_AWS_SECRET_ACCESS_KEY=your_aws_secret
   VITE_REACT_APP_AWS_REGION=your_aws_region
   VITE_REACT_APP_AWS_S3_BUCKET_NAME=your_bucket_name
   ```

4. **Run the development server**:
   ```bash
   npm run dev
   ```

## 📜 Scripts

- `npm run dev`: Start development server.
- `npm run build`: Build the project for production.
- `npm run preview`: Preview the production build locally.
- `npm run lint`: Run ESLint to check for code issues.
- `npm run test`: Run the test suite.

## 🤝 Contributing

Contributions are welcome! Please fork the repository and create a pull request with your changes.

## 📄 License

This project is licensed under the MIT License - see the `package.json` file for details.

---

*Developed with ❤️ by Pranav Nikam for Big Bear Vans.*
