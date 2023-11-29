# Thermal Udder Segmentation for Mastitis Prediction

This repository showcases a comprehensive approach to thermal segmentation for mastitis prediction in buffaloes. The segmentation task involves identifying the udder region within thermal images, crucial for accurate mastitis assessment. The implemented solution integrates several key strategies to enhance segmentation performance.

## Key Features

1. **Segmentation Mask Smoothing:**
   - The provided polygonal masks are smoothed using Gaussian blurring to account for the inherent imprecision in the boundary definition of the udder region.

2. **Joint Dice Loss Function:**
   - The segmentation task employs a joint Dice loss function, optimizing the model's performance by considering the spatial overlap between predicted and ground truth masks.

3. **Self-Supervised Autoencoder:**
   - A self-supervised learning stage is implemented using an autoencoder. The autoencoder learns to reconstruct the thermal images, serving as a pretext task to leverage unlabeled data effectively.

4. **Transfer Learning:**
   - Transfer learning is applied after the self-supervised autoencoder stage, leveraging knowledge gained from a related domain to fine-tune the segmentation model on the target thermal images.

## Project structure

1. **Training:**
   - Execute the training notebook (`training.ipynb`), adjusting hyperparameters as needed.

2. **Testing:**
   - Execute the testing notebook (`testing.ipynb`) to evaluate the trained model on test data.
