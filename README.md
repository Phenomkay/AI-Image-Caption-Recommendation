# AI Image Caption Recommendation

## Project Overview

This project is an AI-powered image caption recommendation system that suggests the most relevant captions for a given image from a predefined list. Instead of generating captions from scratch, the system evaluates how well each candidate caption aligns with the image and ranks them accordingly.

The solution is built using CLIP, a multimodal model that understands both images and text. By transforming both into embeddings within the same semantic space, the system can effectively measure similarity and recommend the best caption options.

---

## Project Objective

The objective of this project is to design a system that can intelligently recommend captions based on the semantic relationship between an image and a set of candidate captions.

The system aims to:

* Understand the content and context of an input image
* Compare the image with multiple caption options
* Rank captions based on semantic similarity
* Recommend the most relevant captions to the user

This eliminates the need for manual caption selection and introduces an automated, intelligent recommendation process.

---

## Installation

To run this project locally, ensure the following dependencies are installed:

* Python (3.8 or higher)
* PyTorch
* Transformers (Hugging Face)
* Scikit-learn
* Pillow

### Setup Steps

1. Clone the repository:

   ```
   git clone <repository-url>
   cd <repository-folder>
   ```

2. Install required dependencies:

   ```
   pip install -r requirements.txt
   ```

3. Place your image inside the project directory or provide the correct path when running the workflow.

---

## Project Structure

```
├── images/
│   └── sample images used for testing
│
├── src/
│   └── main workflow logic
│
├── results/
│   └── output examples and logs
│
├── README.md
└── requirements.txt
```

---

## Workflow

The system follows a structured pipeline to recommend captions:

### Step 1: Image Loading and Preprocessing

The input image is loaded and converted into a standard RGB format. It is then processed into a tensor format suitable for the model.

### Step 2: Image Embedding Generation

The CLIP model extracts semantic features from the image. These features are represented as numerical vectors that encode the meaning of the image.

### Step 3: Candidate Caption Preparation

A list of predefined captions is provided. These captions represent possible outputs that the system can recommend.

### Step 4: Text Embedding Generation

Each caption is processed through the CLIP text encoder to generate embeddings. This ensures both image and text are represented in the same semantic space.

### Step 5: Similarity Computation

Cosine similarity is used to compare the image embedding with each caption embedding. This measures how closely each caption aligns with the image.

### Step 6: Ranking Captions

All captions are sorted in descending order based on similarity scores.

### Step 7: Output Recommendation

The system returns the top-ranked captions along with their similarity scores.

---

## Results

### Sample Output

Top 5 Best Captions:

1. Where concrete learns to coexist with green. (Similarity: 0.2616)
2. A pause in the rush of the city. (Similarity: 0.2505)
3. The city breathes when you slow down. (Similarity: 0.2292)
4. Moving forward, quietly. (Similarity: 0.2143)
5. Every step has a story. (Similarity: 0.2128)

### Interpretation

The results demonstrate that the model successfully captures the context of the image and aligns it with captions that reflect:

* Urban environments
* Calmness and movement
* Interaction between nature and city life

The ranking shows relative relevance, allowing users to choose from multiple strong caption options.

---

## Tools and Technologies

* PyTorch
* Hugging Face Transformers (CLIP)
* Scikit-learn
* Python Imaging Library (PIL)

---

## Future Improvements

This project provides a strong foundation, but there are several ways it can be enhanced:

### Caption Generation

Extend the system to generate captions dynamically instead of relying only on predefined options.

### Larger Caption Pool

Integrate a larger or domain-specific caption dataset to improve recommendation diversity.

### Fine-tuning

Fine-tune the CLIP model on domain-specific images and captions for improved performance.

### Web Application

Deploy the system using Streamlit or a web framework to allow users to upload images and receive captions in real time.

### Personalization

Incorporate user preferences or tone selection (e.g., formal, poetic, humorous).

### Multilingual Support

Enable caption recommendations in multiple languages.

---

## Conclusion

This project demonstrates how AI can be used to recommend image captions through semantic similarity matching. By leveraging CLIP, the system bridges the gap between visual understanding and textual interpretation.

What has been achieved:

* Built a complete image-to-caption recommendation pipeline
* Enabled semantic comparison between images and text
* Ranked captions based on relevance using similarity scoring
* Delivered multiple high-quality caption suggestions for user selection

The project successfully achieves its goal of making caption selection more intelligent, efficient, and context-aware.

---

## Author

**Caleb Osagie (Kay)**
Data Scientist | Machine Learning Engineer
Founder, KayGroup Tech Hub

Focused on building data-driven solutions and AI-powered systems for real-world applications.
