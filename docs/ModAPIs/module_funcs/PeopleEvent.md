## CalAllPeople

**函数原型**

```csharp
void CalAllPeople();
```

**描述**

计算所有人物的状态。

**参数**

- NULL

**返回值**

- NULL

------

## CalPeople

**函数原型**

```csharp
void CalPeople(Personal a);
```

**描述**

计算特定人物的状态。

**参数**

- `a`: Personal类型，表示人物。

**返回值**

- NULL

------

## CurePeople

**函数原型**

```csharp
bool CurePeople(int i, Items item);
```

**描述**

治疗特定人物。

**参数**

- `i`: int类型，表示人物ID。
- `item`: Items类型，表示用于治疗的物品。

**返回值**

- `bool`: 操作是否成功。

------

## SelfCityCurePeople

**函数原型**

```csharp
bool SelfCityCurePeople(int cityId, int mapId, Personal personal, bool money);
```

**描述**

在自建城市中治疗特定人物。

**参数**

- `cityId`: int类型，表示城市ID。
- `mapId`: int类型，表示地图ID。
- `personal`: Personal类型，表示人物。
- `money`: bool类型，表示是否使用金钱进行治疗。

**返回值**

- `bool`: 操作是否成功。

------

## FixPeople

**函数原型**

```csharp
void FixPeople(int value, int hero);
```

**描述**

维修机器人。

**参数**

- `value`: int类型，表示维修值。
- `hero`: int类型，表示机器人ID。

**返回值**

- NULL

------

## DrinkPeople

**函数原型**

```csharp
void DrinkPeople(int i, Items item);
```

**描述**

让特定人物喝酒。

**参数**

- `i`: int类型，表示人物ID。
- `item`: Items类型，表示饮料。

**返回值**

- NULL

------

## DriverUpdate

**函数原型**

```csharp
void DriverUpdate();
```

**描述**

更换司机。

**参数**

- NULL

**返回值**

- NULL

------

## PeopleDrinkWater

**函数原型**

```csharp
void PeopleDrinkWater(int hero);
```

**描述**

让特定人物喝水。

**参数**

- `hero`: int类型，表示人物ID。

**返回值**

- NULL

------

## DrinkOil

**函数原型**

```csharp
void DrinkOil(int hero, int value);
```

**描述**

让机器人“喝”汽油。

**参数**

- `hero`: int类型，表示机器人ID。
- `value`: int类型，表示汽油量。

**返回值**

- NULL

---

## PeopleEat

**函数原型**

```csharp
void PeopleEat(int hero);
```

**描述**

让特定人物吃食物。

**参数**

- `hero`: int类型，表示人物ID。

**返回值**

- NULL

------

## PeopleEat (重载)

**函数原型**

```csharp
void PeopleEat(int hero, Items item);
```

**描述**

让特定人物吃特定的食物。

**参数**

- `hero`: int类型，表示人物ID。
- `item`: Items类型，表示食物。

**返回值**

- NULL

------

## PeopleCoffee

**函数原型**

```csharp
void PeopleCoffee(int hero);
```

**描述**

让特定人物喝咖啡。

**参数**

- `hero`: int类型，表示人物ID。

**返回值**

- NULL

------

## SetDriver

**函数原型**

```csharp
void SetDriver(int hero);
```

**描述**

设置特定人物为驾驶员。

**参数**

- `hero`: int类型，表示人物ID。

**返回值**

- NULL

------

## Sleep

**函数原型**

```csharp
void Sleep(int time);
```

**描述**

让程序等待特定时间。

**参数**

- `time`: int类型，表示等待时间。

**返回值**

- NULL

------

## AutoWait

**函数原型**

```csharp
void AutoWait();
```

**描述**

自动等待，直到特定条件满足。

**参数**

- NULL

**返回值**

- NULL

------

## RecoverMood

**函数原型**

```csharp
void RecoverMood(int value, int peopleID, int type);
```

**描述**

恢复特定人物的心情。

**参数**

- `value`: int类型，表示恢复的心情值。
- `peopleID`: int类型，表示人物ID。
- `type`: int类型，表示心情类型。

**返回值**

- NULL

------

## FoodLastDays

**函数原型**

```csharp
int FoodLastDays();
```

**描述**

计算食物的剩余天数。

**参数**

- NULL

**返回值**

- `int`: 食物的剩余天数。

------

## WaterLastDays

**函数原型**

```csharp
int WaterLastDays();
```

**描述**

计算水的剩余天数。

**参数**

- NULL

**返回值**

- `int`: 水的剩余天数。