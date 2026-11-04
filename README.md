# Implementation-of-Filters

# **Name:** KAMLESH P


# **Register Number:** 212225240067 

## Aim

To implement filters for smoothing and sharpening images in the spatial domain.

## Software Required

- Anaconda - Python 3.7
- OpenCV
- NumPy
- Matplotlib

## Algorithm

### Step 1
Import the required libraries.

### Step 2
Read the image and convert it from BGR to RGB.

### Step 3
Apply the required smoothing and sharpening filters to the image separately.

### Step 4
Plot and display the original and filtered images using `matplotlib.pyplot`.

### Step 5
End the program.

## Program

**Developed By:** SHRIVARSHAN P G

**Register Number:** 212225240146

## 1. Smoothing Filters

### i) Using Averaging Filter

```python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("sv.jpeg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()
```

### ii) Using Weighted Averaging Filter

```python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
image3=cv2.filter2D(image2,-1,kernel1)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show())
```

### iii) Using Gaussian Filter

```python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```

### iv) Using Median Filter

```python
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```

## 2. Sharpening Filters

### i) Using Laplacian Linear Kernel

```python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```

### ii) Using Laplacian Operator

```python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()
```

## Output

### 1. Smoothing Filters

#### i) Using Averaging Filter

<img width="822" height="544" alt="Screenshot 2026-11-04 113616" src="https://github.com/user-attachments/assets/87108d8f-d696-4802-b05a-8fa02e439776" />


#### ii) Using Weighted Averaging Filter

<img width="611" height="393" alt="Screenshot 2026-11-04 113644" src="https://github.com/user-attachments/assets/a513a5ef-8f83-472d-8bc7-1fa1e95691fb" />


#### iii) Using Gaussian Filter

<img width="578" height="375" alt="Screenshot 2026-11-04 113711" src="https://github.com/user-attachments/assets/f0031ef0-7fcb-4e01-924d-084344f04964" />


#### iv) Using Median Filter

<img width="817" height="528" alt="Screenshot 2026-11-04 113737" src="https://github.com/user-attachments/assets/97d59a09-fda3-46e0-a48f-b1ab97eb7133" />


### 2. Sharpening Filters

#### i) Using Laplacian Kernel

<img width="597" height="403" alt="Screenshot 2026-11-04 113756" src="https://github.com/user-attachments/assets/ab9e072d-b2a4-4539-a770-2c2def70c869" />


#### ii) Using Laplacian Operator

<img width="594" height="381" alt="Screenshot 2026-11-04 113811" src="https://github.com/user-attachments/assets/97360a20-8473-408b-84e6-fcdbf9ebd47c" />


## Result

Thus, filters were implemented for smoothing and sharpening images in the spatial domain using OpenCV and Python.
