# Week 2: Classification, PCA, and Intro to PyTorch

This week will center on classification problems using scikit-learn. Students will also learn about PCA as a tool for visualizing high-dimensional data. They’ll be introduced to workflows using both `sklearn.pipeline` and Prefect. By the end of the week, they'll take their first steps with PyTorch: installing it, connecting to the GPU, and using it as a replacement for NumPy by manipulating arrays (tensors).

## Focus
- Train classification models with scikit-learn
- Evaluate performance with accuracy, precision, recall, and F1
- Use PCA to reduce data to 2D for visualization
- Structure ML code using scikit-learn Pipelines and Prefect Flows
- Begin working with tensors using PyTorch, learn about the power of GPU. 

## Hands-On Activities
- Train kNN, logistic regression, and decision tree models
- Generate and interpret a confusion matrix
- Visualize a higher-dimensional dataset using PCA
- Build a `Pipeline` using `sklearn.pipeline` to chain preprocessing and modeling
- Use Prefect to structure a simple ML workflow
- Install PyTorch locally.
- Use PyTorch to create and manipulate tensors

## Learning Outcomes
By the end of this week, students will be able to:

- Train and evaluate multiple classification models
- Visualize and understand a confusion matrix
- Interpret accuracy, precision, recall, and F1 score
- Understand the purpose of ML workflows and use basic tools like Pipelines and Prefect Flows
- Use PCA to visualize classification boundaries in 2D
- Describe what a tensor is and use PyTorch to explore tensor operations
- Recognize tell-tale signs of overfitting in classification

## Resources

- [scikit-learn Classification Docs](https://scikit-learn.org/stable/supervised_learning.html)
- PCA in scikit-learn
- [PyTorch Tensors Quickstart](https://pytorch.org/tutorials/beginner/introyt/tensors_deeper_tutorial.html)
- [scikit-learn Pipeline Docs](https://scikit-learn.org/stable/modules/generated/sklearn.pipeline.Pipeline.html)
- [Prefect Quickstart](https://docs.prefect.io/latest/)

## Instructor Notes
The main focus will be on building intuitions with traditional classification tasks and metrics (i.e, not neural networks or tensors), and implementing workflows with pipelines. We will introduce PyTorch at the end just to make sure students can install it, and use it as a vehicle like NumPy for manipulating arrays (tensors). 
