# FACE RECOGNITION PROJECT 

This is a beginner friendly face recognition project built in Google Colab. The project detects faces from an image, saves the detected faces, creates image embeddings, stores them in a PostgreSQL database, and compares a new image with the stored faces to find the closest match.

## What the Project Does

1. Loads an image using OpenCV.
2. Detects faces using a Haar Cascade classifier.
3. Crops and saves the detected faces.
4. Generates embeddings for each face using `imgbeddings`.
5. Stores the image name and embedding in PostgreSQL.
6. Creates an embedding for a new test image.
7. Compares the new embedding with the stored embeddings using vector similarity.
8. Displays the closest matching stored face.

## Images Used in This Project

The stored-faces folder contains the detected face images named from 0.jpg to 8.jpg. These images represent the faces that are stored in the PostgreSQL database together with their corresponding embeddings.

The Jeff-Bezos.jpg image is used as the test image. The program generates an embedding for this image and compares it with the embeddings of the faces stored in the database.

Using vector similarity, the program searches for the stored face whose embedding is closest to the embedding of Jeff-Bezos.jpg. The closest matching image from the stored-faces folder is then displayed as the result.

## Technologies Used

- Python
- Google Colab
- OpenCV
- imgbeddings
- Pillow
- NumPy
- PostgreSQL
- pgvector

## Installation

In Google Colab, install the required libraries with:

!pip install opencv-python numpy imgbeddings psycopg2-binary pillow

Depending on the current version of imgbeddings, you may also need:

!pip install "huggingface_hub==0.25.2"


