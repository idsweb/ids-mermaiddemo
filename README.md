# ids-mermaiddemo
Sample project for the book Creating Software with Modern Diagramming Techniques

```
    Dieter -- FoodDiary
    Dieter *-- Statistics
    Entrys o-- Favourites
...
```
```mermaid
classDiagram-v2
    Dieter -- FoodDiary
    Dieter *-- Statistics
    Dieter *-- Favourites

    FoodDiary *-- Day

    Entrys o-- Ingredients
    Entrys o-- Favourites

    Favourites o-- Ingredients

    Ingredients o-- NutritionInfo

    Snacks o-- Ingredients
    Snacks o-- Favourites
    
    Statistics *-- Weights
    Statistics *-- WaistMeasurements

    Day o-- Entrys
    Day o-- Snacks
 ```
 ## Chapter 2
 __Note__ FoodItems are now singular and ingredient is now food FoodItem. Day is now Entry

 ```mermaid
 ---
 title: Diet App
 ---
classDiagram-v2
    Dieter "1" --> "1" FoodDiary : Keeps a
    Dieter "1" --> "0..*" Statistic : Tracks their
    Dieter "1" *-- "0..*" Favourite : Saves 
    
    FoodDataBank "1" -- "1..*" FoodItem : Is made up of

    FoodDiary "1" *-- "1..*" Day : Made up of

    Entry o-- FoodItem : Implements

    Breakfast --|> Entry : Implements
    Lunch --|> Entry : Implements
    Dinner --|> Entry : Implements
    Snack --|> Entry : Implements

    Day "1" o-- "1" Breakfast  : Has
    Day "1" o-- "1" Lunch : Has
    Day "1" o-- "1" Dinner : Has
    Day "1" o-- "1..*" Snack : Has

    Favourite o-- FoodItem : Implements

    FoodItem o-- NutritionInfo : Has
    
    Weight --|> Statistic : Is a kind of
    WaistMeasurement --|> Statistic : Is a kind of

    
 ```
