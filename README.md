# DeepLabCut Mouse Location Prediction

This repository contains the code and report for the assignment on DeepLabCut, a toolbox for training deep neural networks to precisely track user-defined features. The goal of the assignment was to train a model to predict the location of a mouse based on annotated joint positions.

## Introduction
DeepLabCut is an open-source toolbox that utilizes a state-of-the-art animal pose estimation algorithm. It allows for the training of a deep neural network using limited training data to accurately track user-defined features. In this assignment, we focused on predicting the location of a mouse using DeepLabCut.

## Problem Statement
The task was to collect annotated joint positions of a mouse, including the nose, ears, hips, tail base, and tail end, from a set of approximately 125 photos. The goal was to train a model that could predict the mouse's location given the annotated joint positions.

## Approach
The project was divided into two main sections. In the first part, we collected and annotated the mouse joint positions using the DeepLabCut library and exported the data as a CSV file. In the second part, we built deep learning models to predict the mouse location based on the annotated joint positions. The model was evaluated using test data, and the results were analyzed.

## Project Structure
The project is structured as follows:

1. Data set annotations using DeepLabCut-master tool
2. Data set cleaning
3. Building deep learning model architectures
4. Evaluation of the model

## Data Preprocessing
The annotated data contained 128 rows and 39 columns. The preprocessing phase involved excluding unnecessary rows, dividing the data into separate sets for each mouse, and calculating the center points of the annotated joints. The data columns were then renamed for better understanding.

## Data Analysis
The dataset consisted of 125 images, with a total of 198 annotated mouse instances.

## ML Model Structure
The data was split into training and test sets using a 70-30 split ratio. A neural network model was utilized for predicting the mouse location. The model consisted of three layers, including an input layer with 14 nodes and a relu activation function.

## Evaluation
The model's performance was evaluated using various metrics, and the results were analyzed to assess the model's effectiveness.

## Conclusion
The model showed some overfitting, indicating a need for further processing of both the model and the data. Additional training and testing data could improve the model's performance.

## Future Scope
To enhance the model, it is recommended to address cases where certain mouse body parts were hidden during annotation. Making educated guesses about the hidden body parts and including them in the annotation process could generate more data and improve the model's accuracy.

## Instructions for Reproducing Results
To reproduce the results, follow these steps:
1. Use the ML-Assignment 3.ipynb notebook provided in the repository.
2. Run the first code block, which defines the `viz(history)` function.
3. Load the annotated CSV file (A204914651_CollectedData_annotation.csv).
4. Run all the code blocks in the notebook.
5. The weights are saved and can be found in the attached JSON file for achieving similar accuracy results.

For detailed implementation and code, please refer to the [ML-DeeplabCut](https://github.com/Amoghkori/ML-DeeplabCut) repository.

---

Submitted by: Amogh A Kori  
Instructed by: Prof. Yan Yan
