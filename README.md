
# 🚀 Image Compression Using Cubic Bézier Curve
## What is this project about?
This project demonstrates an image compression method for 600x600 RGB images by applying cubic Bézier curves. The technique significantly reduces storage space while maintaining visual quality, achieving a compression ratio of approximately 6:1.

## Overview
The compression works by dividing the image into blocks of 25 pixels and fitting a cubic Bézier curve to each block. For each block, only 4 control points (P₀, P₁, P₂, and P₃) are stored. These control points are used to reconstruct the pixel values by calculating the curve's t values, providing an efficient way to encode and decode the image.

## Features
- **Efficient Storage:** Instead of storing each pixel, we store 4 control points per 25-pixel block.
- **Compression Ratio:** Achieves approximately 6:1 compression.
- **Visual Quality:** Maintains good visual fidelity of the original image through cubic Bézier curve reconstruction.


## Methodology
- **Image Blocking:** The image is divided into 24x24 blocks, each containing 25 pixels.
  
  <div align = "center" >
  <img width = "500" alt = "Image Block" src="https://github.com/user-attachments/assets/28f7e72b-0bc4-4f3f-9e36-eaa2e15102d0"/>
  </div>


- **Curve Fitting:** For each block, a cubic Bézier curve is calculated by fitting 4 control points.
 <div align = "center" >
  <img width = "500" alt = "Fitting" src="https://github.com/user-attachments/assets/1cc86328-6fcd-42ef-b04e-f0ff9eb7a3b6"/>
  </div>

- **Compression:** Only the 4 control points (P₀, P₁, P₂, and P₃) are stored instead of the pixel values.

- **Formulation of general equations from Cubic Bezier Curve**
 <div align = "center" >
<img width="350" alt="image" src="https://github.com/user-attachments/assets/d1f6e081-13e0-4419-b1f8-7d9dd61bd8a3">
 </div>
 <br>
   <div align = "center" >
  <img width = "350" alt = "Fitting" src="https://github.com/user-attachments/assets/5feb5492-9560-45f6-ae48-7ce4544991df"/>
  </div>
Decompression: The pixel values are reconstructed using the stored control points and calculated t values.
