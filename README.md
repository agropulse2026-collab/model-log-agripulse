# model-log-agropluse
A repo to log and track the progress model training

PlantVillage dataset (Was cloned from github since cloning from huggingface had some complications)
        ↓
Inspect dataset (The dataset has 54306 images of 38 different plant disease)
        ↓
Use COLOR images (The images in the dataset are RGB similar to the images the users will upload)
        ↓
Create train/validation split (The dataset was split into two parts 80:20 for training and validation)
        ↓
Build TensorFlow datasets (The dataset was split into two so the model won't just memorise the training images)
        ↓
Resize images to 224×224 (MobileNetV2 used here for transfer learning and MobileNetV2 normally uses images of resolution 224x224)
        ↓
MobileNetV2 preprocessing (The imbalances in the dataset are fixed using normalised weights and the data is augmentation)
        ↓
Pilot training (A pilot training was done to check whether the model would train and estimate total training time for 10 epcoh)
        ↓
Estimate full training time (estimated time for 1 epoch was 100sec so it would take 15min to train the full initial model)
        ↓
Train initial model (The inital model was trained ,performance data can be found in model_v1 folder)
        ↓
Evaluate (performance data can be found in model_v1 folder, to improve to model's accuracy futher fine tuning was done)
        ↓
Fine-tune (Last 30 layers of the model was trained through 5 epochs)
        ↓
Evaluate again (the model showed significant improvement in few underperforming classes, performance data can be found in model_v2)
        ↓
Save model

