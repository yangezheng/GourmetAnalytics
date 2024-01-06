# Gourmet Analytics

GOAL:  Use  these  data  sets  to  develop  a  model  that  can  predict  the  outcome  of  the  column  Like,  which 
indicates  whether  a  customer  likes  a  recipe  (your  model  predicts  Like=1)  or  dislikes  it  (your  model  predicts 
Like=0).  
For  reviews  with  a  TestSetId  and  for  which  you  are  not  given  the  Like  (the “private  test  set”), you must make 
predictions  that  will  form  your  submission.  See  the  “submission_template.csv”  for  details  about  the  required 
format. Your project will be evaluated and graded based on these predictions.

## Files
```
.
│   Data Description.pdf
├── Data
│   ├── diet.csv
│   ├── recipes.csv
│   ├── requests.csv
│   ├── reviews.csv
│   └── submission_random.csv
```

## The data

### diet.csv 
Column | Description 
--------|-------------
AuthorId| (String, primary key) A unique identifier for the customer.
Diet |(String) The diet option of a user. 
Age |(Numeric) The age of the corresponding user.

### recipes.csv 

Column | Description 
--------|-------------
RecipeId |(Numeric, primary key) The unique identifier of a recipe. 
Name |(String) The name of the recipe. 
CookTime |(Numeric) The time it needs to cook the recipe. 
PrepTime |(Numeric) The time it needs to prepare the recipe. 
RecipeCategory |(String) A label indicating the type of the recipe. 
RecipeIngredientQuantities |(String) A label that represents the number of ingredients in the recipe.  
RecipeIngredientParts | (String) A label that contains the ingredients in the recipe. 
Calories 
FatContent 
SaturatedFatContent
CarbohydrateContent 
FiberContent 
SugarContent 
ProteinContent |(Numeric) The amount of Macronutrients in kcal/ g per 100g. 
SodiumContent 
CholesterolContent | (Numeric) Nutrition facts in mg per 100g 
RecipeServings |(Numeric) The number of servings that result from this recipe. 
RecipeYield |(String) The number of servings that result from this recipe.


### reviews.csv
Column | Description 
--------|-------------
AuthorId 
RecipeId | (String, foreign key) The unique identifier of a customer and a recipe. 
Rating |(Numeric) A rating between 1 and 5 that the users could submit to evaluate the difficulty of the recipe. 
Like |(Numeric) A label that indicates whether a user likes a recipe (=1) or not (=0). 
TestSetId| (Numeric) The unique identifier in the test set.

### requests.csv

Column | Description 
--------|-------------
AuthorId 
RecipeId | (String, Foreign keys) The unique identifiers of a user and a recipe. 
Time |(Numeric) The duration a recipe should take at most (including the time reserved for the preparation and cooking). 
HighCalories |(String) A flag that indicates whether the resulting meal/ beverage should have a high number of calories. 
LowFat |(Numkleric) A flag that indicates whether the resulting meal/ beverage should include a low amount of fat.  
HighProtein |(String) A flag indicating whether the resulting meal/ beverage has a high amount of proteins.  
LowSugar |(String) A flag indicates whether the resulting meal/beverage has low sugar. 
HighFiber |(Numeric) A flag indicates whether the resulting meal/beverage has high fiber.