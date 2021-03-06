# Binary Image Classifier Using Pytorch for Examining Robotic Grasp Success
Binary Image Classifier Using Pytorch for Examining Robotic Grasp Success
## 1.	Model description

![image](https://user-images.githubusercontent.com/70087843/114982429-ace00e00-9e4c-11eb-99b9-8a3d2c17107e.png)










## 2.	 Data Description
Images for each class (Successful and Unsuccessful Grasp) were extracted from videos of an Allegro robotic hand trying to grasp an object. These were used to train this classifier.
Data samples

![image](https://user-images.githubusercontent.com/70087843/114982614-e87ad800-9e4c-11eb-9d35-ef937b81bbcb.png)

Successful


![image](https://user-images.githubusercontent.com/70087843/114982708-07796a00-9e4d-11eb-95c8-ac393174785b.png)
 
Unsuccessful

The sample size for both class was increased to 1000 using below augmentation function:

![image](https://user-images.githubusercontent.com/70087843/114982889-37287200-9e4d-11eb-985e-f0c60449c859.png)

 


## 3. Training reports
•	2000 images were used to train the model.

•	After each epoch class accuracy was obtained using the same images again (2000).

•	Test accuracy was obtained after every second epoch using 28 (Not Successful: 13 and Successful: 15) new images which were not used in the training and validation.

•	The model was trained for 10 epochs and following results were obtained:

![image](https://user-images.githubusercontent.com/70087843/114981832-d3ea1000-9e4b-11eb-9cea-37554884e576.png)

## 4.	Conclusion
Though model started to have a good validation and test accuracy after 2nd epoch, but it was trained till 10th epoch. Also to keep monitor if model is being overfitted, after every 2nd epoch it was tested with random images which were not used for the training and accordingly test accuracy was calculated.
 
![image](https://user-images.githubusercontent.com/70087843/114983000-545d4080-9e4d-11eb-97f9-21043cd84b7d.png)



![image](https://user-images.githubusercontent.com/70087843/114983033-5fb06c00-9e4d-11eb-85ee-31ad8f6ab25f.png)

 



Files:
DATASET:
Extracted Images (Successful): https://drive.google.com/drive/folders/1oUyCLogBPbyN6Ju7gkbbHfY4AuJ12HSo?usp=sharing

Extracted Images (Unsuccessful):
https://drive.google.com/drive/folders/1HwL92VNdifV6ecPpF3O3ChKgq_rMCULj?usp=sharing

MODELS:
After 2 epochs:
https://drive.google.com/file/d/1aq_r2KDCvS0ipiha8t0o6aW7JtLcGkg4/view?usp=sharing

After 4 epochs:
https://drive.google.com/file/d/1YOB5UIpeWq5F4Iy7IAjNHNscsxoKinPI/view?usp=sharing

After 6 epochs:
https://drive.google.com/file/d/1-6P8prjIuyHBWPg7tk5WwNnZxBbtoNSv/view?usp=sharing

After 8 epochs:
https://drive.google.com/file/d/1-6mVbQldtyca2DDEG9fhbFO1m5Q_hXG7/view?usp=sharing

After 10 epochs:
https://drive.google.com/file/d/1-7XCkNyvtQA4MQ_UCatlkZmqhTRbE1aB/view?usp=sharing

IMAGE SAMPLES FOR TEST:
https://drive.google.com/drive/folders/1blB7_SYCXL0S5JXrheKZ_y7Xmv7ukxfx?usp=sharing


