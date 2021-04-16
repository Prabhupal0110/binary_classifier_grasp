# binary_classifier_grasp
Binary Image Classifier Using Pytorch for Examining Robotic Grasp Success
## 1.	Model description
Net(
  (block1): Sequential(
    (0): Conv2d(3, 256, kernel_size=(5, 5), stride=(1, 1), padding=(2, 2))
    (1): BatchNorm2d(256, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
    (2): ReLU()
    (3): Dropout2d(p=0.1)
  )
  (block2): Sequential(
    (0): Conv2d(256, 128, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1))
    (1): BatchNorm2d(128, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
    (2): ReLU()
    (3): Dropout2d(p=0.1)
  )
  (block3): Sequential(
    (0): Conv2d(128, 64, kernel_size=(3, 3), stride=(1, 1), padding=(1, 1))
    (1): BatchNorm2d(64, eps=1e-05, momentum=0.1, affine=True, track_running_stats=True)
    (2): ReLU()
    (3): Dropout2d(p=0.1)
  )
  (lastcnn): Conv2d(64, 2, kernel_size=(56, 56), stride=(1, 1))
  (maxpool): MaxPool2d(kernel_size=2, stride=2, padding=0, dilation=1, ceil_mode=False)
)










## 2.	 Data Description
Images for each class (Successful and Unsuccessful Grasp) were extracted from videos of an Allegro robotic hand trying to grasp an object. These were used to train this classifier.
Data samples
 
Successful

 
Unsuccessful

The sample size for both class was increased to 1000 using below augmentation function:
 


3. Training reports
•	2000 images were used to train the model.
•	After each epoch class accuracy was obtained using the same images again (2000)
•	Test accuracy was obtained after every second epoch using 28 (Not Successful: 13 and Successful: 15) new images which were not used in the training and validation.
•	The model was trained for 10 epochs and following results were obtained:
Loss	Validation Accuracy	Testing Accuracy
Epoch: 1 Loss:  123.70484164357185
Epoch: 2 Loss:  61.192153841257095
Epoch: 3 Loss: 26.804708188399673
Epoch: 4 Loss: 11.293394926236942
Epoch: 5 Loss: 4.254946916596964
Epoch: 6 Loss: 1.8401405285694636
Epoch: 7 Loss: 1.6579175041406415
Epoch: 8 Loss: 0.9414917040267028
Epoch: 9 Loss: 0.6904916932107881
Epoch: 10 Loss: 0.9886632559646387	After 2 Epochs:
Accuracy of Not_Success : 100 %
Accuracy of Success: 70 %

After 4 Epochs:
Accuracy of Not_Success: 98 %
Accuracy of Success: 96 %

After 6 Epochs:
Accuracy of Not_Success: 93 %
Accuracy of Success: 100 %

After 8 Epochs:
Accuracy of Not_Success: 100 %
Accuracy of Success: 100 %

After 10 Epochs:
Accuracy of Not_Success: 98 %
Accuracy of Success: 100 %

	After 2 Epochs:
Not Success:  13/13 = 1
Success : 13/15 = 0.866

After 4 Epochs:
Not Success:  11/13 = 0.846
Success : 15/15 = 1

After 6 Epochs:
Not Success:  11/13 = 0.846
Success : 15/15 = 1

After 8 Epochs:
Not Success:  12/13 = 0.92
Success : 15/15 = 1

After 10 Epochs:
Not Success:  12/13 = 0.92
Success : 15/15 = 1

3.	Conclusion
Though model started to have a good validation and test accuracy after 2nd epoch, but it was trained till 10th epoch. Also to keep monitor if model is being overfitted, after every 2nd epoch it was tested with random images which were not used for the training and accordingly test accuracy was calculated.
 
 

 
 

Wrongly classified image:
 






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


