## GetCurrentUpdateExpNeed

**函数原型**

```csharp
int GetCurrentUpdateExpNeed(Personal p);
```

**描述**

计算特定人物当前升级所需的经验值。

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

为所有人物增加经验值（见闻值）。（通常会在车上人员到达一个新地方的时候触发这个函数）

**参数**

- `value`: int类型，表示增加的经验值。

**返回值**

- NULL

------

## CheckArrivedCity

**函数原型**

```csharp
void CheckArrivedCity(CityData City, bool Heard = false);
```

**描述**

当团队到达某个城市之后，触发这个函数。该函数会遍历车上的每一个人，对这个城市的印象进行评价。

在游戏中看到的：

> xxx由于第一次 听说/来到 xxx，由于第一印象 好/坏 更喜欢/更讨厌 这个城市了。

就是这个函数触发的。

**参数**

- `City`: CityData类型，表示城市数据。
- `Heard`: bool类型，表示是听说，还是来到。

**返回值**

- NULL

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

检查车内的人物是否是第一次见面，如果是第一次见就会触发评价。

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

计算当前人物，对于某个`特性`的可升级点数。

+ 如果该`特性`的值已经大于了25，那么就只能+1
+ 如果没有大于25，那么会计算一次可以提升多少点。

**参数**

- `p`: Personal类型，表示人物。
- `Type`: string类型，表示您要进行升级的`特性`的名称。
  + **注意**：`Type`应该传入的是英文单词，具体有哪些string，您可以参考[Personal数据接口](/data_desc/Appendix.md#Personal)

**返回值**

- `int`: 特定类型的升级点数。

---

## GetUpgradeBookUse

**函数原型**

```csharp
int GetUpgradeBookUse(Personal p, string Type);
```

**描述**

计算特定人物在升级某个`特性`时，需要的书籍数量。

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

使用升级点数对特定人物进行升级。这个函数中会自动查询、扣除相应的经验点、书籍，最后完成对某个人物的某个`特性`的升级。

默认扣除1个技能点。

**参数**

- `p`: Personal类型，表示人物。
- `Type`: string类型，表示升级的`特性`的英文名。
  + 例如，如果您想升级战斗力，这里应该传入`_battle`。
- `TypeName`: string类型，表示升级的`特性`的中文名称。

**返回值**

- NULL

------

## UsePointToGetBuff

**函数原型**

```csharp
void UsePointToGetBuff(Personal b, int Book);
```

**描述**

使用升级点数获取特定人物的增益效果。也可能会因此获得一个负面属性。

默认扣除2个技能点。

每个人最多能获得8个buff。

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

获得一个负面buff，从而获取特定人物的升级点数。

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

默认扣除3个技能点。

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

移除正面效果以获取特定人物的技能点。

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