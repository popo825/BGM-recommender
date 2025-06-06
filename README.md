# BGM-recommender
# Dependencies
* Python 3.10

# Installation
To install the required packages, run the following command:
```pip
pip install -r requirements.txt
```
This command will install the necessary Python packages specified in the requirements.txt file.

# Training
## 1. Download the Dataset
Dowmload the UTKFace dataset from [here](https://www.kaggle.com/datasets/jangedoo/utkface-new).

Move the "UTKFace" folder to the "data" directory.

## 2. Preprocess the Dataset
To preprocess the dataset, run the following command:
```python
python preprocess.py
```
You can limit the number of photos by adjusting the "num_photos" parameter.

## 3. Train the Model
To train the face classification model, run the following command:
```python
python train_age.py
python train_gender.py
```
You can download the trained model from [here](https://drive.google.com/drive/folders/146qbJXDoewV6p73qA4vFUPLgEmL7svVi?usp=drive_link) if you want it.

# Usage
Before testing the model, we must first crop the face.

1. Place the photo in the "input" folder and execute the following command:
```python
python face_detect.py
```
The pretrained model of face detection is from [spmallick/learnopencv](https://github.com/spmallick/learnopencv/tree/master/AgeGender).

2. Once the face is cropped, you'll find it in the "crop_input" folder.

3. Run the following code to obtain the predicted gender and age, along with recommended music:
```python
python test.py
```


