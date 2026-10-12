# Lucky Image Tracer 🔱

A Python Turtle and OpenCV project that converts an image into a high-contrast outline and draws it on screen using Turtle Graphics. The included input artwork is a Maa Durga / Navratri illustration (`maadurga.png`).

> Created by Lucky — a small experiment combining Python, image processing, and digital art.

## Preview / What it does

- Loads `maadurga.png` from the project folder.
- Converts the image to grayscale.
- Applies blur and adaptive thresholding with OpenCV to extract dark outlines.
- Uses Python Turtle to trace the detected points in a graphics window.
- Scales large images to fit the drawing canvas while preserving their aspect ratio.

**Note:** This project creates a monochrome/gray outline drawing. It does not reproduce the original image in full colour. Drawing speed depends on the number of detected points and may be slow for detailed images.

## Requirements

- Python 3
- OpenCV (`opencv-python`)
- NumPy
- Tk support for Python Turtle (normally included with standard Windows Python installers)

## Run on Windows

1. Download and extract this repository ZIP.
2. Open the folder that contains `main.py` and `maadurga.png`. In the uploaded archive, the path is `Lucky-Image-Tracer/image-tracer-main/`.
3. Open Command Prompt in that folder.
4. Install dependencies:

   ```bash
   py -m pip install opencv-python numpy
   ```

5. Run the program:

   ```bash
   py main.py
   ```

A Turtle graphics window should open and begin drawing. Keep the window open until the drawing finishes; close it to exit.

## Use another image

1. Place your image in the same folder as `main.py`.
2. Either replace `maadurga.png` with your image (keep the filename `maadurga.png`), or change this line in `main.py` to match your image filename:

   ```python
   IMAGE_FILE = "maadurga.png"
   ```

Use a clear image with strong contrast for cleaner outlines. Images with lots of texture or fine detail can produce many points and take longer to draw.

## Configuration

In `main.py`, you can adjust the drawing window limits:

```python
MAX_DRAW_WIDTH = 1000
MAX_DRAW_HEIGHT = 650
```

These values limit the image's displayed dimensions; the image's aspect ratio is preserved.

## Project structure

```text
Lucky-Image-Tracer/
└── image-tracer-main/
    ├── main.py       # Image processing and Turtle drawing logic
    ├── maadurga.png  # Default input image
    ├── README.md     # Project instructions
    └── LICENSE       # License file included with the project
```

## Built with

- [Python](https://www.python.org/)
- [OpenCV](https://opencv.org/)
- [NumPy](https://numpy.org/)
- Python Turtle Graphics

## Festival note

🪷 **शुभ नवरात्रि | जय माता दी** 🔱

Made with Python and creativity by **Lucky**.
