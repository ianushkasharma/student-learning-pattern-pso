# Student Learning Pattern Clustering 

**Bio-Inspired Computing – Unsupervised Learning, Problem 20**

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ianushkasharma/student-learning-pattern-pso/blob/main/Student_Learning_Pattern_Clustering_PSO.ipynb)

## Problem
Cluster students by **study hours, quiz performance, attendance and assignment completion** to find distinct learning patterns.

## Bio-inspired concept
**Particle Swarm Optimization** (bird-flock / fish-school intelligence). Each particle encodes all `k` cluster centroids; particles
move using inertia + personal-best + global-best attraction. Fitness = mean squared quantization error.
PSO is implemented **from scratch in NumPy** with linearly decreasing inertia, velocity clamping and boundary handling.

## What the notebook does
1. Generates 400 synthetic students (or upload your own CSV)
2. EDA – histograms, correlation heatmap, pairplot
3. PSO clustering + automatic `k` selection (elbow, silhouette, Davies-Bouldin, Calinski-Harabasz, rank aggregation)
4. Convergence, swarm diversity, inertia schedule, centroid-evolution snapshots
5. PCA scatter, interactive 3-D plot, parallel coordinates
6. Cluster profiling – heatmap, radar, violins, sizes
7. Silhouette plot, **PSO vs K-Means**, ARI vs hidden truth, 15-run stability test, swarm-size sensitivity
8. Student-level recommendations + new-student prediction; exports `clustered_students.csv`

## Run
Open the notebook in Google Colab and choose **Runtime ▸ Run all** (about 1–2 minutes), or locally:
```
pip install -r requirements.txt
jupyter notebook Student_Learning_Pattern_Clustering_PSO.ipynb
```

## Result (seed 42)
PSO selects k = 4: Consistent High Achievers, Hard Workers, Smart Skippers, Disengaged/At-Risk.
