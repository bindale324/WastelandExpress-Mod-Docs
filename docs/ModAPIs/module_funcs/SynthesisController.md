## GetInformation

**函数原型**

```csharp
List<int> GetInformation(int id);
```

**描述**

获取特定ID的合成信息。

**参数**

- `id`: int类型，表示合成ID。

**返回值**

- `List<int>`: 合成信息列表。

------

## HaveSynsMenu

**函数原型**

```csharp
int HaveSynsMenu(string goodsID);
```

**描述**

检查是否拥有特定商品的合成菜单。

**参数**

- `goodsID`: string类型，表示商品ID。

**返回值**

- `int`: 合成菜单的状态。

------

## GetPercentage

**函数原型**

```csharp
float GetPercentage(int ID, float Rate = 1);
```

**描述**

获取特定合成ID的成功率。

**参数**

- `ID`: int类型，表示合成ID。
- `Rate`: float类型，表示额外影响率，默认为1。

**返回值**

- `float`: 合成成功率。

------

## GetLearnPercentage

**函数原型**

```csharp
float GetLearnPercentage(int ID);
```

**描述**

获取学习特定合成ID的成功率。

**参数**

- `ID`: int类型，表示合成ID。

**返回值**

- `float`: 学习合成成功率。

------

## CraftSynthesis

**函数原型**

```csharp
bool CraftSynthesis(int id, int cout, float Percentage, out int PlusLevel);
```

**描述**

进行合成操作。

**参数**

- `id`: int类型，表示合成ID。
- `cout`: int类型，表示合成数量。
- `Percentage`: float类型，表示成功率。
- `PlusLevel`: out int类型，输出合成等级。

**返回值**

- `bool`: 操作是否成功。

------

## LearnSynthesis

**函数原型**

```csharp
bool LearnSynthesis(int id, float Percentage, int BookCount);
```

**描述**

学习合成技能。

**参数**

- `id`: int类型，表示合成ID。
- `Percentage`: float类型，表示成功率。
- `BookCount`: int类型，表示书籍数量。

**返回值**

- `bool`: 学习是否成功。

------

## SynthesisCost

**函数原型**

```csharp
void SynthesisCost(int id, int cout);
```

**描述**

计算合成成本。

**参数**

- `id`: int类型，表示合成ID。
- `cout`: int类型，表示合成数量。

**返回值**

- NULL

------

## GetMenu

**函数原型**

```csharp
void GetMenu(int ID);
```

**描述**

获取特定ID的合成菜单。

**参数**

- `ID`: int类型，表示菜单ID。

**返回值**

- NULL

------

## GetRandomMenu

**函数原型**

```csharp
void GetRandomMenu();
```

**描述**

获取随机合成菜单。

**参数**

- NULL

**返回值**

- NULL

------

## IsAllSynsMenu

**函数原型**

```csharp
bool IsAllSynsMenu();
```

**描述**

检查是否拥有所有合成菜单。

**参数**

- NULL

**返回值**

- `bool`: 是否拥有所有合成菜单。