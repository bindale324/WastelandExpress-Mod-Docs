## UpdateCityMatrial

**函数原型**

```csharp
void UpdateCityMatrial();
```

**描述**

更新城市的物资数据。

**参数**

- NULL

**返回值**

- NULL

------

## CityCanSearch

**函数原型**

```csharp
bool CityCanSearch(int cityId, out int grade);
```

**描述**

检查特定城市是否可以进行搜索，并获取等级。

**参数**

- `cityId`: int类型，表示城市ID。
- `grade`: out int类型，输出搜索等级。

**返回值**

- `bool`: 城市是否可以进行搜索。

------

## ShowSearch

**函数原型**

```csharp
void ShowSearch(int cityId, float mult);
```

**描述**

显示特定城市的搜索结果。

**参数**

- `cityId`: int类型，表示城市ID。
- `mult`: float类型，表示搜索倍率。

**返回值**

- NULL