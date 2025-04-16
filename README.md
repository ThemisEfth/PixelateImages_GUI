Pixelate ROI in Image

A simple Python script that allows users to manually select multiple regions of interest (ROIs) within an image and pixelate those areas. Useful for obscuring sensitive information like faces, license plates, or private details.

📦 Requirements
	•	Python 3.x
	•	OpenCV (cv2)
	•	NumPy

You can install the required packages using:

pip install opencv-python numpy

📄 How It Works
	1.	Load an image — the script loads an image from a user-specified path.
	2.	Select ROIs — you can interactively select one or more rectangular regions by dragging the mouse.
	•	Press ENTER or SPACE to confirm a selection.
	•	Press ESC or draw a zero-size rectangle to finish.
	3.	Pixelate selected areas — the selected ROIs are pixelated with a configurable pixelation strength.
	4.	Save the result — the modified image is saved to a user-specified output path.

🖥️ Usage
	1.	Set your input and output image paths

Edit these lines in the script:

image_path = 'path/to/your/image.jpg'
output_path = 'path/to/save/pixelated_image.jpg'

	2.	Run the script

python pixelate_roi.py

	3.	Interact with the selection window
	•	Draw a rectangle around each region you want to pixelate.
	•	Confirm each selection with ENTER or SPACE.
	•	Press ESC or draw a rectangle with zero width/height to finish.
	4.	Find your pixelated image
	•	The pixelated image will be saved to the specified output_path.

🔧 Configuration

You can adjust the pixelation strength by changing the pixelation_size parameter within the pixelate_region function call. Lower values result in a stronger pixelation effect.

pixelation_size=10

📑 Notes
	•	The script uses OpenCV’s selectROI tool for manual ROI selection.
	•	The output image will overwrite any existing file at the same output_path.
	•	Make sure your image paths are correct and accessible.
