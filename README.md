![image](https://github.com/divyanshujain11/divyanshujain11-python_opencv_imageProcessing/assets/77712311/ae11b02c-9b00-4f9d-8b2d-1afe3846254b)


In this article, you will learn different image filtering techniques using the Python OpenCV. Python OpenCV has several filtering techniques to perform smoothing operations on images. These smoothing techniques are generally used to reduce noise, reduce detail, and so on. These techniques can also be applied to reduce the pixelated effect in low resolution images.

1. Averaging Filter
        import cv2
        import numpy as np
        from matplotlib import pyplot as plt
 
        # image path 
        path = r'blur.jpg'
        # using imread() 
        img = cv2.imread(path)
        im1 = cv2.blur(img,(5,5))
        im2 = cv2.boxFilter(img, -1, (2, 2),normalize=True)
        cv2.imshow('image', np.hstack((im1, im2)))
        cv2.waitKey(0)
        cv2.destroyAllWindows()
        cv2.waitKey(1)

![image](https://github.com/divyanshujain11/divyanshujain11-python_opencv_imageProcessing/assets/77712311/bc068dc8-b182-4115-8022-54873f2287f1)

2. Gaussian Filter
      import cv2
      import numpy
  
      # image path 
      path = r'flower.jpg'

      # using imread()  
      img = cv2.imread(path)
      img = cv2.resize(img,(640,480))
      dst = cv2.GaussianBlur(img,(5,5),cv2.BORDER_DEFAULT) 

      cv2.imshow('image', numpy.hstack((img, dst)))
      cv2.waitKey(0);
      cv2.destroyAllWindows();
      cv2.waitKey(1)


![image](https://github.com/divyanshujain11/divyanshujain11-python_opencv_imageProcessing/assets/77712311/47888b28-c7be-4a4d-a61d-8eefd413a9a7)


