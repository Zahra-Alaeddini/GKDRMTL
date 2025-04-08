## GKD2RMTL: A Multi-Task Learning and Knowledge Distillation Framework for Efficient Graph-Based Drug Repurposing  

GKD2RMTL introduces a graph-based teacher-student framework for multi-task learning on a customized Biomedical Knowledge Graph (BKG). The teacher model leverages a multi-layer GraphSAGE architecture with Leaky ReLU activations, dropout regularization, and task-specific output heads. It is designed to predict various biomedical relationships, including:  
- **Drug-Disease Associations**  
- **Drug Similarity**  
- **Drug-Gene Binding Interactions**  
- **Disease-Gene Associations**
  
   ![image](https://github.com/user-attachments/assets/846f3738-7303-4a98-853c-953c97555f8b)
  
The student model adopts a lighter structure for efficient deployment, utilizing a single-layer GraphSAGE while retaining task-specific heads to facilitate multi-task predictions. Knowledge distillation plays a key role, where the teacher’s softened logits, obtained through temperature scaling, guide the student model via a distillation loss function, ensuring the effective transfer of task-specific knowledge.  

To address class imbalance in edge prediction tasks, the framework incorporates a weighted binary cross-entropy loss alongside optimized negative sampling strategies, enhancing performance on sparse datasets. The pipeline integrates node features, edge connections, edge attributes, and GraphSAGE layers, ensuring predictions are informed by ground-truth data and teacher supervision.  

## Features  
✅ Multi-task learning with task-specific heads  
✅ Graph-based knowledge distillation for efficient student model training  
✅ Optimized negative sampling for sparse biomedical datasets  
✅ Lightweight student model for scalable deployment  
✅ Integration of node features, edge attributes, and GraphSAGE embeddings  

## Prerequisites  
Ensure you have the following dependencies installed:  
- Python 3.8+  
- PyTorch    
- NumPy  
- Pandas  
- Scikit-learn  


