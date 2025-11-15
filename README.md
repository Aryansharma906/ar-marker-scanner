# 🔍 AR Marker Scanner

**Marker-Based Augmented Reality Application | 3D Model Visualization with A-Frame**

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![A-Frame](https://img.shields.io/badge/A--Frame-EF2D5E?style=flat&logo=aframe&logoColor=white)
![WebXR](https://img.shields.io/badge/WebXR-4285F4?style=flat&logo=webxr&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![AR.js](https://img.shields.io/badge/AR.js-00D4FF?style=flat&logo=augmented-reality&logoColor=white)

## 📦 Overview

**AR Marker Scanner** is a marker-based augmented reality application built with A-Frame and AR.js. This project enables users to scan physical markers (barcodes/QR codes) through their device camera and visualize interactive 3D models in real-time.

Perfect for learning AR development, creating interactive experiences, or demonstrating WebXR capabilities!

## ✨ Features

- 🎯 **Marker-Based AR**: Scan physical markers to trigger 3D content
- 🎨 **3D Model Rendering**: Display GLTF models with custom positioning and scaling
- 📱 **Mobile Compatible**: Works on smartphones and tablets
- 🔄 **Real-Time Tracking**: Smooth model placement and orientation
- 🎬 **Dynamic Loading**: JSON-based model configuration
- 🔌 **Event Handling**: markerFound and markerLost event listeners

## 🛠️ Tech Stack

- **A-Frame 1.3.0** - WebVR framework for building VR experiences
- **AR.js** - Augmented reality library for the web
- **JavaScript (ES6)** - Core logic and event handling
- **HTML5** - Structure and WebXR support
- **GLTF Models** - 3D assets for AR visualization

## 💻 Project Structure

```
ar-marker-scanner/
│
├── project 175/
│   ├── js/
│   │   ├── markerHandler.js    # AR marker event handling
│   │   ├── createModel.js       # 3D model creation logic
│   │   └── models.json          # Model configurations
│   │
│   └── assets/              # Images and resources
│
└── README.md
```

## 📥 Installation

### Prerequisites

- Modern web browser with camera access (Chrome, Firefox, Safari)
- HTTPS connection (required for camera access)
- Physical AR markers/barcodes

### Quick Start

1. **Clone the repository**
```bash
git clone https://github.com/Aryansharma906/ar-marker-scanner.git
cd ar-marker-scanner
```

2. **Navigate to project folder**
```bash
cd "project 175"
```

3. **Serve with HTTPS**
```bash
# Using Python
python -m http.server 8000

# Using Node.js http-server
npx http-server -p 8000 --ssl
```

4. **Access the application**
```
Open: https://localhost:8000
```

## 📱 Usage

### Running the AR Experience

1. Open the application in your mobile browser
2. Grant camera permissions when prompted
3. Point your camera at a compatible AR marker
4. Watch as 3D models appear on the marker!

### Model Configuration

Edit `js/models.json` to add custom models:

```json
{
  "0": {
    "barcode_value": 0,
    "model_name": "base",
    "model_url": "#",
    "position": { "x": 0, "y": 0, "z": 0 },
    "rotation": { "x": -90, "y": 0, "z": 0 },
    "color": "#795548",
    "width": 10,
    "height": 15
  },
  "1": {
    "barcode_value": 1,
    "model_name": "road",
    "model_url": "https://raw.githubusercontent.com/.../model.gltf",
    "position": { "x": 0, "y": -2.2, "z": 0 },
    "rotation": { "x": 0, "y": -90, "z": 0 },
    "scale": { "x": 3, "y": 3, "z": 3 },
    "placement_position": { "x": 1.22957, "y": -2.2, "z": 5.7 },
    "placement_rotation": { "x": 0, "y": -90, "z": 0 },
    "placement_scale": { "x": 3, "y": 3, "z": 3 }
  }
}
```

## 🎯 Key Components

### markerHandler.js

Handles AR marker detection and 3D model placement:

```javascript
AFRAME.registerComponent("markerhandler", {
  init: async function() {
    this.el.addEventListener("markerFound", () => {
      // Trigger when marker is detected
      var modelName = this.el.getAttribute("model_name");
      // Add model to scene
    });
    
    this.el.addEventListener("markerLost", () => {
      // Remove model when marker is lost
    });
  }
});
```

### createModel.js

Dynamically creates and positions 3D models based on marker data.

## 🌐 Browser Compatibility

| Browser | Version | AR Support |
|---------|---------|------------|
| Chrome (Android) | 90+ | ✅ Full Support |
| Safari (iOS) | 14+ | ✅ Full Support |
| Firefox | 88+ | ⚠️ Limited |
| Edge | 90+ | ✅ Full Support |

**Note**: Requires HTTPS and camera permissions.

## 🔧 Development

### Testing

1. Print AR markers/barcodes (0-9)
2. Test on mobile device over HTTPS
3. Verify model loading and positioning

### Debugging

- Open browser console for errors
- Check camera permissions
- Verify HTTPS connection
- Test marker visibility and lighting

## 🚀 Deployment

### GitHub Pages

1. Enable HTTPS in repository settings
2. Deploy to GitHub Pages
3. Access via `https://yourusername.github.io/ar-marker-scanner/`

### Custom Server

Ensure:
- HTTPS enabled
- CORS configured for external 3D models
- Camera permissions granted

## 📚 Learning Resources

- [A-Frame Documentation](https://aframe.io/docs/)
- [AR.js Documentation](https://ar-js-org.github.io/AR.js-Docs/)
- [WebXR Device API](https://developer.mozilla.org/en-US/docs/Web/API/WebXR_Device_API)
- [GLTF Model Format](https://www.khronos.org/gltf/)

## 🔧 Future Enhancements

- [ ] Add image tracking (not just barcodes)
- [ ] Implement multi-marker support
- [ ] Add interactive model controls
- [ ] Include sound effects
- [ ] Add screenshot/recording feature
- [ ] Optimize for low-end devices
- [ ] Add location-based AR

## 🤝 Contributing

Contributions welcome! Feel free to:
1. Fork the repository
2. Create a feature branch
3. Add new models or features
4. Submit a pull request

## 📜 License

Open-source and available for educational and personal use.

## 📬 Contact & Connect

**✨Aryan Sharma✨**

📧 *Where algorithms dream and melodies spark*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/aryan-sharma-6a7b85317/)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Aryansharma906)

*🎓 Student | 🤖 AI Generalist | 💻 Full-Stack Developer✨*

---

<div align="center">

### ⭐ If you found this helpful, give it a star!

**Built with 💜 by Aryan Sharma**

*Bridging reality and digital worlds, one marker at a time* 🔍✨

</div>
