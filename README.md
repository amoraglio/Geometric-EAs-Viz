# Distance-Based Search Algorithm Visualizations

Interactive visualizations of optimization algorithms unified under the **Geometric Theory of Evolutionary Algorithms** framework. This repository demonstrates how distance metrics provide a mathematical foundation for understanding and designing search operators across different problem representations.

## Overview

Traditional optimization algorithms appear fundamentally different across representations (binary strings, real vectors, permutations, etc.). However, the geometric framework reveals that these algorithms share common underlying principles when viewed through the lens of distance metrics and spatial relationships.

**Key Concepts:**
- **Geometric Mutation**: Sampling from balls (neighborhoods) around parent solutions
- **Geometric Crossover**: Sampling from segments (paths) between parent solutions  
- **Distance-Based Tabu Search**: Using geometric regions instead of attribute-based restrictions
- **Unified Design**: Same geometric principles work across all representations

## Current Visualizations

### Tabu Search Algorithms

#### 1. Ball-Based Tabu Search
- **File**: `ball_based_tabu_search.html`
- **Approach**: Uses circular regions to define forbidden areas
- **Key Features**:
  - Red circle: Tabu ball (forbidden region) centered at oldest solution
  - Blue circle: Neighborhood sampling region around current solution
  - Purple line: Segment connecting oldest to current solution
  - Dynamic radius based on distance between oldest and current solutions

#### 2. Convex Hull Tabu Search  
- **File**: `convex-hull-tabu-search.html`
- **Approach**: Uses convex hull of recent solutions as forbidden region
- **Key Features**:
  - Gray polygon: Convex hull of recently visited solutions (tabu region)
  - Red dots: Individual points in tabu list
  - Exact geometric generalization of traditional attribute-based tabu search

### Test Functions
Both visualizations include standard multimodal optimization functions:
- **Rastrigin**: Highly multimodal with many local optima
- **Ackley**: Nearly flat outer region with central peak
- **Rosenbrock**: Valley-shaped with global optimum in narrow valley  
- **Himmelblau**: Four global optima

## How to Use

1. **Open any HTML file** in a modern web browser (Chrome, Firefox, Safari, Edge)
2. **Select a test function** from the dropdown menu
3. **Adjust algorithm parameters** using the control sliders:
   - Neighborhood size and radius
   - Tabu tenure (memory length)
   - Search speed and iteration limits
4. **Click "Start"** to begin the optimization process
5. **Observe** how the algorithm navigates the fitness landscape while avoiding tabu regions

### Interactive Controls

- **Speed**: Animation delay between iterations (100-1000ms)
- **Neighborhood Size**: Number of candidate solutions generated per iteration
- **Neighborhood Radius**: Spatial extent of solution sampling
- **Tabu Tenure**: How long solutions remain forbidden
- **Random Walk**: Toggle between best-improvement and random selection

## Planned Additions

### Evolutionary Algorithms
- [ ] **Geometric Crossover Visualizations**: Show how crossover samples from segments between parents
- [ ] **Mutation Operators**: Demonstrate ball-based sampling across representations
- [ ] **Convex Search Property**: Visualize how populations remain in convex hulls

### Local Search Methods  
- [ ] **Path-Relinking**: Systematic exploration of shortest paths between solutions
- [ ] **Variable Neighborhood Search**: Distance-based neighborhood switching
- [ ] **Simulated Annealing**: Geometric interpretation of acceptance criteria

### Multi-Representation Examples
- [ ] **Binary String Operations**: Hamming distance neighborhoods
- [ ] **Permutation Operations**: Adjacent swap and insertion distances  
- [ ] **Tree Operations**: Edit distance-based genetic programming
- [ ] **Graph Operations**: Graph edit distance neighborhoods

### Advanced Concepts
- [ ] **Distance Metric Comparison**: Visualize how different metrics affect search behavior
- [ ] **Segment API Demonstrations**: Interactive examples of the distance-based programming interface
- [ ] **Representation-Search Space Duality**: Show algebraic vs geometric perspectives

## Technical Implementation

- **Frontend**: Pure HTML5 + JavaScript with React
- **Visualization**: HTML5 Canvas for real-time rendering
- **Dependencies**: React, Lodash (loaded via CDN)
- **Compatibility**: Modern browsers with ES6+ support

## Academic Background

This work is based on the **Geometric Theory of Evolutionary Algorithms**, which provides a unified mathematical framework for understanding optimization algorithms across different representations. The theory reveals deep connections between:

- Evolutionary algorithms and local search methods
- Distance metrics and neighborhood structures  
- Representation-specific operators and geometric primitives
- Algorithm design principles and mathematical foundations

### Key Insights

1. **Unification**: Seemingly different operators (bit-flip, Gaussian mutation, swap operations) are instances of the same geometric principle
2. **Convex Search**: Crossover-based algorithms inherently perform convex search in their respective metric spaces  
3. **Design Principles**: Good neighborhood structures lead to good crossover operators
4. **Generalization**: Traditional algorithms can be extended to new representations through distance metrics

## Contributing

Contributions are welcome! Areas of particular interest:
- Additional test functions and problem domains
- New algorithm visualizations following the geometric framework
- Performance optimizations and UI improvements
- Educational features and explanations
- Mobile-responsive design improvements

## License

This project is released under the MIT License. See `LICENSE` file for details.

## Related Work

For deeper understanding of the theoretical foundations, see academic literature on:
- Geometric Theory of Evolutionary Algorithms
- Distance-based search operators
- Metric spaces in optimization
- Representation-independent algorithm design

---

**Note**: These visualizations are educational tools designed to illustrate theoretical concepts. For production optimization tasks, consider using specialized optimization libraries with appropriate performance characteristics.
