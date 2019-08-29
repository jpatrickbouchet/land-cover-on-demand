# land-cover-on-demand
End-to-end pipeline to train and serve a land segmentation ML model for a chosen area in Europe. The ultimate goal being to observe land use evolution on a more regular basis than manual inventory.

- Corine Land Cover 2018 is used as the ground truth for training
- Satellite patches are generated with Google Earth Engine Python API
- Data is preprocessed with Geopandas and Tensorflow tf.data API
- ML model is a Unet with a pre-trained Resnet50 as encoder using Keras
- Serving is done via Google AI Platform with both batch and online prediction support

**NOTE:**  
My objective for this project was more to put together a working and effective pipeline than reaching the best accuracy with the model.

I generated a pretty small dataset to keep things fast and didn't perform any data augmentation. I also didn't spend much time experimenting with hyperparameters.

The result is still decent enough to confirm that the approach works.
(Train accuracy: 97.21% / Validation accuracy: 67.18%)
