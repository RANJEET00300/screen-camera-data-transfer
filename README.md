Data Transfer Using QR Codes and Video
Overview
This project implements a method to transfer data between devices using QR codes embedded in video frames. It allows for the offline transfer of small to medium-sized files (images, text, etc.) without requiring an internet connection. Data is chunked, encoded into QR codes, compiled into a video, and decoded on the receiving device.

Features
Offline Data Transfer: No need for a network connection.
Cross-Platform: Works with any device equipped with a camera and QR code scanner.
Flexible: Supports text, images, and other small file types.
How It Works
Data Preparation: The data (image, text, etc.) is base64-encoded.
QR Code Generation: The encoded data is split into smaller chunks, each represented by a QR code.
Video Creation: The QR codes are compiled into a video.
Data Capture and Decoding: The receiving device records the video, decodes the QR codes, and reassembles the original data.
Setup
Prerequisites
Python 3.x
Libraries: opencv-python, qrcode, numpy, Pillow
You can install these using:

bash
Copy code
pip install opencv-python qrcode numpy Pillow
Installation
Clone this repository:
bash
Copy code
git clone https://github.com/yourusername/screen-camera-data-transfer.git
Navigate to the project directory:
bash
Copy code
cd scree-camera-data-transfer
Usage
Encode Data into QR Codes:

Run the script to generate QR codes from your input data (e.g., an image).
python
Copy code
python encode_qr_video.py
Decode Data from Video:

Use the receiving device to record the video and decode the QR codes.
python
Copy code
python decode_qr_video.py
Example
Input: An image file is chunked, each chunk encoded into a QR code.
Output: A video containing the QR codes, which is captured and decoded to reassemble the original image.
Limitations
Suitable for small to small-sized files.
Transfer speed is constrained by camera and video playback quality.
Contributing
Feel free to contribute by opening issues or submitting pull requests.

License
This project is licensed under the MIT License.
