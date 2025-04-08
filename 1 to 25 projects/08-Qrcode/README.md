# QR Code Encoder / Decoder Python Project

## Project Overview

This project allows you to generate (encode) and read (decode) QR codes using Python. It’s simple, beginner-friendly, and helps you understand how to use external libraries like `qrcode` and `opencv-python` (cv2).

### Key Features

- Create custom QR codes with text or URLs.
- Save QR codes as image files.
- Decode QR codes from images and retrieve encoded data.

### Technologies Used

- **Python**
- **qrcode** library for QR code creation
- **PIL (Pillow)** for image handling
- **OpenCV (cv2)** for decoding QR codes

### Installation

```bash
pip install qrcode
pip install pillow
pip install opencv-python
```

### Main Functions Used

| Function | Description |
|----------|-------------|
| `qrcode.make(data)` | Creates a QR code with the provided data |
| `img.save('filename.png')` | Saves the generated QR code as an image file |
| `cv2.imread('filename.png')` | Reads an image containing a QR code |
| `cv2.QRCodeDetector().detectAndDecode(img)` | Decodes the QR code and extracts the information |

### Example Code for Encoding

```python
import qrcode

data = "https://example.com"
qr = qrcode.make(data)
qr.save("example_qr.png")
print("QR code generated and saved!")
```

### Example Code for Decoding

```python
import cv2

img = cv2.imread("example_qr.png")
detector = cv2.QRCodeDetector()
data, bbox, _ = detector.detectAndDecode(img)

if data:
    print(f"Decoded data: {data}")
else:
    print("No QR code detected.")
```

### Benefits of This Project

- Learn how to work with external Python libraries.
- Understand how encoding and decoding QR codes work.
- Build practical tools you can use for websites, apps, or personal projects.

### Credit

Tutorial by **Code With Tomi**.
YouTube Channel: [Code With Tomi](https://www.youtube.com/c/CodeWithTomi)
