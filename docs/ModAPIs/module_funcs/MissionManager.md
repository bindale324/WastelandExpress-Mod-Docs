## FinishCity

**属性**

```
List<int> FinishCity { get; }
```

**描述**

获取已完成的城市列表。

**用法**

- 通过该属性可以访问已完成的城市ID列表。

------

## GetTableName

**函数原型**

```csharp
string GetTableName(int ID);
```

**描述**

根据ID获取对应的表名。

**参数**

- `ID`: int类型，表示ID。

**返回值**

- `string`: 对应的表名。

------

## AbortMission

**函数原型**

```csharp
void AbortMission(int id);
```

**描述**

中止特定ID的任务。

**参数**

- `id`: int类型，表示任务ID。

**返回值**

- NULL

------

## AddMission

**函数原型**

```csharp
void AddMission(Mission m);
```

**描述**

添加新的任务。

**参数**

- `m`: Mission类型，表示新的任务。

**返回值**

- NULL

------

## FinishTime

**函数原型**

```csharp
void FinishTime();
```

**描述**

完成当前任务的时间。

**参数**

- NULL

**返回值**

- NULL

------

## GetMissionList

**函数原型**

```csharp
List<Mission> GetMissionList();
```

**描述**

获取当前的任务列表。

**参数**

- NULL

**返回值**

- `List<Mission>`: 当前的任务列表。

------

## GetMission

**函数原型**

```csharp
Mission GetMission(int id, string fractionID);
```

**描述**

根据ID和派系ID获取特定任务。

**参数**

- `id`: int类型，表示任务ID。
- `fractionID`: string类型，表示派系ID。

**返回值**

- `Mission`: 获取的任务。

---

## InitMission

**函数原型**

```csharp
void InitMission();
```

**描述**

初始化任务系统。

**参数**

- NULL

**返回值**

- NULL

------

## MissionEnd

**函数原型**

```csharp
void MissionEnd(int cityid);
```

**描述**

标记特定城市的任务为结束状态。

**参数**

- `cityid`: int类型，表示城市ID。

**返回值**

- NULL

------

## PickMissionId

**函数原型**

```csharp
int PickMissionId();
```

**描述**

选择并返回一个任务ID。

**参数**

- NULL

**返回值**

- `int`: 选中的任务ID。

------

## ClosetMissionID

**函数原型**

```csharp
int ClosetMissionID();
```

**描述**

获取最近的任务ID。

**参数**

- NULL

**返回值**

- `int`: 最近的任务ID。

------

## CheckMissionIDLegal

**函数原型**

```csharp
bool CheckMissionIDLegal(int missionID);
```

**描述**

检查特定任务ID是否合法。

**参数**

- `missionID`: int类型，表示任务ID。

**返回值**

- `bool`: 任务ID是否合法。

------

## ExistAvailableMission

**函数原型**

```csharp
bool ExistAvailableMission();
```

**描述**

检查是否存在可用的任务。

**参数**

- NULL

**返回值**

- `bool`: 是否存在可用的任务。