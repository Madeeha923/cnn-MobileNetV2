# Flower Image Classification using Transfer Learning

This project uses a **pre-trained MobileNetV2** model to classify flower images from the **Flowers-102 dataset**.  
The core technique demonstrated is **transfer learning**, where a model trained on a large dataset (*ImageNet*) is adapted for a new, specific task.

---

##  Project Overview
The goal of this project is to build an **accurate image classifier** for **102 different types of flowers**.  
Instead of training a deep neural network from scratch (which requires massive data and compute power), we **fine-tune MobileNetV2**.

###  Process
1. Load the MobileNetV2 model with pre-trained **ImageNet weights**.  
2. **Freeze** the convolutional base (acts as a fixed feature extractor).  
3. **Replace** the final classification layer with a new one for **102 flower classes**.  
4. Train only the new layer on the flower dataset.  
5. Implement **early stopping** to prevent overfitting and save the best model.  

---

##  About MobileNetV2
MobileNetV2 is a CNN architecture designed for **high efficiency**, making it ideal for **mobile and low-power systems**.

- **Efficiency**: Uses *depthwise separable convolutions* to reduce computation while maintaining accuracy.  
- **Architecture**: Built on *inverted residuals* and *linear bottlenecks*, enabling deep networks with fewer parameters.  
- **Transfer Learning**: Trained on **ImageNet**, it serves as an excellent **feature extractor** for tasks like flower classification.

---

## Results & Analysis
The initial training run shows a classic learning pattern:

-  **Successful Learning**:  
  The model learned effectively for ~18 epochs, reaching **77.55% validation accuracy** at **epoch 19** with a validation loss of **0.9687**.  

-  **Overfitting**:  
  After epoch 19, training loss decreased while validation loss increased, indicating overfitting.  

- ⏹ **Early Stopping**:  
  T
