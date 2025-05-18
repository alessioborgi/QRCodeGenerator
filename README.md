# QRStaticCode Generator

A flexible Python code for generating styled QR codes with optional icons and captions. 

## Features

- **Rounded modules** for a smooth look.  
- **Custom colors** for both the QR code and the background.  
- **Icon overlay**: tint and embed any silhouette icon in the center.  
- **Caption support**: add custom text below (or overlapping) the code.  
- Fully **configurable** via function parameters.

---

## Installation

1. **Clone or copy** this repository.  

   ```bash
   git clone https://github.com/alessioborgi/QRStaticCode_Generator.git```
2. Ensure you have Python 3.7+ installed.  
3. Install dependencies:

   ```bash
   pip install qrcode[pil] Pillow```


## Usage
Import the ```generate_stylish_qr``` function and call it with your desired parameters:

``` bash 
    from qr_generator import generate_stylish_qr

    # Example: generate a QR for your project page
    generate_stylish_qr(
        url="https://example.com",
        output_path="my_qr.png",
        fill_color="#182b5f",
        back_color="white",
        icon_path="./icons/globe.png",
        icon_size_ratio=0.25,
        icon_border=30,
        caption="Project Page",
        font_path="/Library/Fonts/Ayuthaya.ttf",
        caption_size_ratio=0.10,
        caption_padding=2,
        caption_offset=-20,
        caption_color="#182b5f",
    )
```
