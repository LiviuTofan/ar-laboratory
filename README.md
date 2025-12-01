# AR Project

An Augmented Reality web application using AR.js and A-Frame for marker-based AR experiences.

## Overview

This project implements an AR application that displays 3D models when specific image markers are detected. It uses marker-based tracking to overlay 3D content in real-world environments.

## Features

- Image marker tracking using AR.js
- Multiple marker support (desk, jungle, picnic, etc.)
- 3D model rendering with glTF/GLB format
- Interactive 3D scene with custom markers

## Project Structure

```
├── index.html              # Main AR application
├── dungeon.py             # Python script (if applicable)
├── markers/               # AR image markers
│   ├── desk.*
│   ├── jungle.*
│   └── picnic.*
├── models/                # 3D models
│   ├── capybara_low_poly.glb
│   ├── slice_of_watermelon.glb
│   └── watermelon.glb
├── textures/              # Texture files
│   └── Atlas_baseColor.png
└── scene.gltf            # Main 3D scene

```

## Getting Started

### Prerequisites

- A web browser with WebGL and camera support
- A local web server (due to browser security restrictions)

### Running the Application

1. Start a local web server in the project directory:
   ```bash
   python -m http.server 8000
   ```
   or
   ```bash
   python3 -m http.server 8000
   ```

2. Open your browser and navigate to:
   ```
   http://localhost:8000
   ```

3. Allow camera access when prompted

4. Point your camera at one of the marker images in the `markers/` folder

## Markers

The application includes several image markers located in the `markers/` directory:
- `desk` - Desk marker
- `jungle` - Jungle marker  
- `picnic` - Picnic marker

Print these markers or display them on a screen to test the AR experience.

## Technologies Used

- **AR.js** - Augmented Reality library for the web
- **A-Frame** - Web framework for building 3D/AR/VR experiences
- **glTF/GLB** - 3D model format

## Development

To modify the AR experience, edit `index.html` and update the A-Frame scene components.

## License

[Add your license here]

## Author

[Add your name/info here]
