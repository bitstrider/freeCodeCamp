---
title: First
localeTitle: 第一
---# 第一

返回满足可选给定条件的第一个元素。如果未找到任何元素，则抛出`InvalidOperationException` ;

### 签名

```csharp
Enumerable.First<TSource>(IEnumerable<TSource>, Func<TSource, Boolean>) 
```

## 例

```csharp
var fruits = new List<Fruit>() { 
    new Fruit() { Id = 1, Name = "Orange",     Color = "Orange", Quantity: 3   }, 
    new Fruit() { Id = 2, Name = "Strawberry", Color = "Red",    Quantity: 12  }, 
    new Fruit() { Id = 3, Name = "Grape",      Color = "Purple", Quantity: 25  }, 
    new Fruit() { Id = 4, Name = "Pineapple",  Color = "Yellow", Quantity: 1   }, 
    new Fruit() { Id = 5, Name = "Apple",      Color = "Red",    Quantity: 5   }, 
    new Fruit() { Id = 6, Name = "Mango",      Color = "Yellow", Quantity: 2   } 
 }; 
 
 var firstFruit = fruits.First(); // Orange 
 
 var firstYellowFruit = fruits.First(f => f.Color == "Yellow"); // Pineapple 

```