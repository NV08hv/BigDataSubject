# Fraud Detection in Reviews using Graph Neural Networks

## Context and Objectives
- Online reviews significantly influence consumer decisions and business reputation.
- The rise of fake reviews poses a major challenge, undermining platform integrity.
- The trained model can be loaded and deployed to predict on data batches from Spark Streaming for this project.

## Methods
- Used the YelpChi dataset, containing over 67,000 reviews from 38,000 users and 201 hotels/restaurants.
- Graph representation with three relation types: same user, same product (same star rating), and same time.
- Implemented GraphSAGE (a GNN model for large graphs) and CARE-GNN (a GNN optimized for fraud detection).

## Results
Both models were effective in fraud detection:
- GraphSAGE achieved 85% accuracy but struggled with "camouflaged" nodes.
- CARE-GNN achieved ROC-AUC of 0.76 and Recall of 0.70, performing better in detecting coordinated fraud groups.
- CARE-GNN required more tuning and had higher computational complexity.

## Advantages & Limitations
- **Advantages**: Enhances reliability of online review systems, effectively detects fraudulent behavior.
- **Limitations**: Dataset not fully representative of other industries and platforms; requires significant computational resources.

## Conclusion and Future Directions
The research contributes to developing trustworthy review systems, aiding consumers in making informed decisions and protecting business reputations.
Future research directions include expanding the dataset, optimizing computational efficiency, and integrating graph-based methods with traditional machine learning.
