# Introduction to Machine Learning

After Artificial Intelligence was introduced in the computing world, there was a need for machines that could automatically improve processes. This improvement needed to be regulated, so rules were established for learning processes.

## Basic Goals of Machine Learning

- Analyse and adapt data independently
- Make decisions based on calculations and analyses
- Improve computers by mimicking the human brain's learning process
- Enable devices to make data-driven decisions

### Example: Real-Time GPS Data

- **Maps on devices**: Use real-time GPS data to show the quickest route
- **Algorithms used**:
  - Shortest path (Dijkstra's algorithm)
  - Travelling salesman (works like water flow)
- **Decision process**:
  - Uses GPS coordinates, traffic data, and predefined map routes
  - Determines the fastest way to travel from Point A to Point B

## Challenges in Machine Learning

- **Accuracy and limitations**: Data accuracy is debated, and decisions must comply with legal boundaries.
- **Self-learning systems**: Must adhere to restrictions to function within legal and ethical limits.

### Importance of Data

- **Data as the soul of business**: Key to decision-making from the prehistoric era to modern times
- **Machine learning**: Helps unlock new potentials using various data types (customer, corporate, demographic)
- **Companies**: Google, Microsoft, Facebook, and Amazon use machine learning for decision-making.

## Common Applications

- **Cyber phenomena**: Interpretation and investigation
- **Future projections**: Extract and predict future values
- **Anomaly detection**: Identify irregularities

### Open-Source Solutions

- **Projects**: Weka, Orange, Rapid-Miner
- **Visualization tools**: Tableau, Pivotal, Spotfire

## Objectives

After studying this unit, you should be able to:
- Understand the basics of machine learning
- Identify various machine learning techniques
- Grasp concepts of Reinforcement Learning, Deep Learning, and Ensemble Methods

## Developing Machine Learning Models

- **Steps**:
  - Understand data
  - Describe data characteristics
  - Locate hidden connections and patterns
- **Methods**: Statistics, data mining, and machine learning

### Data Mining vs. Machine Learning

- **Data Mining**:
  - Extraction of latent, unknown, and beneficial information
  - Builds algorithms to search large databases for patterns
  - Patterns lead to benefits, often economic

- **Machine Learning**:
  - Core of data mining's technical infrastructure
  - Extracts information from raw data
  - Constructs usable models

### Relationships Between Fields

- **Overlap**: Machine learning, data mining, and statistics are interconnected
- **Differences**:
  - Statistics: Focus on hypothesis testing
  - Machine learning: Focus on generalisation processes

## Techniques and Applications

- **Algorithms**: Decision-tree, genetic algorithms, inductive logic procedures
- **Goals**:
  - Understand cyber phenomena
  - Abstract understanding into models
  - Predict future values
  - Identify anomalous behavior

### Learning Techniques

- **Definition**: To learn means to acquire knowledge, experience, or mastery of a skill.
- **Machine Learning**: Improves systems through experience and learning processes

### Check Your Progress

1. **Difference from AI**:
   - Machine learning is a subset of AI focusing on data-driven learning and adaptation.
   
2. **Major functions of ML algorithms**:
   - Understand cyber phenomena
   - Model underlying phenomena
   - Predict future values
   - Detect anomalies

## 9.3 Techniques of Machine Learning

Machine learning uses various algorithms to improve, describe, and predict outcomes by repeated learning from data. Here's a breakdown of key concepts and techniques in machine learning:

### Machine Learning Cycle
Creating a machine learning application involves an iterative process:
1. **Data Identification**
2. **Data Preparation**
3. **Selection of Machine Learning Algorithm**
4. **Training the Algorithm to Develop a Model**
5. **Evaluating the Model**
6. **Deploying the Model**
7. **Performing Prediction**
8. **Assessing the Predictions**

### Effective Use of Machine Learning Techniques
- Understand how techniques work.
- Different techniques suit different problems.
- Choose the right algorithm based on data type and business problem.

### Steps in the Machine Learning Cycle
1. **Access and Load the Data**
2. **Preprocess the Data**
3. **Derive Features from Preprocessed Data**
4. **Train Models Using Derived Features**
5. **Iterate to Find the Best Model**
6. **Integrate the Best-Trained Model into a Production System**
7. **Perform Prediction and Assess the Predictions**

### When to Use Machine Learning
- Use when the task involves a lot of data and no clear formula.
- Applications: face and speech recognition, fraud detection, automated trading, energy demand forecasting, predicting shopping trends.

### Supervised vs. Unsupervised Learning
- **Supervised Learning**: Trains a model with known inputs and outputs to predict future outputs (e.g., email classification, tumor detection).
  - Techniques: Classification, Regression
- **Unsupervised Learning**: Analyzes data to uncover patterns without labeled answers.
  - Technique: Clustering

### Classification, Regression, and Clustering
- **Classification**: Predicts discrete outcomes (e.g., spam detection).
  - Algorithms: Decision Trees, Logistic Regression, SVM
- **Regression**: Predicts continuous outcomes (e.g., stock prices).
  - Algorithms: Linear Regression, Polynomial Regression
- **Clustering**: Groups data based on similarities.
  - Algorithms: K-Means, Hierarchical Clustering

### Common Machine Learning Algorithms
- **Bayesian**: Useful with limited data.
- **Clustering**: Groups similar data points.
- **Decision Tree**: Visualizes possible outcomes.
- **Dimensionality Reduction**: Removes redundant data.
- **Instance-Based**: Classifies new data based on training data.
- **Neural Networks and Deep Learning**: Solves problems like human brain, adapts to new information.
- **Linear Regression**: Measures relationships between data points.
- **Regularization**: Avoids overfitting.
- **Rule-Based**: Uses rules to describe data relationships.

### Examples of Supervised Learning Techniques
- **Classification**: Predicts categories (e.g., spam detection).
- **Regression**: Predicts continuous variables (e.g., stock prices).

### Examples of Unsupervised Learning Techniques
- **Clustering**: Finds hidden patterns (e.g., market research).

### Important Considerations in Machine Learning
- Data preprocessing requires specialized knowledge.
- Finding the best model takes time.
- Machine learning relies on trial and error.

### Choosing the Right Algorithm
- **Supervised Learning**: For predictions with known data.
- **Unsupervised Learning**: For exploring unknown patterns.

### Progress Check Questions
1. **Discuss the various phases of Machine Learning.**
2. **When should we use machine learning?**
3. **Compare the concepts of Classification, Regression, and Clustering. List the algorithms in respective categories.**


## 9.4 Reinforcement Learning and Algorithms

### Introduction

- **Learning Categories**: Supervised, Unsupervised, Semi-supervised, Reinforcement Learning (RL), Deep Learning (DL), Adaptive Learning.
- **Focus**: Introduction to Reinforcement Learning.

### Reinforcement Learning (RL)

- **Concept**: Algorithms receive instructions and figure out tasks by trial and error, receiving rewards or punishments.
- **Agent and Environment Interaction**: The agent interacts with the environment, making decisions that are rewarded or punished, which helps in learning the best actions.

#### Key Terms in RL

1. **Agent**: Learns and makes decisions.
2. **Environment**: Where the agent learns and acts.
3. **Action**: Possible moves the agent can take.
4. **State**: Current situation of the agent in the environment.
5. **Reward**: Feedback for actions, can be positive or negative.
6. **Policy**: Agent's strategy for deciding actions.
7. **Value Function**: Maps states to long-term rewards.
8. **Function Approximator**: Approximates functions based on training examples (e.g., decision trees, neural networks).
9. **Model**: Agent's understanding of the environment, mapping state-action pairs to state probability distributions.

### RL Algorithms

- **Categories**: Model-Free and Model-Based
  - **Model-Based RL**: Uses a model to simulate environment dynamics.
  - **Model-Free RL**: Learns through trial and error without storing all state-action combinations.

#### Model-Free RL

- **Policy Optimization**: Subclass of Model-Free RL.
  - **On-Policy**: Learns value based on the current action from the current policy.
  - **Off-Policy**: Learns value based on actions from another policy (e.g., greedy policy in Q-learning).

- **Q-Learning**: 
  - Acquires the action-value function.
  - Determines the value of performing an action in a state.
  - Uses a scalar value for actions based on states.

- **SARSA (State-Action-Reward-State-Action)**:
  - Variation of Q-Learning.
  - **On-Policy**: Learns value function based on current policy's actions.
  - **Off-Policy**: Uses another policy's actions to learn value function.
  - **Q-Learning**: Off-Policy, uses greedy learning strategy.
  - **SARSA**: On-Policy, uses current policy's actions to learn Q-value.

#### Deep Q Neural Network (DQN)

- **Concept**: Q-learning with neural networks.
- **Application**: Useful in large state-space environments where defining a Q-table is complex and time-consuming.
- **Approach**: Neural networks approximate Q-values for each action based on the state.

### Applications

- **Unsupervised Learning**: Text mining, facial recognition, city planning, targeted marketing.
- **Supervised Learning**: Fraud detection, spam detection, diagnostics, image classification, score prediction.
- **Reinforcement Learning**: Gaming, manufacturing, inventory management, financial sector.

### Check Your Progress

- **Q6**: What is Reinforcement Learning? List the components involved in it.
- **Q7**: Briefly discuss the various algorithms of Reinforcement Learning.


## 9.5 Deep Learning and Algorithms

### Introduction

- **Deep Learning (DL)**: A subset of machine learning using artificial neural networks and representation learning.
- **Applications**: Computer vision (image), natural language processing (text), automated speech recognition (audio).
- **Architecture**: Deep neural networks, with multiple layers compared to traditional neural networks.

### Relationship Between AI, ML, and DL

- **Artificial Intelligence (AI)**: Broad field encompassing various techniques.
- **Machine Learning (ML)**: Subset of AI focused on learning from data.
- **Deep Learning (DL)**: Subset of ML, primarily using neural networks inspired by the human brain.

### Neural Networks

- **Neurons**: Basic units, taking input signals, multiplying by weights, adding, and applying a non-linear function.
- **Layers**: Input layer, multiple hidden layers, and an output layer.
- **Deep Neural Networks**: Multiple layers for complex processing.

### Key Deep Learning Algorithms

1. **Back Propagation Neural Networks (BPNN)**
   - **Concept**: Iterative learning by adjusting weights based on errors.
   - **Process**: Uses stochastic gradient descent to minimize errors.
   - **Example**: Recognizing images with trees by iterative learning.

2. **Feed-forward Neural Networks (FNN)**
   - **Structure**: Fully connected neurons between layers.
   - **Multilayer Perceptron (MLP)**: Learns non-linear associations, unlike single-layer perceptrons.
   - **Applications**: Classification and regression tasks.

3. **Convolutional Neural Networks (CNN)**
   - **Function**: Uses convolution to connect neurons to a limited number of subsequent neurons.
   - **Applications**: Computer vision tasks like image classification, video identification, and medical image analysis.
   - **Advantages**: Regularizes feed-forward networks to prevent overfitting.

4. **Recurrent Neural Networks (RNN)**
   - **Concept**: Utilizes feedback loops to process sequential data.
   - **Applications**: Time series forecasting, language translation, speech production, text-to-speech synthesis.
   - **Advanced Structures**: GRU units and LSTM units for improved performance.

5. **Recursive Neural Networks**
   - **Structure**: Arranged in a tree-like manner.
   - **Applications**: NLP tasks like audio-to-text transcription and sentiment analysis.

6. **Auto-Encoders (AEN)**
   - **Type**: Unsupervised technique for dimensionality reduction and data compression.
   - **Components**: Encoder (compresses data) and Decoder (reconstructs data).

7. **Restricted Boltzmann Machines (RBM)**
   - **Type**: Stochastic neural networks with generative capabilities.
   - **Structure**: Only input and hidden layers, no output layer.
   - **Deep Belief Networks**: Multiple RBMs stacked together.

8. **Generative Adversarial Networks (GANs)**
   - **Concept**: Two models - Generator (creates fake data) and Discriminator (identifies fake data).
   - **Applications**: Video games, astronomical imagery, interior design, fashion.
   - **Example**: Creating realistic fake images.

9. **Transformers**
   - **Usage**: Mainly in language applications.
   - **Concept**: Based on attention mechanisms to focus on relevant data parts.
   - **Components**: Stacked encoders and decoders with attention layers.

10. **Graph Neural Networks (GNN)**
    - **Function**: Models graph data, converting node connections into embeddings.
    - **Applications**: Social networks, chemical molecules, knowledge graphs, location information.
    - **Tasks**: Grouping, classifying, etc.

### Check Your Progress

- **Q8**: What is Deep Learning? How does it relate to AI & ML?
- **Q9**: Briefly discuss the various algorithms of Reinforcement Learning.

## 9.6 Ensemble Methods

### Introduction

- **Ensemble Learning**: Combines predictions from different models to improve predictive performance.
- **Primary Methods**:
  - Bagging
  - Stacking
  - Boosting

### Bagging Ensemble Learning

- **Concept**: Fits multiple decision trees to various samples of the same dataset and averages the results.
- **Process**:
  - Use bootstrap sampling to create different samples of the training dataset.
  - Fit unpruned decision trees on each sample.
  - Combine predictions using voting or averaging.
- **Bootstrap Sample**:
  - Randomly selects rows (examples) from the dataset with replacement.
  - A row can be selected multiple times.
- **Popular Algorithms**:
  - Bagged Decision Trees
  - Random Forest
  - Extra Trees

### Stacking Ensemble Learning

- **Concept**: Fits multiple types of models to the same data and uses another model to combine predictions.
- **Levels of Models**:
  - Level-0: Individual models that make predictions.
  - Level-1: Model that combines predictions from level-0 models.
- **Process**:
  - Fit various machine learning models to the same dataset.
  - Use a meta-model to learn how to combine these predictions.
- **Popular Algorithms**:
  - Stacked Models
  - Blending
  - Super Ensemble

### Boosting Ensemble Learning

- **Concept**: Successively adds ensemble members to correct prior model predictions, creating a weighted average.
- **Process**:
  - Adjust training data to focus on examples that earlier models predicted incorrectly.
  - Add ensemble members one at a time to refine predictions.
  - Combine predictions using a weighted average.
- **Weak Learners**:
  - Typically simple decision trees.
  - Each weak learner makes small improvements.
- **Popular Algorithms**:
  - AdaBoost
  - Gradient Boosting Machines
  - Stochastic Gradient Boosting (e.g., XGBoost)

### Key Elements Summary

- **Bagging**:
  - Samples training data using bootstrapping.
  - Fits unpruned decision trees on each sample.
  - Uses voting or averaging for predictions.
- **Stacking**:
  - Uses unchanged training dataset.
  - Fits different machine learning algorithms.
  - Uses a meta-model to combine predictions.
- **Boosting**:
  - Gives more weight to hard-to-predict examples.
  - Adds ensemble members one by one.
  - Uses weighted average for predictions.

### Check Your Progress

- **Q10**: What is Ensemble Learning?
- **Q11**: Briefly discuss the various Ensemble Methods.

