
Salt and Pepper Noise Addition to Color Images
This project demonstrates how to add Salt-and-Pepper noise to a color image using Python. The code allows you to increase or decrease the level of noise in the image by adjusting the salt and pepper probabilities.

Table of Contents
Overview

Requirements

Code Explanation

How to Run

Adjusting Noise Levels

Overview
In digital image processing, Salt-and-Pepper noise is a type of noise where some pixels in the image are set to black (pepper) or white (salt). This is typically used to test the effectiveness of noise removal algorithms.

This script:

Loads a color image.

Adds Salt-and-Pepper noise based on configurable probabilities.

Displays both the original and noisy image side by side.

Requirements
To run the code, you need the following Python libraries:

OpenCV for image processing.

NumPy for array manipulation.

Matplotlib for displaying the images.

You can install the necessary libraries using pip:

bash
Copy
Edit
pip install opencv-python numpy matplotlib
Code Explanation
The code performs the following steps:

Load Image: The image is loaded using cv2.imread().

Convert to RGB: OpenCV loads images in BGR format by default. The image is converted to RGB for proper visualization using cv2.cvtColor().

Add Salt-and-Pepper Noise:

Salt Noise: White pixels (255) are added randomly.

Pepper Noise: Black pixels (0) are added randomly.

Display Images: Both the original and noisy images are displayed side by side using matplotlib.

How to Run
Clone or download this repository.

Place the image you want to add noise to in the same directory or provide the full path to the image in the code.

Run the script using Jupyter Notebook or any Python IDE.

Example command to run in terminal:

bash
Copy
Edit
python add_noise.py
This will display the original image on the left and the noisy image with Salt-and-Pepper noise on the right.

Adjusting Noise Levels
The Salt-and-Pepper noise level is controlled by two parameters: salt_prob and pepper_prob. These represent the probability that each pixel will be set to salt (white) or pepper (black), respectively.

salt_prob: Probability of adding salt (white noise).

pepper_prob: Probability of adding pepper (black noise).

Example Code:
python
Copy
Edit
salt_prob = 0.2  # 20% of the pixels will be salt (white)
pepper_prob = 0.2  # 20% of the pixels will be pepper (black)
To increase the noise:
Increase the probabilities. For instance:

python
Copy
Edit
salt_prob = 0.5  # 50% of the pixels will be salt (white)
pepper_prob = 0.5  # 50% of the pixels will be pepper (black)
To decrease the noise:
Reduce the probabilities. For instance:

python
Copy
Edit
salt_prob = 0.05  # 5% of the pixels will be salt (white)
pepper_prob = 0.05  # 5% of the pixels will be pepper (black)
You can experiment with these values to control how much noise is added to your image.

Example Output
Original Image:

Noisy Image:

License
This project is open-source and can be used for educational purposes. Feel free to modify and experiment with the code.
