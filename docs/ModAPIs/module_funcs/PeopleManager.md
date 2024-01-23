## Getpeople

__函数原型__

```csharp
PeopleData Getpeople();
```

__描述__

当前所有人物。

__参数__

+ NULL

__返回值__

+ `PeopleData`: 人物数据，
  + 这个里面有各种属性，其中有一个叫做`NowPeople`的属性，`NowPeople`的数据类型是`List<Personal>`，表示车上的人。



> 如果你想获取当前车上所有人的信息，您可以像这样：
>
> ```lua
> local people_on_truck = PeopleManager:Getpeople().NowPeople
> 
> -- 尝试打印车上第1个人的信息
> print(type(people_on_truck))
> print(people_on_truck[0].PeopleID)
> ```
>
> 这样您就会看到车上第一个人的人物ID。



有关这些数据的内部成员变量、方法，您可以查看[附录](ModAPIs/module_funcs/Appendix.md) 。

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

------

## MovePeople

**函数原型**

```csharp
void MovePeople(int id, bool next);
```

**描述**

在车上移动指定ID的人物的位置。

**参数**

- `id`: int类型，表示人物的ID。
- `next`: bool类型，表示移动的方向。

**返回值**

- NULL

------

## Deletepeople

**函数原型**

```csharp
void Deletepeople(int index, int method = 0);
```

**描述**

把车上的某个人踢下车。

**参数**

- `index`: int类型，表示要踢下车的人物在车上的位置。
- `method`: int类型，表示删除的方式，默认为0。（我们也不建议更改这个值）

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

该函数会遍历车上的所有人，挨个改变状态。如果遇到单身狗就break循环。且整体逻辑具有随机性。（概率为50%）

**参数**

- `IsSingle`: bool类型，表示是否是单身
- `Type`: int类型，表示要改变什么属性的值
  + `Type=0`: 增加战斗力数值
  + `Type=1`: 增加身体素质
  + `Type=2`: 增加注意力
  + `Type=3`: 增加口才
  + `Type=4`: 增加制作
  + `Type=5`: 增加智力
  + `Type=6`: 增加道德
  + `Type=7`: 增加耕作
  + `Type=8`: 增加魅力
  + 注意：**如果传入其他int值，会报错。**
- `Value`: int类型，表示要增加的属性值

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
  + 注意在这里是一个int数值，而不是浮点数，比如说可能性是98%的话，直接传入98即可。
- `Like`: bool类型，表示好感或不好感。
- `Reason`: string类型，表示原因。
- `hero`: int类型，表示英雄的ID，默认为-1。

**返回值**

- `bool`: 操作是否成功。

------

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
  + 注意在这里是一个int数值，而不是浮点数，比如说可能性是98%的话，直接传入98即可。

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
  + 注意在这里是一个int数值，而不是浮点数，比如说可能性是98%的话，直接传入98即可。

**返回值**

- NULL

------

## ChangePeopleToPeopleAttitute

**函数原型**

```csharp
void ChangePeopleToPeopleAttitute(Personal peopleFrom, Personal peopleTo, int Attitude);
```

**描述**

改变一个人对另一个人的好感度，如果`Altitude`是正值就是增加好感度，如果是`负值`就降低好感度。

> 注：在Altitude < 2的时候，可能会破坏两人的关系

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
- `Hint`: bool类型，表示是否提示，默认为false。（不建议修改该值）

**返回值**

- NULL

---

## PeopleTalk

**函数原型**

```csharp
void PeopleTalk(int index, bool InCamp = false);
```

**描述**

让车上的人聊天。

**参数**

- `i`: int类型，表示车上的哪个人开始说话。
- `InCamp`: bool类型，表示是否在营地中。

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

尝试开始进行鱼水之欢。这个函数会先开始查询队伍中每个人的状态，如果状态合适会执行鱼水之欢代码逻辑，也就是降低压力值。

**参数**

- NULL

**返回值**

- `bool`: 是否操作成功。

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

- `bool`: 两人是否产生可能 （？）

---

## CheckLoveInDifferentPlace

**函数原型**

```csharp
void CheckLoveInDifferentPlace();
```

**描述**

检查车上每个人对该地点的感觉。也就是到了某个地方之后，每个人的感觉变化

**参数**

- NULL

**返回值**

+ NULL