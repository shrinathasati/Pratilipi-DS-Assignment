# Pratilipi Story Recommendation System

A recommendation system that predicts which stories (pratilipis) users are likely to read based on historical reading behavior data.

## Project Overview

This project implements a Collaborative Filtering approach using Singular Value Decomposition (SVD) to create personalized story recommendations. The system analyzes past user interactions with stories and metadata to predict and recommend relevant content to users.

## Dataset Links

1. [User Interaction Dataset](https://drive.google.com/file/d/1DLhc8_3UHAiUhSGtcp5vjRMWPJLcYMuA/view)
2. [Story Metadata Dataset](https://drive.google.com/file/d/1RRvZIsp9AUlNrWHVGYYNflLbQsfMn6qM/view)
3. [Project Documentation](https://drive.google.com/file/d/1pHGpJpBmqiMiPetRoo01FHc0ewrLbIy5/view?usp=sharing)

## Dependencies

Install the required packages using:

```bash
pip install pandas numpy matplotlib seaborn surprise
```

Or install from requirements.txt:

```bash
pip install -r requirements.txt
```

## How to Run

1. Clone this repository:
```bash
git clone [https://github.com/yourusername/pratilipi-recommendation-system.git](https://github.com/shrinathasati/Pratilipi-DS-Assignment.git)
cd pratilipi-recommendation-system
```

2. Download the datasets and place them in your project directory:
   - Rename them to `user_interaction.csv` and `metadata.csv`

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Run the main script:
```bash
python main.ipynb
```

## Code Structure

The system performs the following steps:

1. Data Loading and Preprocessing
   - Loads user interactions and metadata
   - Handles missing values
   - Converts data types
   - Merges datasets

2. Feature Engineering
   - Creates temporal features
   - Encodes categorical variables
   - Normalizes numerical features

3. Model Training (SVD)
   - Splits data (75% training, 25% testing)
   - Trains SVD model
   - Performs cross-validation

4. Recommendation Generation
   - Predicts top 5 stories for users
   - Evaluates using precision and accuracy metrics

5. Visualization
   - Read percentage distribution
   - Popular stories analysis
   - Category distribution

## Output

The system generates:

1. Top 5 story recommendations for each user
2. Performance metrics:
   - Precision@5
   - Accuracy@5
   - RMSE
   - MAE
3. Visualization plots:
   - Read percentage distribution
   - Top 10 most popular stories
   - Category-wise story distribution

## Model Performance

The model uses Singular Value Decomposition (SVD) for collaborative filtering and achieves:
- Strong predictive accuracy on unseen data
- Effective handling of sparse user-item interactions
- Scalable recommendations for new users and stories

## Files Description

- `main.py`: Main script containing all the code
- `requirements.txt`: List of Python dependencies
- `documentation.pdf`: Detailed project documentation
- `README.md`: This file
- Dataset files (to be downloaded):
  - `user_interaction.csv`: User reading behavior data
  - `metadata.csv`: Story metadata information

## Future Improvements

1. Implement content-based filtering
2. Add real-time recommendation capabilities
3. Include more user behavioral features
4. Optimize model hyperparameters
5. Add support for cold-start problems
