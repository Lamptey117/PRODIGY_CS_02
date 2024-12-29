# PRODIGY_CS_02

Image Encryption Tool

Project Overview

This project implements a simple image encryption and decryption tool using pixel manipulation. The tool performs basic operations, such as XOR, to modify pixel values and obscure image data for educational purposes.

Features

Encrypts image files by manipulating pixel values.

Decrypts encrypted images using the same key.

Supports .png, .jpg, and other common image formats.

Prerequisites

Python 3.x installed on your system.

Ensure the Pillow library is installed to handle image processing.

Required Libraries

Pillow

Installation: Run the following command:

pip install pillow

How to Run

Clone or download this repository to your local machine.

Install the required library (Pillow).

Place the image to be encrypted in the same directory as the script.

Run the script using:

python image_encryption.py

Follow the on-screen prompts to:

Select encryption or decryption mode.

Provide the image file path.

Enter an encryption/decryption key.

File Structure

.
├── image_encryption.py   # Python script for image encryption
├── encrypted_image.png   # Encrypted output file (auto-generated)
├── README.md             # Project documentation
└── example_image.png     # Example input image

Code Explanation

image_encryption.py

This script uses the Pillow library to manipulate image pixel values:

encrypt_image(): Encrypts the image by applying an XOR operation to each pixel.

decrypt_image(): Reverses the encryption using the same XOR operation and key.

Example Code Snippet

from PIL import Image

def encrypt_image(image_path, key):
    img = Image.open(image_path)
    pixels = img.load()

    for i in range(img.width):
        for j in range(img.height):
            r, g, b = pixels[i, j]
            pixels[i, j] = (r ^ key, g ^ key, b ^ key)

    img.save("encrypted_image.png")

Ethical Guidelines

This tool is intended for educational purposes only. It demonstrates basic image encryption concepts and should not be used for securing sensitive information.

Legal Disclaimer

The authors are not responsible for any misuse of this tool. Always use it responsibly and in compliance with applicable laws.

References

Pillow Documentation

Image Processing Basics

Future Enhancements

Implement stronger encryption algorithms, such as AES.

Add support for batch image encryption.

Create a graphical user interface (GUI) for ease of use.

