## Cook

**函数原型**

```csharp
Food Cook(List<int> ingredients, bool learnRecipe = true);
```

**描述**

使用给定的原料烹饪食物。

**参数**

- `ingredients`: List<int>类型，表示原料的ID列表。
- `learnRecipe`: bool类型，表示烹饪后是否学习该食谱，默认为true。

**返回值**

- `Food`: 烹饪出的食物。

------

## CookAll

**函数原型**

```csharp
List<Food> CookAll(List<int> ingredients, int count, bool learnRecipe = true);
```

**描述**

使用给定的原料批量烹饪食物。

**参数**

- `ingredients`: List<int>类型，表示原料的ID列表。
- `count`: int类型，表示烹饪的数量。
- `learnRecipe`: bool类型，表示烹饪后是否学习该食谱，默认为true。

**返回值**

- `List<Food>`: 批量烹饪出的食物列表。

------

## GetRecipe

**函数原型**

```csharp
Recipe GetRecipe(int id);
```

**描述**

获取特定ID的食谱信息。

**参数**

- `id`: int类型，表示食谱ID。

**返回值**

- `Recipe`: 对应ID的食谱信息。

------

## GetRandomRecipe

**函数原型**

```csharp
void GetRandomRecipe();
```

**描述**

随机获取一份食谱。

**参数**

- NULL

**返回值**

- NULL