# Pathfinder Task - LRA Benchmark

Welcome to our AI project repository, where we have tackled the **Pathfinder Task** from the **Long Range Arena (LRA) Benchmark**. This task is a challenging computer vision problem that tests a model's ability to detect and distinguish paths in complex images by treating them as a sequence of individual pixels.


## Repository Structure

### 1. **Root Directory**
- **`dataset.ipynb`**: This notebook aggregates and processes the original dataset to create the **easy**, **medium**, and **hard** difficulty datasets. It ensures that the data is in a format suitable for experimentation, consisting of sequences of 1024 pixels' values.
- **`LRA_Report`**: A comprehensive slide deck detailing the architectures tried, findings, and benchmarks from the experiments conducted.

### 2. **Individual Contributions**
The repository contains four main folders corresponding to the individual contributors and other experiments:

#### **BEiT + Performer + ViT (Maha)**
- **`experiments/`**: Contains Jupyter notebooks used on Kaggle to benchmark models or run experiments related to the pathfinding task.
- **`Performance Images/`**: Contains screenshots of the performance metrics for each model tested by Maha, documenting the results visually.

#### **Gru + LSTM + RNN + TCN + Linformer (Zakaria)**
- **`experiments/`**: Includes Jupyter notebooks for benchmarking models and running experiments on the pathfinding task, executed on Kaggle.
- **`Tensorboard/`**: Contains Tensorboard logs of the experiments conducted by Zakaria, providing detailed performance visualizations.

#### **Vanilla Transformer + Perceiver (Mohieddine)**
- **`experiments/`**: Houses Jupyter notebooks used on Kaggle to test various models and conduct experiments on the pathfinding task.
- **`Logs/`**: Contains a text file with logs detailing the training processes and outcomes of the models experimented with by Mohieddine.

#### **Other Experiments**
- **`experiments/`**: Contains additional Jupyter notebooks for various experiments. This folder does not include any logs.

### 3. **Experiments**
- All experiment-related notebooks have self-descriptive names and are stored within the respective `experiments` folders under each contributor's directory.
- Examples of experiments include:
  - Comparing the effects of **embedding** vs. **normalization/scaling** of pixel values.
  - Exploring whether **structured self-attention** enhances the performance of a GRU model.
  - Investigating the impact of simplifying a Temporal Convolutional Network (TCN).
  - Evaluating the performance of models such as Performer, ViT, and BeiT.

### 4. **Model Logging**
- **Zakaria**: Logs and performance visualizations are stored in the `Zakaria/Tensorboard` folder as Tensorboard logs.
- **Maha**: Performance screenshots for each model are stored in the `Maha/Performance Images` folder.
- **Mohieddine**: Training logs in text format are stored in the `Mohieddine/Logs` folder.

---

This structure ensures organized documentation and storage of experiments, logs, and findings, allowing for easy navigation and comprehensive analysis.


## Core Implementations
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