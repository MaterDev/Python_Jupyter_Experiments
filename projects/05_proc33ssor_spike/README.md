# Proc33ssor Prototype

![Cover Image](./images/cover.png)

## Overview

**Proc33ssor** is a standalone application designed to analyze and catalog a large archive of images on a local machine. This prototype focuses on processing a single image to generate detailed metadata and then extending the process to handle multiple images. The metadata will be stored in a local database, enabling efficient searching and retrieval of images based on various criteria.

## Features

1. **Image Tagging:**
   - Generate descriptive tags for images using a locally hosted Large Language Model (LLM).
   - **Technologies:** Hugging Face Transformers, spaCy

2. **Basic Data Analysis:**
   - Analyze and display metrics such as value distribution, color scheme, and color gamut.
     - [x] Read Image Metadata
     - [x] Grayscale Value Distribution: Histogram of pixel values, after image has been converted to BW.
     - [ ] 2 Value Posterize Value Distribution: Histogram of pixel values, after image has been converted to 2 colors.
     - [ ] Full Color Distribution: Histogram of color values.
     - [ ] Image Proportion: Aspect ratio of the image.
   - Additional metrics: edge detection, texture analysis, and histogram analysis.
   - **Technologies:** OpenCV, scikit-image

3. **Unique Identifier Embedding:**
   - Embed a unique identifier into the byte data of each image to record authorship and identity.
   - **Technologies:** Pillow, Steganography Libraries (e.g., Stegano)

4. **Additional Metrics:**
   - Detect dominant colors and objects in images.
   - **Technologies:** TensorFlow/Keras, EXIFRead

5. **Database Storage:**
   - Store and retrieve image metadata and version history in a local database.
   - **Technologies:** SQLite

6. **Natural Language Search:**
   - Implement basic search functionality to find images based on written prompts.
   - **Technologies:** Elasticsearch

7. **Version Control:**
   - Maintain a `proc33ssVersion` value embedded in each image and store version history in the database.
   - Track and store the current version in an environment variable on the host system.