# Mall Customer Segmentation 🛍️
> **Unsupervised Machine Learning for Targeted Retail Marketing**

## 📌 Project Overview
The goal of this project is to segment a mall's customer base into distinct groups based on their demographic and spending profiles. Using **K-Means Clustering**, we identified five unique customer personas. These insights allow marketing teams to move away from generic outreach and instead deploy data-driven, targeted campaigns that increase customer retention and maximize ROI.

## 🛠️ Technical Methodology
This project follows a structured data science pipeline, ensuring the results are mathematically sound and business-ready.

### 1. Preprocessing & Feature Scaling
Because K-Means is a distance-based algorithm, features on different scales (e.g., Annual Income in thousands vs. Spending Score 1-100) can bias the model. I used `StandardScaler` to normalize the data, ensuring both features contribute equally to the cluster assignment.

### 2. Finding the Optimal Clusters ($K$)
To determine the most effective number of segments, two primary techniques were used:
* **The Elbow Method:** Analyzing the Within-Cluster Sum of Squares (WCSS) to find the "bend" in the plot where adding more clusters yields diminishing returns.
* **Silhouette Score:** Measuring how similar an object is to its own cluster compared to other clusters. A score closer to **1** indicates well-defined, separate groups.

### 3. Mathematical Logic
The algorithm works by minimizing the **Inertia**, defined as the sum of squared distances of samples to their closest cluster center:
$$\sum_{i=0}^{n}\min_{\mu_j \in C}(||x_i - \mu_j||^2)$$
Where $x_i$ is a data point and $\mu_j$ is the mean (centroid) of the samples in the cluster.

---

## 📊 Identified Customer Personas
Based on the final model ($K=5$), the following segments were identified:

| Segment | Profile | Strategic Action |
| :--- | :--- | :--- |
| **Elite** | High Income, High Spending | **Top Priority:** Exclusive loyalty rewards and early access. |
| **Potential** | High Income, Low Spending | **Target:** Hyper-focused ads for premium/high-ticket items. |
| **Core** | Avg Income, Avg Spending | **Maintain:** General promotions and steady engagement. |
| **Impulsive** | Low Income, High Spending | **Engage:** Target with trends and high-frequency "flash" sales. |
| **Sensible** | Low Income, Low Spending | **Low Priority:** Focus on value-based marketing for essentials. |

---

## 🚀 Getting Started (How to Run)
Follow these steps to set up the project and run the analysis on your local machine.

### Prerequisites
* Python 3.8 or higher
* `pip` (Python package manager)
