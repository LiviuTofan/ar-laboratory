# AR Story - Capybara Adventure

An Augmented Reality web application using AR.js and A-Frame that tells an interactive story through three sequential markers.

## Overview

This project implements an AR storytelling experience featuring a hungry capybara. The story unfolds across three markers that must be scanned in sequence, creating an engaging narrative with 3D models and animations.

## Story Flow

🟥 **Marker 1 - Jungle (Capybara)**
- Shows a rotating 3D capybara
- Message: "Oh no... I'm hungry!"
- Must be scanned FIRST

🟩 **Marker 2 - Desk (Watermelon)**
- Shows a rotating 3D watermelon
- Message: "Wow, this melon looks amazing!"
- Can only be viewed after scanning Marker 1
- Shows warning if Marker 1 not scanned first

🟦 **Marker 3 - Picnic (Happy Capybara + Watermelon Slice)**
- Shows a bouncing capybara and watermelon slice
- Message: "Thank you, now I'm happy!"
- Can only be viewed after scanning BOTH Marker 1 and Marker 2
- Shows warning if previous markers not scanned

## Features

- **Sequential marker tracking** - Enforces story order (jungle → desk → picnic)
- **3D model rendering** - Capybara and watermelon models with animations
- **Interactive storytelling** - Real-time feedback and story progression
- **Smooth tracking** - Optimized smoothing parameters for stable AR experience
- **Visual feedback** - Color-coded log display shows story messages

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

## How to Use

1. Open the application in a browser with camera access
2. **Scan Marker 1 (Jungle)** first - you'll see the hungry capybara
3. **Scan Marker 2 (Desk)** - you'll see the watermelon (only works after Marker 1)
4. **Scan Marker 3 (Picnic)** - you'll see the happy capybara with watermelon slice (only works after Markers 1 & 2)

If you try to scan markers out of order, you'll see a warning message!

## Markers

The application includes three NFT image markers in the `markers/` directory:
- **jungle** - Shows hungry capybara (SCAN FIRST)
- **desk** - Shows watermelon (SCAN SECOND)
- **picnic** - Shows happy capybara + slice (SCAN THIRD)

Print these markers or display them on a screen to test the AR experience.

## Technologies Used

- **AR.js** - Augmented Reality library for the web
- **A-Frame** - Web framework for building 3D/AR/VR experiences
- **glTF/GLB** - 3D model format for capybara and watermelon
- **NFT Markers** - Natural Feature Tracking for image-based AR

## Technical Details

- Smooth tracking with optimized parameters (smoothCount: 10, smoothTolerance: 0.01)
- Sequential logic enforced in JavaScript
- Models positioned and rotated for optimal viewing
- Bouncing animation on final scene for happy capybara

## Deployment

This project can be deployed on:
- **Vercel** - Zero configuration deployment
- **GitHub Pages** - Static hosting
- **Netlify** - Continuous deployment
- Any static file hosting service

## Author

Built with AR.js and A-Frame
