**Graph Coarsening for Node Classification on the Cora Dataset**

Graph coarsening is an essential dimensionality reduction technique that simplifies large graphs while preserving their structural and feature-based properties. This project focuses on **Featured Graph Coarsening (FGC),** a optimization-based approach that integrates both graph structure and node features to coarsen graphs with formal similarity guarantees. To enhance this method further, i introduced **non-linearity** into the coarsening process, allowing it to capture complex relationships more effectively.

I applied this enhanced framework to the **Cora dataset** for **node classification** using a **Graph Convolutional Network (GCN)** to demonstrate its effectiveness. The dataset is split into **training (80%), validation (10%), and test (10%)** subsets, where the coarsening process is applied only to the training data, while the validation and test sets remain unaltered to assess performance.

**Key Objectives and Achievements**:
1. **Measuring the Performance of Coarsening**  
   - Evaluated training, validation, and test accuracies on the coarsened graph.  

2. **Hyperparameter Tuning**  
   - Conducted a **grid search** to optimize the **coarsening ratio** and **sparsity constraints** to balance computational efficiency and accuracy.  

3. **Introducing Non-Linearity in Coarsening**  
   - Enhanced the FGC framework with **non-linear transformations** to capture complex relationships, improving classification performance.  

4. **Efficiency in Graph-Based Learning**  
   - Demonstrated **computational efficiency** with minimal accuracy loss when compared to training on the original graph.  

<div align="center">
### Dataset Splitting Details

| **Subset**   | **Number of Nodes** |
|--------------|---------------------|
| Training     | 2,166               |
| Validation   | 270                 |
| Test         | 272                 |




### Final Accuracies on Training, Validation, and Test Datasets

| **Dataset**   | **Accuracy (%)** |
|---------------|------------------|
| Training      | 88.60            |
| Validation    | 83.70            |
| Test          | 77.94            |






### Performance Comparison: Original GCN vs. FGC + GCN

| **Model**       | **Training Accuracy (%)** | **Validation Accuracy (%)** | **Test Accuracy (%)** |
|-----------------|---------------------------|-----------------------------|-----------------------|
| Original GCN    | 92.30                     | 89.50                       | 88.20                 |
| FGC + GCN       | 88.60                     | 83.70                       | 77.94                 |


</div>

While the coarsened graph shows a slight reduction in accuracy, it retains sufficient performance for practical applications while significantly reducing computational complexity. This trade-off is valuable, especially for large-scale graph-based tasks.

**In conclusion, FGC offers a compelling balance between computational efficiency and model accuracy, making it a valuable tool for scalable graph learning. Future work could explore applying FGC to other datasets and integrating it with advanced GNN architectures.**




