# Transfer Learning for Skin Cancer Classification using AlexNet and ResNet50

This project applies the concept of Transfer Learning for the classification of different types of skin cancer. Two pre-trained networks, AlexNet and ResNet50, have been utilized for this purpose.

The dataset used for this project is Skin Cancer MNIST: HAM10000, a large collection of multi-source dermatoscopic images of common pigmented skin lesions. 

The main goals of this project are not only to accurately classify the different types of skin cancer but also to gain insights into the training process. It aims to make the machine learning process a bit more transparent and explainable.

## Code Organization

The code is divided into two parts: 

1. `generate_transfer_data.ipynb`: This notebook is used to train the model and save the training process. It stores relevant data after each training epoch.

2. `generate_altair_plot.ipynb`: This notebook is used to load all the dataframes, append them and visualize the results.

### Data after each Epoch

In the `generated_df_data` folder, a comprehensive record of the following parameters is stored separately for each model after every epoch:

- `name`: The name of the model.
- `epoch`: The current epoch number.
- `lr`: The learning rate used in the current epoch.
- `classifier.weight`: The weights of the classifier layer of the model.
- `classifier.bias`: The biases of the classifier layer of the model.
- `confusion_matrix`: The confusion matrix of the model's predictions in the current epoch.
- `train_errs`: Training error of the model in the current epoch.
- `valid_errs`: Validation error of the model in the current epoch.
- `used_data_augmentation`: Boolean flag to indicate if data augmentation was used in the training process.

## Visualization and Plots

In the `generate_altair_plot.ipynb` notebook, all the saved dataframes are loaded and appended to make a comprehensive dataframe. This dataframe is then used to generate a series of plots, which help in visualizing the training process of the models. 

The plots include information such as how the learning rate, training error, and validation error varied with each epoch. They also visualize the effect of using data augmentation during training.

Some of the plots generated in this notebook are saved in the `altair_plots` folder for further reference.

## Getting Started

1. Run `generate_transfer_data.ipynb` to train the model and save the dataframe after each epoch.
2. Run `generate_altair_plot.ipynb` to load all the saved dataframes and generate the plots.

Enjoy exploring the project!
