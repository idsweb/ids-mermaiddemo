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
 ## Chapter 2
 __Note__ Items are now singular and ingredient is now food item. Day is now Entry

 ```mermaid
classDiagram-v2
    Dieter --> Diary : Keeps a
    Dieter *-- Statistic : Tracks their
    Dieter *-- Favourite : Saves their

    Diary *-- Entry : Made up of

    Meal o-- Item
    Meal o-- Favourite

    Breakfast --|> Meal : Implements
    Lunch --|> Meal : Implements
    Dinner --|> Meal : Implements

    Favourite o-- Item

    Item o-- Nutrition

    Snack o-- Item : Can be
    
    Weight --|> Statistic
    Measurement --|> Statistic

    Entry o-- Meal
    Entry o-- Snack
 ```
