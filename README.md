# 3D Chess - WebGL Interactive Chess Game

![3D Chess](https://img.shields.io/badge/WebGL-2.0-blue) ![License](https://img.shields.io/badge/license-ISC-green) ![Status](https://img.shields.io/badge/status-active-success)

An immersive 3D chess game built with WebGL 2.0, featuring advanced lighting, customizable themes, and AI opponents of varying difficulty levels.

## 🎮 Features

### Game Modes
- **PC vs PC**: Watch two AI opponents battle it out
- **Human vs PC**: Challenge the computer at 5 different difficulty levels (0-4)
- **Human vs Human**: Play against another person locally

### Graphics & Rendering
- **WebGL 2.0** powered 3D rendering
- **Phong lighting model** with multiple light sources:
  - Directional light (ambient lighting)
  - Spot light with adjustable cone and decay
  - Point light with position controls
- **Normal mapping** for enhanced surface detail
- **Skybox environments** (Galaxy and Polimi themes)
- **Smooth piece animations** with 10-frame interpolation
- **Customizable piece themes** with different textures and colors

### Camera Controls
- **Multiple camera views**: White perspective, Black perspective, and Top-down view
- **WASD/Arrow keys**: Move camera up/down and rotate left/right
- **Z/X keys**: Zoom in and out
- **Dynamic view switching** during gameplay

### Interactive Features
- **3D raycasting** for piece selection with mouse clicks
- **Real-time lighting controls** via UI sliders
- **Customizable light colors** for each light source
- **Pawn promotion** with modal piece selection
- **Legal move highlighting** and validation

## 🚀 Getting Started

### Prerequisites
- Modern web browser with WebGL 2.0 support (Chrome, Firefox, Edge, Safari)
- Local web server (for loading external resources)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/YourUsername/webgl-3d-chess.git
   cd webgl-3d-chess
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start a local server**
   
   Using Python:
   ```bash
   python -m http.server 8000
   ```
   
   Using Node.js (http-server):
   ```bash
   npx http-server -p 8000
   ```
   
   Using Live Server in VS Code:
   - Install the "Live Server" extension
   - Right-click on `index.html` and select "Open with Live Server"

4. **Open in browser**
   ```
   http://localhost:8000
   ```

## 🎯 How to Play

### Starting a Game
1. Select your game mode (PC vs PC, Human vs PC, or Human vs Human)
2. Choose AI difficulty level (0-4, where 4 is the hardest)
3. Pick your color (White, Black, or Random)
4. Click **"Start new game"**

### Controls
- **Click** on a piece to select it
- **Click** on a valid square to move the selected piece
- **WASD or Arrow Keys**: Rotate and move the camera
- **Z/X Keys**: Zoom in/out
- **"Change View" button**: Switch between White, Black, and Top perspectives

### Game Features
- Legal moves are automatically calculated
- Pieces animate smoothly between squares
- Pawn promotion triggers a modal for piece selection
- Check and checkmate detection
- Castling and en passant support

## 🎨 Customization

### Lighting Controls
Access the left panel to adjust:
- **Ambient Light**: Direction (X, Y, Z)
- **Spot Light**: Position, direction, decay, cone angle
- **Point Light**: Position (X, Y, Z)
- **Light Colors**: Individual color pickers for each light type

### Themes
Use the dropdown menu to select different visual themes for pieces and board.

## 🏗️ Project Structure

```
3d-chess/
├── index.html              # Entry point with loading screen
├── package.json            # Project dependencies
├── assets/
│   ├── images/            # Textures and UI images
│   ├── models/            # 3D OBJ models for chess pieces
│   └── skybox/            # Skybox textures (Galaxy, Polimi)
├── html/
│   ├── index.html         # Main game interface
│   ├── about.html         # About page
│   └── style.css          # Styling
├── scripts/
│   ├── App.js             # Main WebGL application logic
│   ├── Board.mjs          # Chess board state and rules
│   ├── Camera.js          # Camera controls and views
│   ├── Classes.js         # GameObject and scene graph
│   ├── Pieces.js          # Piece creation and management
│   ├── Raycast.js         # Mouse picking and raycasting
│   ├── index.js           # Game controller and AI integration
│   └── utils.js           # WebGL utilities
└── shaders/
    ├── vs.glsl            # Vertex shader
    ├── fs_phong.glsl      # Phong fragment shader
    ├── skybox-vs.glsl     # Skybox vertex shader
    └── skybox-fs.glsl     # Skybox fragment shader
```

## 🛠️ Technologies

- **WebGL 2.0**: Graphics rendering
- **GLSL 3.0**: Shader programming
- **JavaScript ES6+**: Application logic
- **js-chess-engine**: Chess rules and AI
- **webgl-obj-loader**: 3D model loading
- **Bootstrap 4**: UI framework
- **OBJ/MTL**: 3D model formats

## 📝 Technical Highlights

### Rendering Pipeline
1. **Scene Graph**: Hierarchical object management with GameObject class
2. **VAO (Vertex Array Objects)**: Efficient vertex data storage
3. **Phong Shading**: Per-fragment lighting calculations
4. **Texture Mapping**: Diffuse textures with normal maps
5. **Skybox Rendering**: Separate shader program for environment

### Chess Engine
- Minimax algorithm with alpha-beta pruning
- Position evaluation based on material and board control
- 5 difficulty levels with varying search depths
- En passant, castling, and pawn promotion support

### Camera System
- Spherical coordinate system (phi, omega, radius)
- Smooth interpolation between views
- Keyboard-based camera manipulation
- Perspective projection with adjustable zoom

## 👥 Authors

- **Luca Vecchio**
- **Alessandro Lisi**
- **Alice Piemonti**

*Computer Graphics Final Project*  
*Politecnico di Milano - 2020/2021*

## 📄 License

This project is licensed under the ISC License.

## 🐛 Known Issues

- Some browsers may require explicit WebGL 2.0 enabling in flags
- Performance may vary depending on GPU capabilities
- Loading times for 3D models on slower connections

## 🚧 Future Improvements

- [ ] Add sound effects for piece movements
- [ ] Implement online multiplayer
- [ ] Add move history and undo functionality
- [ ] Include more piece themes and board styles
- [ ] Mobile touch controls support
- [ ] Save/load game states
- [ ] Performance optimizations for lower-end devices

## 🙏 Acknowledgments

- Chess engine powered by [js-chess-engine](https://github.com/josefjadrny/js-chess-engine)
- 3D models created specifically for this project
- Skybox textures from various open-source providers
- Computer Graphics course instructors at Politecnico di Milano

## 📞 Support

For questions or issues, please open an issue on the GitHub repository.

---

**Enjoy playing 3D Chess!** ♟️
