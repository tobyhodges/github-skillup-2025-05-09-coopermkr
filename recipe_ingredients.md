---
title: "Cinnamon Roll Ingredients"
teaching: 10
exercises: 2
---

:::::::::::::::::::::::::::::::::::::: questions 

- What are the ingredients needed for the cinnamon rolls?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Be able to put together your shopping list
- Convert between metric and imperial units, if necessary
- Double the recipe if you're really hungry

::::::::::::::::::::::::::::::::::::::::::::::::




## Ingredients

There are 3 main components to this recipe: the main ingredients for the dough, the ingredients for the cinnamon-sugar filling, and the ingredients for the glaze.

### Dough Ingredients


``` r
main_ingredients <- tribble(
  ~ingredient, ~amount_imperial, ~amount_grams,
  "butter (cold)", "8 tablespoons", 113,
  "all-purpose flour", "2 ½ cups", 300,
  "sourdough starter discard", "⅓ cup", 100,
  "buttermilk", "1 cup", 240,
  "honey or granulated sugar", "1 tbsp + 1 tsp", 25,
  "fine sea salt", "¾ teaspoon", 4,
  "baking powder", "1 tsp", NA,
  "baking soda", "½ cup", NA)

main_ingredients %>% 
  kableExtra::kable(align = "r")
```



|                ingredient| amount_imperial| amount_grams|
|-------------------------:|---------------:|------------:|
|             butter (cold)|   8 tablespoons|          113|
|         all-purpose flour|        2 ½ cups|          300|
| sourdough starter discard|           ⅓ cup|          100|
|                buttermilk|           1 cup|          240|
| honey or granulated sugar|  1 tbsp + 1 tsp|           25|
|             fine sea salt|      ¾ teaspoon|            4|
|             baking powder|           1 tsp|           NA|
|               baking soda|           ½ cup|           NA|

::::::::::::::::::::::::::::: callout

**Recipe modifications:**

You can use **active** sourdough starter instead of discard, if you so choose. There will be a slight modification to the recipe if that is the case.

In warmer climates, you may want to reduce the amount of buttermilk and/or increase the amount of flour to produce a less sticky, more manageable dough. You may have to experiment a bit.

:::::::::::::::::::::::::::::

### Cinnamon-sugar filling


``` r
filling_ingredients <- tribble(
  ~ingredient, ~amount_imperial, ~amount_grams,
  "light brown sugar", "¾ cup", 150,
  "ground cinnamon", "2 teaspoons", NA,
  "butter (melted)", "4 tablespoons", 56)

filling_ingredients %>% 
  kableExtra::kable(align = "r")
```



|        ingredient| amount_imperial| amount_grams|
|-----------------:|---------------:|------------:|
| light brown sugar|           ¾ cup|          150|
|   ground cinnamon|     2 teaspoons|           NA|
|   butter (melted)|   4 tablespoons|           56|


### Glaze 


``` r
glaze_ingredients <- tribble(
  ~ingredient, ~amount_imperial, ~amount_grams,
  "powdered sugar", "1 cup", 120,
  "butter (melted)", "1 tablespoon", 14,
  "vanilla extract", "1 teaspoon", 5,
  "milk", "2 tablespoons", 30)

glaze_ingredients %>% 
  kableExtra::kable(align = "r")
```



|      ingredient| amount_imperial| amount_grams|
|---------------:|---------------:|------------:|
|  powdered sugar|           1 cup|          120|
| butter (melted)|    1 tablespoon|           14|
| vanilla extract|      1 teaspoon|            5|
|            milk|   2 tablespoons|           30|

::::::::::::::::::::::::::::::::::::: instructor

It's worth emphasizing to your learners that there are many valid ways of accomplishing this task in R, whether using a `tidyverse` or base R approach.

::::::::::::::::::::::::::::::::::::: 


::::::::::::::::::::::::::::::::::::: challenge

Add a column to `main_ingredients` that has the amount in ounces (weight, not fluid oz).

::::::::::::::::::::::::::::::::::::: solution


``` r
main_ingredients <- main_ingredients %>% 
  mutate(amount_oz = amount_grams * 0.035274)

main_ingredients
```

``` output
# A tibble: 8 × 4
  ingredient                amount_imperial amount_grams amount_oz
  <chr>                     <chr>                  <dbl>     <dbl>
1 butter (cold)             8 tablespoons            113     3.99 
2 all-purpose flour         2 ½ cups                 300    10.6  
3 sourdough starter discard ⅓ cup                    100     3.53 
4 buttermilk                1 cup                    240     8.47 
5 honey or granulated sugar 1 tbsp + 1 tsp            25     0.882
6 fine sea salt             ¾ teaspoon                 4     0.141
7 baking powder             1 tsp                     NA    NA    
8 baking soda               ½ cup                     NA    NA    
```


::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::
