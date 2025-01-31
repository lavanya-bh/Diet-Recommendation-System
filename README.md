# Personalized Diet Recommendation System

This is a personalized diet recommendation system designed to suggest recipes based on user preferences, body mass index (BMI), and fitness goals. The system uses a combination of K-Nearest Neighbors (KNN) and content-based filtering to recommend recipes that align with the user's dietary needs. The application is built using **Python**, **Streamlit**, **Pandas**, **Plotly**, and **Scikit-Learn**.

## Features

- **User Inputs**: 
  - Age
  - Height (cm)
  - Weight (kg)
  - Goal (weight loss, muscle gain, weight gain, maintenance)
  - Diet preference (veg, non-veg, or mixed)
  - Exclude ingredients (optional)
  
- **Recipe Recommendations**: 
  - Personalized recipe suggestions based on BMI and fitness goals.
  - Option to exclude certain ingredients.
  - Display of the top 5 recommended recipes with detailed nutritional information.
  
- **Nutritional Breakdown**:
  - Nutrient analysis of the top recommended recipe (calories, protein, carbohydrates, fiber).
  - Interactive pie chart for easy visualization.

- **Download Option**: 
  - Download the top 5 recommended recipes as a text file.

## Requirements

To run this project locally, you'll need the following dependencies:

- Python 3.x
- Streamlit
- Pandas
- Plotly
- Scikit-Learn

You can install the required libraries by running:

```
pip install -r requirements.txt
```

## How to Use

1. Clone this repository:
    ```
    git clone https://github.com/your-username/diet-recommendation-app.git
    ```
   
2. Navigate to the project folder:
    ```
    cd diet-recommendation-app
    ```

3. Run the Streamlit app:
    ```
    streamlit run diet_recommendation_app.py
    ```

4. Open the provided link in your browser to interact with the app.

5. Enter your details (age, height, weight, goal, diet preference) and click "Get Recommendations" to receive personalized diet recommendations.

## How It Works

- **Data Preprocessing**: The app processes a dataset of recipes (with nutritional values and ingredients) and scales the nutritional features using **StandardScaler** for better comparison.
  
- **K-Nearest Neighbors (KNN)**: The system uses the KNN algorithm to find the most similar recipes based on the nutritional content, using **cosine similarity** as the distance metric. The value of **k** is set to 5, meaning the system recommends the top 5 most similar recipes.

- **Content-Based Filtering**: Based on the user’s preferences (BMI, goal, diet type, and excluded ingredients), the app filters the dataset to display the most relevant recipes.

## Dataset

The dataset used in this project contains nutritional information and ingredient details for various recipes. Ensure that the dataset (CSV file) is placed at the correct location, or you can modify the code to load from a different file path.

## File Structure

- `diet_recommendation_app.py`: Main Streamlit application file.
- `requirements.txt`: List of required Python libraries.
- `dataset.csv`: The CSV file containing the recipe details (make sure to place the dataset in the correct directory).

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- **Streamlit** for the interactive app framework.
- **Scikit-Learn** for the machine learning models.
- **Plotly** for data visualization.

---

This README should provide an overview of the project, how to set it up, how it works, and the tools used. You can modify it based on the exact structure of your project and any additional features you may have added.
