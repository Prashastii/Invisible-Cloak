Invisible Cloak Effect using OpenCV

This code implements an "Invisible Cloak" effect using OpenCV, a computer vision library. The effect allows a user to disappear from a live video feed by replacing their image with a background image.

How it works

*Background Capture*: The code captures a background image by taking the median of 30 frames from the camera feed. This helps to reduce noise and create a stable background image.
*Color Detection*: The code detects the color blue (within a specified range) in each frame of the video feed. This is done by converting the frame to HSV (Hue, Saturation, Value) color space and applying a mask to isolate the blue color.
*Mask Refining*: The mask is refined using morphological operations (opening and dilation) to remove noise and fill in gaps.
*Cloak Effec*t: The cloak effect is applied by combining the original frame with the background image, using the refined mask to determine which pixels to replace.
*Display*: The resulting frame is displayed in a window, creating the illusion of an invisible cloak.
Usage

Run the code using Python (e.g., python invisible_cloak.py).
The code will capture a background image and then start the main loop.
Move out of the frame to capture a clean background image.
Once the background image is captured, move back into the frame and the cloak effect will be applied.
Press 'q' to quit the program.
Dependencies

OpenCV (cv2)
NumPy (np)
Note: This code assumes that the user is wearing a blue-colored cloth or object to be detected as the "cloak". The color range can be adjusted by modifying the lower_blue and upper_blue arrays.
