# Machine Learning Ratatouille Recipes

This project uses machine learning to predict the skills and tools needed to make Ratatouille based on an ingredient list.

# Background

I was interested in a situation where a collection of input variables were known and I needed to predict what outputs would be needed. For example, in preparing a room for a medical procedure, it would be useful to know what tools and pharmaceutical to have on hand for the procedure.

The situation also maps to the kitchen: given a collection of ingredients, what skills and tools will be needed to make a recipe?

# Source Code

I gathered a dozen Ratatouille recipes from various sources and used them as a template for generating variations. The R script that generates the recipe variations is [here](/src/Recipe_Generator.Rmd).

Once I had the [recipe variations](/data/generated_recipes.csv), I developed an algorithm that goes through the recipe, learns the patterns associated with each skill, then predicts the skills needed for a testing set of the data. There are two variations of this algorithm:

1. [Using logistic regression] (/src/Recipe_Predictions.Rmd)
2. [Using XGBoost] (/src/Recipe_Predictions_xgboost.Rmd)

The algorithm was developed using [this set of test data](/src/Recipe_ML_testing.Rmd)
