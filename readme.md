# Pathfinder Task - LRA Benchmark

Welcome to our AI project repository, where we have tackled the **Pathfinder Task** from the **Long Range Arena (LRA) Benchmark**. This task is a challenging computer vision problem that tests a model's ability to detect and distinguish paths in complex images by treating them as a sequence of individual pixels.

## Repository Structure

### 1. **Dataset Preparation**
- **`dataset.ipynb`**: This notebook aggregates and processes the original dataset to create the **easy**, **medium**, and **hard** difficulty datasets. It ensures that the data is in a format suitable for experimentation, a sequence of 1024 pixels' values.

### 2. **Experiments**
- All other files in the repository are Jupyter notebooks with self-descriptive names. Each notebook represents a unique experiment conducted on Kaggle.
- Examples of experiments:
  - Comparing the effects of **embedding** vs. **normalization/scaling** of pixel values.
  - Exploring whether **structured self-attention** improves the performance of a GRU model.
  - Testing if simplifying a Temporal Convolutional Network (TCN) yields performance improvements.
  - Testing the Performer, ViT and BeiT Models

### 3. **Model Logging**
- Logs and performance visualizations are stored in the `tensorboard` folder.
- Each subfolder within `tensorboard` corresponds to a specific experiment, allowing for easy navigation and comparison of results.

### 4. **Core Implementations**
- **TCN from Scratch**: Our implementation of the Temporal Convolutional Network (TCN) was crafted from the ground up, providing us with deep insights into its functionality.
- **Structured Self Attention**

## Key Insights

### Questions We Explored
1. **Embedding vs. Scaling**: 
   - Which approach yields better results: using embeddings or normalizing/scaling pixel values?
2. **Structured Self-Attention**: 
   - Does structured self-attention boost the performance of the GRU model?
3. **Simplified TCN**:
   - Can simplifying the TCN architecture result in meaningful gains?

### Gradual Fine-Tuning: The Ace Up Our Sleeve
Our most impactful strategy was **gradual fine-tuning**:
- Models were trained progressively on the **easy**, **medium**, and finally the **hard** dataset.
- This approach delivered remarkable improvements, such as a **25% accuracy boost** for the GRU model.

### Theoretical Foundations
We ensured a strong theoretical foundation for our work by thoroughly understanding the intuition behind each model. We achieved this by studying the original research papers, some of which are referenced in the presentation included in this repository.

## Getting Started

1. Clone this repository.
2. Use the `dataset.ipynb` to prepare the datasets.
3. Navigate through the experiment notebooks to explore various approaches and their results.
4. Visualize results in the `tensorboard` directory.

## Conclusion

This project has been an exciting journey, combining theoretical insights with practical experimentation to solve a complex benchmark task. We hope you find our work both inspiring and useful. Happy exploring!