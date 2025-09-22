---
title: "Neural Optimizer: Deep Learning for Combinatorial Optimization"
type: landing
date: 2024-01-15

design:
  spacing: "6rem"

sections:
  - block: hero
    content:
      title: Neural Optimizer
      text: |
        A novel deep learning approach to solving complex combinatorial optimization problems using graph neural networks and reinforcement learning.
      primary_action:
        text: View Paper
        url: "#paper"
        icon: document
      secondary_action:
        text: See Results
        url: "#results"
    design:
      background:
        color: "bg-blue-50 dark:bg-blue-900"
      spacing:
        padding: ["3rem", 0, "3rem", 0]

  - block: markdown
    id: paper
    content:
      title: "📄 Research Paper"
      text: |
        **Title**: Neural Optimizer: Deep Learning Approaches for Combinatorial Optimization
        
        **Authors**: Zhang Wei, Li Ming, Wang Xiaoli
        
        **Conference**: ICML 2024 (International Conference on Machine Learning)
        
        **Abstract**: This work presents a novel neural architecture for solving combinatorial optimization problems. Our approach combines graph neural networks with reinforcement learning to achieve state-of-the-art performance on various optimization benchmarks.
        
        **Key Contributions**:
        - Novel GNN architecture for optimization problems
        - Reinforcement learning framework for solution search
        - 15% improvement over previous methods on TSP benchmarks
        - Generalization across different problem sizes

  - block: stats
    id: results
    content:
      title: "🎯 Key Results"
      items:
        - statistic: "15%"
          description: |
            Performance improvement
            over state-of-the-art
        - statistic: "10x"
          description: |
            Faster convergence
            compared to traditional methods
        - statistic: "5+"
          description: |
            Benchmark datasets
            evaluated on
    design:
      css_class: "bg-gray-100 dark:bg-gray-800"
      spacing:
        padding: ["2rem", 0, "2rem", 0]

  - block: features
    content:
      title: "🔬 Experimental Results"
      text: "Comprehensive evaluation across multiple optimization problems and datasets."
      items:
        - name: Traveling Salesman Problem
          icon: route
          description: "Achieved 15% improvement on TSPLIB benchmarks with up to 1000 cities."
        - name: Vehicle Routing Problem
          icon: truck
          description: "Reduced total route distance by 12% on standard VRP datasets."
        - name: Job Shop Scheduling
          icon: calendar
          description: "Improved makespan by 18% on benchmark scheduling instances."
        - name: Graph Coloring
          icon: color-swatch
          description: "Found optimal colorings for 95% of test graphs within time limit."
        - name: Knapsack Problem
          icon: archive-box
          description: "Achieved optimal solutions for 98% of large-scale knapsack instances."
        - name: Bin Packing
          icon: cube
          description: "Reduced number of bins by 8% compared to best known heuristics."

  - block: markdown
    content:
      title: "📊 Detailed Analysis"
      text: |
        ### Training Methodology
        
        Our neural optimizer was trained on a diverse set of optimization problems using:
        - **Graph Neural Networks**: Custom architecture with attention mechanisms
        - **Reinforcement Learning**: Policy gradient methods with curriculum learning
        - **Multi-task Learning**: Joint training across different problem types
        
        ### Performance Comparison
        
        | Method | TSP-100 | TSP-500 | TSP-1000 | Training Time |
        |--------|---------|---------|----------|---------------|
        | Nearest Neighbor | 12.3 | 15.8 | 18.2 | - |
        | Genetic Algorithm | 8.7 | 11.2 | 14.1 | - |
        | Previous Neural Method | 7.2 | 9.8 | 12.5 | 24h |
        | **Our Method** | **6.1** | **8.3** | **10.6** | **18h** |
        
        ### Ablation Studies
        
        We conducted extensive ablation studies to understand the contribution of each component:
        - **GNN Architecture**: 8% performance gain
        - **Attention Mechanism**: 4% performance gain  
        - **Curriculum Learning**: 3% performance gain

  - block: cta-card
    content:
      title: "Access the Research"
      text: "Get full access to our paper, code, and datasets to reproduce and extend our results."
      button:
        text: "Download Resources"
        url: "#downloads"
    design:
      card:
        css_class: "bg-primary-700"
---