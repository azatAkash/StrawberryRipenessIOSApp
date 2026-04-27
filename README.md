# 🍓 Strawberry Ripeness iOS App
<img width="480" height="1040" alt="IMG_2561" src="https://github.com/user-attachments/assets/01ae431a-51ff-44e1-afce-9503660d84e2" />


Native iOS app for on-device strawberry ripeness detection using CoreML + Vision.

## Requirements
- Mac with Xcode 15+
- iPhone XS or newer (iOS 15+)
- Apple ID (free account works)

## Quick Start

### 1. Clone
```bash
git clone https://github.com/Atrementos/StrawberryRipenessDetection
cd StrawberryRipenessDetection/ios
```

### 2. Add the model
Download `best.mlpackage` from [Releases](https://github.com/Atrementos/StrawberryRipenessDetection/releases) and drag it into Xcode under the `strawberry` folder.

### 3. Sign the app
Xcode → strawberry target → **Signing & Capabilities** → set Team to your Apple ID

### 4. Run
- Plug in iPhone via USB → tap **Trust**
- Select your iPhone in Xcode top bar
- Press **▶ Cmd+R**
- On iPhone: **Settings → General → VPN & Device Management → Trust**

## How it Works
1. Tap **Camera** or **Gallery** to select a strawberry photo
2. Tap **Detect Ripeness**
3. Bounding boxes appear on image — tap any row in the list to highlight that strawberry

## Model
| Property | Value |
|---|---|
| Format | CoreML FP16 (.mlpackage) |
| Architecture | YOLO11n |
| Classes | ripe / partially_ripe / unripe |
| Model size | 2.9 MB |
| Inference | ~0.5s on Neural Engine |
| Internet | Not required |

## Tech Stack
- SwiftUI
- CoreML + Vision framework
- UIImagePickerController
- On-device inference — no backend needed

