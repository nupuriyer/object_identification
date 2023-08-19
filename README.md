# object_identification
The Candy Counter project utilizes Hugging Face’s DETR object identification model and fine tunes it to a custom dataset of different types of candy images. The project uses a few-shot learning approach as the final results are obtained using a small dataset for training (~20 images)
The code flow can be summarized as follows:
- Labeling the images: In order to label the different types of candy in a picture, we make use of Label Studio.
  - These images can be found in the "train" and "test" folders of the repository.
  - Further information for these elements can be found in their commit messages
- Preprocessing: Since we are fine-tuning to an existing model, we introduce a preprocessing phase to ensure that the input file format matches the input requirements of the DETR model. We will also ensure folder structures are as required for the model to process images correctly
  - The repository root folder contains the result JSON file meant to be inputted in the notebook along with the images.
  - Also note the structure for the images should ensure that the folder name specified in the load_dataset method should be the folder name for where images are stored. Further, these folders should include the metadata file created for the images.
  - Further information for these elements can be found in their commit messages
- Fitting & Evaluation: Finally, this phase ensures that we find the best possible hyperparameters to maximize model performance, i.e., ensure high accuracy while trying to minimize resource usage to prioritize efficiency.
