# BaggageAI-task
Task:   
Case Study:- Image Processing
You are given two sets of images:- background and threat objects. Background images are the 
background x-ray images of baggage that gets generated after passing through a X-ray machine at 
airport. Threat images are the x-ray images of threats that are prohibited at airport while travelling.
• Your task is to cut the threat objects, scale it down, rotate with 45 degree and paste it 
into the background images using image processing techniques in python.
• Threat objects should be translucent, means it should not look like that it is cut pasted. It 
should look like that the threat was already there in the background images. Translucent 
means the threat objects should have shades of background where it is pasted.
• Threat should not go outside the boundary of the baggage. **difficult**
• If there is any background of threat objects, then it should not be cut pasted into the 
background images, which means while cutting the threat objects, the boundary of a threat 
object should be tight-bound.
You should share the python files which you have written for this task and also the results that are 
generated. You should also provide a proper well-written Readme file which justifies each and 
every algorithms and parameters you used with proper reasoning. You should complete this task 
within two days from the time it is shared with you.

Approach:

Step1: Read the threat image.
Step2: Cnverted the color format in to RGB.
step 3: Cropped the image by using ROI.
step 4: To remove noise from the image, I have used GaussianBlur. I have taken my kernel size here (9,9).
step 5: Scale down image by half by using cv.resize, say this image as scaled_image.
step 6: Read the background image
step 7: select the roi but size should be same as scaled_image.
step 8: Rotated the scaled_image by 45 degree. for this, I have calculated center of the image then used the rotation matrix.
step 9: After rotating the image it has black corners. Now my task is to remove those black corners.
step 10: For this I have drawn the contours and tried to extract the crop the roi from scaled image.(Faced problem)
step 11: After step 10, Masking technique has been used.
