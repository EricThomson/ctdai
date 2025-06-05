# Week 3: Image Classification with PyTorch
This week introduces students to using neural networks for machine vision using PyTorch. The focus is on using pretrained models to make predictions and evaluate network performance. Students will also be introduced to the Hugging Face model hub as a source for vision models.

## Focus
- Use pretrained models for image classification
- Access and run image models from Hugging Face Hub
- Understand how image data is represented and processed
- Learn how CNNs work at a high level
- Visualize predictions and monitor model performance
- Understand class imbalance, precision/recall trade-offs, and bias in ML models

## Hands-On Activities
- Load and run a pretrained model (e.g., ResNet18) from `torchvision.models`
- Load and run a Hugging Face vision model (e.g., ViT) for image classification
- Preprocess and classify images using PyTorch and Hugging Face
- Plot training and validation accuracy/loss
- Read and discuss the Amazon résumé screening case and how bias can emerge from data

## Learning Outcomes
By the end of this week, students will be able to:
- Use a pretrained PyTorch model to classify new images
- Use Hugging Face Hub to explore and run vision models
- Understand the input/output structure of vision models
- Understand different metrics of vision models.
- Describe the basic architecture and function of a CNN
- Identify signs of overfitting from loss/accuracy plots

## Resources
- [torchvision.models documentation](https://pytorch.org/vision/stable/models.html)
- [Hugging Face Vision Models](https://huggingface.co/models?pipeline_tag=image-classification)
- [Intro to hugging face](https://www.youtube.com/watch?v=82Bt4K4YdHg)
- [Reuters article on bias at Amazon](https://www.reuters.com/article/world/insight-amazon-scraps-secret-ai-recruiting-tool-that-showed-bias-against-women-idUSKCN1MK0AG/)

## Instructor Notes
Focus on inference to keep things practical and engaging. Emphasize that most real-world ML use involves using pretrained models. Consider keeping runtime short (e.g., use small datasets and few epochs). 

We'll have to see how many students have GPUs on their local machines -- this may be a limitation -- consider using fashion3k dataset to limit runtime.
