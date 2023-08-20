# Object Identification: the Candy Counter project

![image](https://github.com/nupuriyer/object_identification/assets/69424215/f290eadf-cf08-45e2-97b1-6cba58c0ad0e)

The Candy Counter project utilizes Hugging Face’s DETR object identification model and fine tunes it to a custom dataset of different types of candy images. The project uses a few-shot learning approach as the final results are obtained using a small dataset for training (~20 images)

Object detection, a task in computer vision, allows users to create machine systems that can identify not only the number of different objects in a picture frame, but also segregate between the different types of these objects. For instance, such models can be used to either identify the different obstacles in a track or the different types of elements such as vehicles, street signs, etc in a frame. 

The major problem when training object detectors is the availability of data. In order to specify different types of elements in a frame, the model needs access to a repository of pictures of these elements in different lighting, different backgrounds and other such settings. Since it isn’t feasible to have access to such data for custom projects, we make use of models already trained on a wide variety of object detection tasks.

Fine-tuning and transfer learning allow users to utilize pre-existing model architecture and customize it to better fit the requirements of the user.

The Candy counter project uses this methodology by fine-tuning the DETR model by Huggingface. The project is meant to demonstrate the scalability of the model and allow accurate object detection using a handful of example pictures.

The entire project can be broken down into three phases:



1. **Labeling the images:** In order to label the different types of candy in a picture, we make use of Label Studio. Since the candy image dataset is small, the labeling process for this project is manual.
2. **Preprocessing:** Since we are fine-tuning to an existing model, we introduce a preprocessing phase to ensure that the input file format matches the input requirements of the DETR model. We will also ensure folder structures are as required for the model to process images correctly
3. **Fitting & Evaluation:** Finally, this phase ensures that we find the best possible hyperparameters to maximize model performance, i.e., ensure high accuracy while trying to minimize resource usage to prioritize efficiency.
