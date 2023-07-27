# COMP 6341 - Garbage Classification using Deep Learning

### Team Members
 
- **Kshitij Yerande - 40194579**
- **Siddhartha Jha - 40201472**
- **Adwait R Sambare - 40162664**

### Problem Statement
The goal is to classify garbage images into 6 categories (cardboard, glass, metal, paper, plastic and trash) using Deep learning CNN architectures and feature based models to identify the recyclability status of garbage. We also evaluate the performance of different solution approaches.

### Dataset
The dataset is retrieved from trahsnet repository. 

Link: https://github.com/garythung/trashnet/tree/master/data

### Evaluation metrics

1. Accuracy: It is the most intuitive performance measure, and it is simply the ratio of correctly predicted observation to the total observations.
2. Precision: It is the ratio of the correctly predicted positive observations.
3. Recall: It is the ratio of correctly predicted positive observations to all observations in actual class.
4. F-score: It is the weighted average of precision and recall.

### Solution approaches

- Custom-CNN model: CNN architecture desined from scratch
- ResNet50 (Pre-trained) : Pretrained weights of ImageNet dataset used to train last layer on our dataset.
- SVM with HOG features(histogram of gradients) : HOG feature extracted and trained using SVM

### Project Directory Structure

* **Waste-Item-Classification**
	* data/archive
	* models/
	* metric/
	* Waste Item Classification.ipynb
	
**Project Setup**

1. Install libraries:
	*  Pytorch
	* Numpy
	* matplotlib
	* Scipy
	* Scikit-learn
	* OpenCV
	* pandas
	* tqdm
	* torchviz
	* skimage
2. Download the data from the kaggle repository. Place all the classes in the following format.  
	* data
		* /archive
			* /cardboard
				* 1.png
			* /plastic
				* 2.png
3. Create the empty folders as per directory structure
4. Run the notebook

### Results

| Model/Metric | Accuracy | F-Socre | Recall | Precision |
| --- | --- | --- | --- | --- |
| ResNet50(Pretrained) | 80.200 | 0.793 | 0.788 | 0.802 |
| Custom-CNN |  69.000 | 0.686 | 0.686 | 0.690 |
| SVM with HOG features | 56.4 | 0.535 | 0.526 | 0.618 |
