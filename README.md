# Siamese Network for Celebrity Image Identification

This project implements a **Siamese Network** to identify individuals from a database of celebrity images. The model is **pretrained** and designed to handle face identification tasks, including scenarios where the user is wearing a mask.

---

## Features

- **Database Creation**: A database of celebrity images is created using a generic dataset.
- **User Image Upload**: A new image of the user can be added to the database.
- **Masked Image Recognition**: The system identifies a user wearing a mask by matching their image with those in the database.

---

## Prerequisites

To run this project, ensure you have the following installed:

- Python (>= 3.7)
- Jupyter Notebook
- Libraries:
  - PyTorch
  - NumPy
  - Matplotlib  
  - SQLite3 (for database storage)

---

## Dataset

The project uses a generic celebrity image dataset. Each image in the database is processed to create a feature descriptor vector for identification.

---

## How It Works

1. **Database Initialization**: 
   - All celebrity images are loaded and processed into a feature vector using the Siamese Network.
   - The feature vectors are stored in a SQLite database.

2. **User Image Upload**:
   - The user uploads their image, which is then processed and added to the database.

3. **Masked Image Identification**:
   - A new image of the user wearing a mask is captured.
   - The system compares the feature descriptor vector of the masked image with all vectors in the database to find the closest match.


---

## Customization

- **Dataset**: Replace the dataset with your own images by modifying the image loading and processing functions.
- **Network Architecture**: The Siamese Network uses a pretrained backbone. This can be swapped for another architecture if desired.

---

## Future Improvements

- Improve performance for images under extreme occlusion or varied lighting.
- Extend to multi-class face recognition for additional scalability.
- Explore transfer learning with other pretrained models.
