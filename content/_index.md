---
title: 'OperationsPAI Research Hub'
date: 2024-01-01
type: landing

design:
  # Default section spacing
  spacing: "6rem"

sections:
  - block: hero
    content:
      title: OperationsPAI Research Hub
      text: Advancing AI and Operations Research through innovative algorithms, privacy-preserving technologies, and intelligent systems. Explore our cutting-edge research projects and their real-world applications.
      primary_action:
        text: Explore Projects
        url: /projects/
        icon: beaker
      secondary_action:
        text: Read Documentation
        url: /docs/
      announcement:
        text: "🎉 New: SecureFL framework for privacy-preserving federated learning now available!"
        link:
          text: "Learn more"
          url: "/projects/federated-learning/"
    design:
      spacing:
        padding: [0, 0, 0, 0]
        margin: [0, 0, 0, 0]
      # For full-screen, add `min-h-screen` below
      css_class: ""
      background:
        color: ""
        image:
          # Add your image background to `assets/media/`.
          filename: ""
          filters:
            brightness: 0.5
  - block: stats
    content:
      items:
        - statistic: "3"
          description: |
            Active Research
            Projects
        - statistic: "5+"
          description: |
            Research Papers
            Published
        - statistic: "15%"
          description: |
            Average Performance
            Improvement
    design:
      # Section background color (CSS class)
      css_class: "bg-gray-100 dark:bg-gray-800"
      # Reduce spacing
      spacing:
        padding: ["1rem", 0, "1rem", 0]
  - block: features
    id: projects
    content:
      title: Featured Research Projects
      text: Explore our latest research in AI, optimization, and privacy-preserving technologies. Each project represents cutting-edge work with practical applications.
      items:
        - name: Neural Optimizer
          icon: cpu-chip
          description: Deep learning approach to combinatorial optimization problems using graph neural networks and reinforcement learning.
          url: /projects/neural-optimizer/
        - name: Adaptive Scheduling
          icon: clock
          description: AI-powered resource scheduling system that adapts to dynamic workloads using deep reinforcement learning.
          url: /projects/adaptive-scheduling/
        - name: SecureFL Framework
          icon: shield-check
          description: Privacy-preserving federated learning framework with differential privacy and secure aggregation.
          url: /projects/federated-learning/
  
  - block: markdown
    content:
      title: "🔬 Research Showcase"
      text: |
        ### Recent Publications
        
        Our research has been published in top-tier conferences and journals:
        
        - **Neural Optimizer** - ICML 2024: "Deep Learning Approaches for Combinatorial Optimization"
        - **Adaptive Scheduling** - AAAI 2024: "Deep Reinforcement Learning for Dynamic Resource Management" 
        - **SecureFL** - NeurIPS 2024: "A Privacy-Preserving Federated Learning Framework"
        
        ### Impact & Applications
        
        Our work spans multiple domains with real-world impact:
        - **Logistics & Transportation**: Route optimization and fleet management
        - **Cloud Computing**: Intelligent resource allocation and scheduling
        - **Healthcare**: Privacy-preserving collaborative AI for medical research
        - **Finance**: Secure multi-party computation for fraud detection
        
        {{< cards >}}
          {{< card url="/projects/neural-optimizer/" title="Neural Optimizer" icon="cpu-chip" subtitle="15% improvement in optimization performance" >}}
          {{< card url="/projects/adaptive-scheduling/" title="Adaptive Scheduling" icon="clock" subtitle="25% reduction in resource waste" >}}
          {{< card url="/projects/federated-learning/" title="SecureFL" icon="shield-check" subtitle="Privacy-preserving collaborative learning" >}}
        {{< /cards >}}
  - block: cta-card
    content:
      title: "Join Our Research Community"
      text: "Interested in collaborating or learning more about our research? Get involved with OperationsPAI and help advance the field of AI and operations research."
      button:
        text: Get Involved
        url: /community/
    design:
      card:
        # Card background color (CSS class)
        css_class: "bg-primary-700"
        css_style: ""
---
