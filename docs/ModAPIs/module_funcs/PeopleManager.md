## GetPeople

__函数原型__

```csharp
PeopleData Getpeople();
```

__描述__

获取人物的数据。

__参数__

+ NULL

__返回值__

+ `PeopleData`: 人物数据

---


## GetPeopleByID

__函数原型__

```csharp
Personal GetPeopleByID(int id);
```

__描述__

根据人物ID获取人物的详细信息类。

__参数__

+ `id`: int类型，表示人物的ID。（对于Lua脚本来说，只需要传入`number`类型的数据即可）

__返回值__

+ `Personal`: 人物详细信息类

---

## Addpeople

**函数原型**

```csharp
void Addpeople(int id);
```

**描述**

向游戏中添加一个人物。

**参数**

- `id`: int类型，表示要添加的人物的ID。

**返回值**

- NULL

------

## MovePeople

**函数原型**

```csharp
void MovePeople(int id, bool next);
```

**描述**

移动指定ID的人物。

**参数**

- `id`: int类型，表示人物的ID。
- `next`: bool类型，表示移动的方向或方式。

**返回值**

- NULL

------

## Deletepeople

**函数原型**

```csharp
void Deletepeople(int index, int method = 0);
```

**描述**

删除指定索引位置的人物。

**参数**

- `index`: int类型，表示要删除的人物的索引。
- `method`: int类型，表示删除的方式，默认为0。

**返回值**

- NULL

------

## TryDeletePeople

**函数原型**

```csharp
bool TryDeletePeople(int peopleId, int method = 0);
```

**描述**

尝试删除指定ID的人物。

**参数**

- `peopleId`: int类型，表示人物的ID。
- `method`: int类型，表示删除的方式，默认为0。

**返回值**

- `bool`: 删除操作是否成功。

------

## ChageStatus

**函数原型**

```csharp
void ChageStatus(bool IsSingle, int Type, int Value);
```

**描述**

改变人物的状态。

**参数**

- `IsSingle`: bool类型，表示是否单独改变状态。
- `Type`: int类型，表示状态类型。
- `Value`: int类型，表示状态值。

**返回值**

- NULL

------

## PeopleTalk

**函数原型**

```csharp
void PeopleTalk(int i, bool InCamp = false);
```

**描述**

使人物进行对话。

**参数**

- `i`: int类型，表示人物索引。
- `InCamp`: bool类型，表示人物是否在阵营中，默认为false。

**返回值**

- NULL

------

## TryLikeCurCity

**函数原型**

```csharp
bool TryLikeCurCity(int Poss, bool Like, string Reason, int hero = -1);
```

**描述**

尝试让人物对当前城市产生好感或不好感。

**参数**

- `Poss`: int类型，表示可能性。
- `Like`: bool类型，表示好感或不好感。
- `Reason`: string类型，表示原因。
- `hero`: int类型，表示英雄的ID，默认为-1。

**返回值**

- `bool`: 操作是否成功。

------

## TryLikeCity

**函数原型**

```csharp
bool TryLikeCity(int Poss, bool Like, string Reason, CityData cityData, int map = -1, int hero = -1);
```

**描述**

尝试让人物对指定城市产生好感或不好感。

**参数**

- `Poss`: int类型，表示可能性。
- `Like`: bool类型，表示好感或不好感。
- `Reason`: string类型，表示原因。
- `cityData`: CityData类型，表示城市数据。
- `map`: int类型，表示地图ID，默认为-1。
- `hero`: int类型，表示英雄的ID，默认为-1。

**返回值**

- `bool`: 操作是否成功。

---

## TryLikeEvent

**函数原型**

```csharp
void TryLikeEvent(int TemplateID, bool Like, int Poss = 100);
```

**描述**

尝试让人物对某个事件产生好感或不好感。

**参数**

- `TemplateID`: int类型，表示事件模板ID。
- `Like`: bool类型，表示好感或不好感。
- `Poss`: int类型，表示可能性，默认为100。

**返回值**

- NULL

------

## TryLikeEvent (重载)

**函数原型**

```csharp
void TryLikeEvent(int TemplateID, int PeopleID, bool Like, int Poss = 100);
```

**描述**

尝试让特定人物对某个事件产生好感或不好感。

**参数**

- `TemplateID`: int类型，表示事件模板ID。
- `PeopleID`: int类型，表示人物ID。
- `Like`: bool类型，表示好感或不好感。
- `Poss`: int类型，表示可能性，默认为100。

**返回值**

- NULL

------

## ChangePeopleToPeopleAttitute

**函数原型**

```csharp
void ChangePeopleToPeopleAttitute(Personal peopleFrom, Personal peopleTo, int Attitude);
```

**描述**

改变两个人物之间的态度。

**参数**

- `peopleFrom`: Personal类型，表示来源人物。
- `peopleTo`: Personal类型，表示目标人物。
- `Attitude`: int类型，表示要改变的态度值。

**返回值**

- NULL

------

## PeopleFirstAttitude

**函数原型**

```csharp
void PeopleFirstAttitude(Personal peopleFrom, Personal peopleTo, bool Hint = false);
```

**描述**

设置两个人物之间的初次态度。

**参数**

- `peopleFrom`: Personal类型，表示来源人物。
- `peopleTo`: Personal类型，表示目标人物。
- `Hint`: bool类型，表示是否提示，默认为false。

**返回值**

- NULL

------

## CalmPeople

**函数原型**

```csharp
void CalmPeople(Personal pFrom, Personal pTo);
```

**描述**

使两个人物平静下来。

**参数**

- `pFrom`: Personal类型，表示来源人物。
- `pTo`: Personal类型，表示目标人物。

**返回值**

- NULL

------

## TryMakeLove

**函数原型**

```csharp
bool TryMakeLove();
```

**描述**

尝试让人物陷入恋爱。

**参数**

- NULL

**返回值**

- `bool`: 操作是否成功。

------

## TryGetOldFriend

**函数原型**

```csharp
bool TryGetOldFriend(int peopleID, out List<int> friendsID, out string friendsNameList);
```

**描述**

尝试获取人物的老朋友。

**参数**

- `peopleID`: int类型，表示人物ID。
- `friendsID`: List<int>类型，输出朋友的ID列表。
- `friendsNameList`: string类型，输出朋友的名字列表。

**返回值**

- `bool`: 操作是否成功。

------

## CheckGenderEffettive

**函数原型**

```csharp
bool CheckGenderEffettive(Personal peopleFrom, Personal peopleTo);
```

**描述**

检查两个人物之间的性别效应。

**参数**

- `peopleFrom`: Personal类型，表示来源人物。
- `peopleTo`: Personal类型，表示目标人物。

**返回值**

- `bool`: 检查是否成功。