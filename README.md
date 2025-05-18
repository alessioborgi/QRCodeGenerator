# QRStaticCode Generator

**Copyright © 2025 Alessio Borgi***

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
   git clone https://github.com/alessioborgi/QRStaticCode_Generator.git
2. Ensure you have Python 3.7+ installed.  
3. Install dependencies:

   ```bash
   pip install qrcode[pil] Pillow

--- 

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
The generated PNG will be saved at the specified ```output_path```.

---

## Function Parameters

| Parameter            | Type    | Default              | Description                                             |
| -------------------- | ------- | -------------------- | ------------------------------------------------------- |
| `url`                | `str`   | *required*           | URL or text to encode in the QR code.                   |
| `output_path`        | `str`   | `"qr_with_text.png"` | Path where the PNG will be saved.                       |
| `box_size`           | `int`   | `20`                 | Pixel size of each QR module.                           |
| `border`             | `int`   | `4`                  | Border width (in modules).                              |
| `fill_color`         | `str`   | `"#000000"`          | Color of QR modules (`#RRGGBB` or CSS name).            |
| `back_color`         | `str`   | `"white"`            | Background color.                                       |
| `icon_path`          | `str`   | `None`               | Path to a silhouette icon (optional).                   |
| `icon_color`         | `str`   | `fill_color`         | Tint color for the icon.                                |
| `icon_size_ratio`    | `float` | `0.25`               | Icon width as fraction of QR width.                     |
| `icon_border`        | `int`   | `30`                 | Padding (pixels) around the icon.                       |
| `caption`            | `str`   | `None`               | Text caption below the QR (optional).                   |
| `font_path`          | `str`   | `None`               | Path to a `.ttf` font file.                             |
| `font_size`          | `int`   | *auto*               | Explicit font size in px (overrides ratio).             |
| `caption_size_ratio` | `float` | `0.30`               | Caption height as fraction of QR width.                 |
| `caption_color`      | `str`   | `"#000000"`          | Color of the caption text.                              |
| `caption_padding`    | `int`   | `4`                  | Vertical gap (px) between QR and caption.               |
| `caption_offset`     | `int`   | `-20`                | Shift caption up/down relative to gap (negative is up). |



---

## Examples

### 1. Basic QR with Default Styling

Generate a simple QR code with the default parameters:
```python
generate_stylish_qr(
    url="https://openai.com"
)
```

### 2. QR with Centered Icon
Embed and tint an icon in the middle of the QR code:
```python
generate_stylish_qr(
    url="https://example.com",
    icon_path="./icons/logo.png",
    icon_color="#FF0000",        # Tint the icon red
    icon_size_ratio=0.2,         # Icon width = 20% of QR width
    icon_border=20               # 20 px padding around the icon
)

```
### 3. QR with Overlapping Caption
Add a large caption that overlaps into the bottom border of the QR:
```python
generate_stylish_qr(
    url="https://project.com",
    caption="Visit Now!",
    caption_size_ratio=0.30,     # Caption height = 30% of QR width
    caption_offset=-40,          # Pull the text 40 px up into the QR
    caption_color="#1f2937"      # Navy‐blue caption text
)

```

---

## License

This documentation is licensed under the Creative Commons Attribution 4.0 International License (CC BY 4.0).  
You are free to **share** (copy and redistribute in any medium or format) and **adapt** (remix, transform, and build upon) this work for any purpose, even commercially, under the following terms:

1. **Attribution** — You must give appropriate credit, provide a link to the license, and indicate if changes were made.  
2. **ShareAlike** — If you remix, transform, or build upon this material, you must distribute your contributions under the same license as the original.

For details, see:  
<https://creativecommons.org/licenses/by/4.0/>
