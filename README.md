# Dorylus
Dorylus: Affordable, Scalable, and Accurate GNN Training over Billion-Edge Graphs (OSDI 2021)

## Summary of Dorylus

A graph neural network (GNN) enables deep learning on structured graph data. There are two major GNN training obstacles: 1) it relies on high-end servers with many GPUs which are expensive to purchase and maintain, and 2) limited memory on GPUs cannot scale to today's billion-edge graphs. This paper presents Dorylus: a distributed system for training GNNs. Uniquely, Dorylus can take advantage of serverless computing to increase scalability at a low cost.

The key insight guiding our design is computation separation. Computation separation makes it possible to construct a deep, bounded-asynchronous pipeline where graph and tensor parallel tasks can fully overlap, effectively hiding the network latency incurred by Lambdas. With the help of thousands of Lambda threads, Dorylus scales GNN training to billion-edge graphs. Currently, for large graphs, CPU servers offer the best performance-per-dollar over GPU servers. Just using Lambdas on top of CPU servers offers up to 2.75✕ more performance-per-dollar than training only with CPU servers. Concretely, Dorylus is 1.22✕ faster and 4.83✕ cheaper than GPU servers for massive sparse graphs. Dorylus is up to 3.8✕ faster and 10.7✕ cheaper compared to existing sampling-based systems.

## Team 
This project is done in collaboration with Professor [Harry Xu](http://web.cs.ucla.edu/~harryxu/)'s group at UCLA. Please visit [Dorylus project at UCLA Systems](https://github.com/uclasystem/dorylus).

https://github.com/uclasystem/dorylus

## How to cite 
Please refer to our OSDI'21 paper, [Dorylus: Affordable, Scalable, and Accurate GNN Training with Distributed CPU Servers and Serverless Threads](https://www.usenix.org/conference/osdi21/presentation/thorpe) for more details. 
### Bibtex
```txt
@inproceedings {273743,
author = {John Thorpe and Yifan Qiao and Jonathan Eyolfson and Shen Teng and Guanzhou Hu and Zhihao Jia and Jinliang Wei and Keval Vora and Ravi Netravali and Miryung Kim and Guoqing Harry Xu},
title = {Dorylus: Affordable, Scalable, and Accurate {GNN} Training with Distributed {CPU} Servers and Serverless Threads},
booktitle = {15th {USENIX} Symposium on Operating Systems Design and Implementation ({OSDI} 21)},
year = {2021},
isbn = {978-1-939133-22-9},
pages = {495--514},
url = {https://www.usenix.org/conference/osdi21/presentation/thorpe},
publisher = {{USENIX} Association},
month = jul,
}
```

## Video
You can watch a OSDI'21 presentation video [here](https://www.youtube.com/watch?v=A2x3LjiFWR0)
 
