# 1. IMPORT LIBRARY
import pandas as pd

# 2. LOAD DATASET
recipes = pd.read_csv(r"C:\Users\SHWETA\Downloads\recipes (1).csv")

# 3. BASIC EXPLORATION
print(recipes)
print(recipes.shape)  # (1090, 15)
print(recipes.columns)
print(recipes.head())
print(recipes.tail())
print(recipes.info())

# 4. SEE FULL COLUMNS DATA (like in your screenshot)
print(recipes["url"])
print(recipes["cuisine_path"])
print(recipes["nutrition"])
print(recipes["timing"])
print(recipes["total_time"])
print(recipes["servings"])
print(recipes["yield"])

# 5. CREATE NEW DATAFRAME WITH ONLY 3 COLUMNS
recipe_data = recipes[["recipe_name", "rating", "prep_time"]]
print(recipe_data)  # [1090 rows x 3 columns]

# 6. HEAD - TOP 5 RECORDS
print(recipe_data.head())

# 7. EXTRACT RATING AS SERIES
recipe_rating = recipes["rating"]
print(recipe_rating)  # 0 to 1089, float64, Length: 1090

# 8. RATING HEAD - TOP 5
print(recipe_rating.head())
