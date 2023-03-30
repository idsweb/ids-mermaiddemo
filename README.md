# ids-mermaiddemo
Sample project for the book Creating Software with Modern Diagramming Techniques

```
    Dieter -- Diary
    Dieter *-- Statistics
    Meals o-- Favourites
...
```
```mermaid
classDiagram-v2
    Dieter -- Diary
    Dieter *-- Statistics
    Dieter *-- Favourites

    Diary *-- Day

    Meals o-- Ingredients
    Meals o-- Favourites

    Favourites o-- Ingredients

    Ingredients o-- Nutrition

    Snacks o-- Ingredients
    Snacks o-- Favourites
    
    Statistics *-- Weights
    Statistics *-- Measurements

    Day o-- Meals
    Day o-- Snacks
 ```
