# Workshop 3 : Canny Edge Detection

## Developed by
Name : SUJITH A

Register No : 212224230278

##  AIM
To develop a Python program using OpenCV to detect edges in a grayscale image using the Canny Edge Detection technique.

## ALGORITHM
1. Import the required libraries, OpenCV and Matplotlib.
2. Read the input image in grayscale format using cv2.imread().
3. Apply Gaussian Blur to the image to remove noise.
4. Apply the Canny Edge Detection algorithm using lower and upper threshold values of 50 and 150.
5. Display the original grayscale image.
6. Display the detected edges using Matplotlib.
7. Compare the original image with the edge-detected image.

## PROCEDURE
1. Open Python IDE or Jupyter Notebook.
2. Import the OpenCV and Matplotlib libraries.
3. Load the input image from the specified file path.
4. Convert the image into grayscale format.
5. Apply Gaussian filtering with a kernel size of (5,5) to reduce noise.
6. Perform Canny Edge Detection with threshold values 50 and 150.
7. Display both the original image and detected edge image using subplots.
8. Observe the edges detected in the output image.

## PROGRAM
```python
import cv2
import matplotlib.pyplot as plt

img = cv2.imread(
    r"C:\Users\ADMIN\Downloads\ex.png",
    cv2.IMREAD_GRAYSCALE
)

blurred = cv2.GaussianBlur(img, (5,5), 0)

edges = cv2.Canny(blurred, 50, 150)

plt.figure(figsize=(10,5))

plt.subplot(121)
plt.imshow(img, cmap='gray')
plt.title('Original Image')
plt.axis('off')

plt.subplot(122)
plt.imshow(edges, cmap='gray')
plt.title('Detected Edges')
plt.axis('off')

plt.show()
```

## Output

<img width="776" height="426" alt="download" src="https://github.com/user-attachments/assets/a04d1b50-cd8a-45d9-8a1c-b95a2902db4f" />


## Result
Thus, the Python program was successfully executed using OpenCV to detect edges in a grayscale image using the Canny Edge Detection technique. Gaussian Blur was applied to reduce noise, and the edges were successfully detected and displayed.
