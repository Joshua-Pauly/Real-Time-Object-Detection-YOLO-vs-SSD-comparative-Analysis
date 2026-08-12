Project Title: Comparison Between YOLO and SSD Algorithms for Video Real Time Object Detection

Team Members: Dagmar Mojena Carrazana, Joshua Pauly, Josue Perez Gomez

Abstract 

This capstone project has the purpose of analyzing and comparing two popular image-based object detection algorithms. The You Only Look Once (YOLO) and the Single-Shot Detector (SSD) algorithms. In contrast to other popular object detection algorithms, the SDD and YOLO object detection algorithms are newer and are designed for the purpose of real-time object detection, thus faster in evaluating input image. The team worked on comparing the performance of both object detection algorithms using an open-source data repository of video recordings from car dashcam videos called Agroverse-HD on Kaggle. On top of evaluating the performance, this project has the additional purpose of introducing, explaining and showing possible applications of both the YOLO and SSD object detection models. 
The team used existing pre-trained and open-source models. The YOLO model from a Python package called Utralytics and the SSD model from PyTorch. Both models were then fined tuned with the training section of the Agroverse-HD data for a fair comparison. Additionally, the data was also augmented with rotations transformations for increased performance. Some of the important metrics the team used to compare both models included accuracy, recall, precision and run time. We show under which hyperparameter values the models best perform and a demonstration of how the models enclose the desired class objects with a bounding box. 
With the results and interpretation of the comparison between both object detection models, one can more easily pick a model that best fits their requirements, for runtime and accuracy.

-------------------------------------------------------------------------------------------------------------

Files included in the Code folder:

NOTE: Dataset not included because because dataset was too large. see step 1 of execution section below.

1.Data_Preprocessing_Team_8.ipynb – Jupyter notebook containing the code to explore and preprocess data up to augmentation.
2.YOLO_Notebook_Team_8.ipynb - Jupyter notebook containing the code to train and evaluate the YOLOv11 model as well as code for inference using the finetuned model. 
3.SSD_Notebook_Team_8.ipynb - Jupyter notebook containing the code to train and evaluate the SSD model as well as code for inference using the finetuned model.
4.bal_toYOLO.yaml – YAML file needed for the yolo model. It contains information with paths as well as class names.
5.requirements.txt – Text file containing all the libraries and their versions that need to be installed into the environment to run the code in the notebooks.
6.final_yolo_model.pt – The finetuned YOLO model that is used for inference.
7.ssd_final_model.pth – The finetuned SSD model used by the SSD notebook.
8.test_pic.jpg -  Picture to be used for inference by both model notebooks.
9.test_video.mp4 – Video to be used for inference by both model notebooks.
10.yolo_output_video.mp4 - Inference video annotated by finetuned YOLO model. 
11.ssd_output_video.mp4 - Inference video annotated by the finetuned SSD model.

--------------------------------------------------------------------------------------------------------------

Installation 
1.Place all the above-mentioned files in a working directory.
2.Create a Jupyter compatible environment with python 3.11.9 or above. python 3.11.9 and 3.11.12 were used effectively.
  
3.Install the required dependencies by running “pip install -r requirements.txt” on the terminal or 
“! pip install -r requirements.txt” on any of the notebooks.

-------------------------------------------------------------------------------------------------------------
Execution Instructions

-If only using the models for inference on test images and videos, see step 7.

-To run the entire project, including data processing, training and validation follow these steps:

1.Create a folder in the working directory named “datasets”. Download the Agroverse dataset from: https://www.kaggle.com/datasets/mtlics/argoversehd and extract into the datasets folder. The data was not uploaded because the file is too large for submission. 

2.Start by opening the Data_Preprocessing.ipynb notebook. The notebook can be executed if the requirements have been installed. If using google colab, uncomment the necessary lines of code.

3.The first section of the notebook is exploration analysis. The second section, which is labeled, is for data augmentation and balancing. The entire dataset is copied over into a new dataset folder called balanced_Agroverse. Then there are various argumentations applied. More details inside the notebook.

4.After the balanced_Agroverse dataset is made the other two notebooks can be run to train the models.

5.Open the YOLO_Notebook_Team_8.ipynb notebook and run all of the cells. The notebook includes the code to make the “labels”, which are the annotations in the format that the YOLO model accepts. This is followed by the following sections: training, evaluation and inference. 

6.Open the SSD_Notebook_Team_8.ipynb notebook and run all of the cells. The notebook includes the code to make custom datasets, loading the data. This is followed by the following sections: training, evaluation and inference. 

7.On both notebooks the inference section is already set up to load their corresponding finetuned model. Make sure to run the imports at the top of the notebooks. 

8.The test_pic.jpg file is used for a single picture inference by both notebooks and the test_video.mp4 is used for inference on video. Other pictures and videos can be used by updating the path.
