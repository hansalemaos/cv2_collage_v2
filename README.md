# Creates a collage from images with OpenCV

## pip install cv2-collage-v2 

# Tested against Windows 10 / Python 3.10 / Anaconda

## How to use it

```python
from cv2_collage_v2 import create_collage_v2
import os
import cv2
folder=r'C:\Users\hansc\Downloads\bd'
allpics =[]
for f in os.listdir(folder):
    try:
        allpics.append(cv2.imread(os.path.join(folder,f)))
    except Exception as fe:
        print(fe)
        continue

collage=create_collage_v2(allpics,maxwidth = 1500,heightdiv=16,widthdiv=5,background=(0, 0, 0),save_path='e:\\nyhctest.png',)

cv2.imshow('Collage', collage)
cv2.waitKey(0)
cv2.destroyAllWindows()



    Args:
        lst (list|tuple): A list or tuple of images - allowed: [file paths, base64, bytes, PIL, urls, np.array].
        maxwidth (int, optional): The maximum width of the collage. Defaults to 1080.
        heightdiv (int, optional): The height division factor. Defaults to 6.
        widthdiv (int, optional): The width division factor. Defaults to 2.
        background (tuple, optional): The background color of the collage. Defaults to (0, 0, 0).
        save_path (str|None, optional): The file path to save the collage. Defaults to None.

    Returns:
        np.array: A NumPy array representing the collage image.

```


![](https://github.com/hansalemaos/screenshots/blob/main/nyhctest.png?raw=true)

