## GetCurrentUpdateExpNeed

**函数原型**

```csharp
int GetCurrentUpdateExpNeed(Personal p);
```

**描述**

获取特定人物当前升级所需的经验值。

**参数**

- `p`: Personal类型，表示人物。

**返回值**

- `int`: 当前升级所需的经验值。

------

## GetExp

**函数原型**

```csharp
void GetExp(Personal p, int value, bool NeedDialog, string Text);
```

**描述**

为特定人物增加经验值。

**参数**

- `p`: Personal类型，表示人物。
- `value`: int类型，表示增加的经验值。
- `NeedDialog`: bool类型，表示是否需要对话框。
- `Text`: string类型，表示相关文本（用于对话框）。

**返回值**

- NULL

------

## GetExpAll

**函数原型**

```csharp
void GetExpAll(int value);
```

**描述**

为所有人物增加经验值。

**参数**

- `value`: int类型，表示增加的经验值。

**返回值**

- NULL

------

## CheckArrivedCity

**函数原型**

```csharp
id CheckArrivedCity(CityData City, bool Heard = false);
```

**描述**

检查是否到达特定城市。

**参数**

- `City`: CityData类型，表示城市数据。
- `Heard`: bool类型，表示是否听说过该城市，默认为false。

**返回值**

- `id`: 到达城市的结果标识。

------

## CheckFirstMeetEvent

**函数原型**

```csharp
void CheckFirstMeetEvent(int TempID, string TempName, bool Heard = false);
```

**描述**

检查首次遇见事件。

**参数**

- `TempID`: int类型，表示事件临时ID。
- `TempName`: string类型，表示事件临时名称。
- `Heard`: bool类型，表示是否听说过该事件，默认为false。

**返回值**

- NULL

------

## CheckFirstMeetPeople

**函数原型**

```csharp
void CheckFirstMeetPeople(int PeopleID, bool Heard = false);
```

**描述**

检查首次遇见特定人物。

**参数**

- `PeopleID`: int类型，表示人物ID。
- `Heard`: bool类型，表示是否听说过该人物，默认为false。

**返回值**

- NULL

------

## CheckPeopleInCar

**函数原型**

```csharp
void CheckPeopleInCar();
```

**描述**

检查车内是否有人物。

**参数**

- NULL

**返回值**

- NULL

------

## CheckUnusedPoint

**函数原型**

```csharp
bool CheckUnusedPoint(Personal p);
```

**描述**

检查特定人物是否有未使用的升级点数。

**参数**

- `p`: Personal类型，表示人物。

**返回值**

- `bool`: 是否有未使用的升级点数。

------

## GetUpgradePoint

**函数原型**

```csharp
int GetUpgradePoint(Personal p, string Type);
```

**描述**

获取特定人物特定类型的升级点数。

**参数**

- `p`: Personal类型，表示人物。
- `Type`: string类型，表示升级点数的类型。

**返回值**

- `int`: 特定类型的升级点数。

---

## GetUpgradeBookUse

**函数原型**

```csharp
int GetUpgradeBookUse(Personal p, string Type);
```

**描述**

获取特定人物在特定类型上使用的升级书籍数量。

**参数**

- `p`: Personal类型，表示人物。
- `Type`: string类型，表示升级类型。

**返回值**

- `int`: 使用的升级书籍数量。

------

## UsePointToUpgrade

**函数原型**

```csharp
void UsePointToUpgrade(Personal p, string Type, string TypeName);
```

**描述**

使用升级点数对特定人物进行升级。

**参数**

- `p`: Personal类型，表示人物。
- `Type`: string类型，表示升级类型。
- `TypeName`: string类型，表示升级名称。

**返回值**

- NULL

------

## UsePointToGetBuff

**函数原型**

```csharp
void UsePointToGetBuff(Personal b, int Book);
```

**描述**

使用升级点数获取特定人物的增益效果。

**参数**

- `b`: Personal类型，表示人物。
- `Book`: int类型，表示使用的书籍数量。

**返回值**

- NULL

------

## UseBuffToGetPoint

**函数原型**

```csharp
void UseBuffToGetPoint(Personal b, int Book);
```

**描述**

使用增益效果获取特定人物的升级点数。

**参数**

- `b`: Personal类型，表示人物。
- `Book`: int类型，表示使用的书籍数量。

**返回值**

- NULL

------

## UsePointToRemoveBuff

**函数原型**

```csharp
void UsePointToRemoveBuff(Personal b, int Book);
```

**描述**

使用升级点数移除特定人物的增益效果。

**参数**

- `b`: Personal类型，表示人物。
- `Book`: int类型，表示使用的书籍数量。

**返回值**

- NULL

------

## RemoveBuffToGetPoint

**函数原型**

```csharp
void RemoveBuffToGetPoint(Personal b, int Book);
```

**描述**

移除增益效果以获取特定人物的升级点数。

**参数**

- `b`: Personal类型，表示人物。
- `Book`: int类型，表示使用的书籍数量。

**返回值**

- NULL

------

## UpgradeCityPeopleCityExp

**函数原型**

```csharp
void UpgradeCityPeopleCityExp();
```

**描述**

升级城市居民的城市经验。

**参数**

- NULL

**返回值**

- NULL

------

## UpdateCityPeopleMeetPeople

**函数原型**

```csharp
void UpdateCityPeopleMeetPeople(int PeopleID);
```

**描述**

更新城市居民遇见特定人物的记录。

**参数**

- `PeopleID`: int类型，表示人物ID。

**返回值**

- NULL