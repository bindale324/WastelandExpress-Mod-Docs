## AddTask

**函数原型**

```csharp
void AddTask(int tid, int mapId);
```

**描述**

在指定地图上添加任务。

**参数**

- `tid`: int类型，表示任务ID。
- `mapId`: int类型，表示地图ID。

**返回值**

- NULL

------

## DelTaskInAllMap

**函数原型**

```csharp
void DelTaskInAllMap(int tid, bool showDialog = true);
```

**描述**

在所有地图上删除指定任务。

**参数**

- `tid`: int类型，表示任务ID。
- `showDialog`: bool类型，表示是否显示对话框，默认为true。

**返回值**

- NULL

------

## GetTaskList

**函数原型**

```csharp
List<int> GetTaskList(int MapID);
```

**描述**

获取特定地图上的任务列表。

**参数**

- `MapID`: int类型，表示地图ID。

**返回值**

- `List<int>`: 特定地图上的任务ID列表。

------

## GetTasksInAllMapDic

**函数原型**

```csharp
Dictionary<int, List<int>> GetTasksInAllMapDic();
```

**描述**

获取所有地图上的任务字典。

**参数**

- NULL

**返回值**

- `Dictionary<int, List<int>>`: 包含所有地图任务ID列表的字典。

------

## TryGetMapIdByTaskId

**函数原型**

```csharp
bool TryGetMapIdByTaskId(int taskId, out List<int> mapIds);
```

**描述**

尝试通过任务ID获取地图ID。

**参数**

- `taskId`: int类型，表示任务ID。
- `mapIds`: out List<int>类型，输出对应的地图ID列表。

**返回值**

- `bool`: 操作是否成功。

------

## ExistTaskInAllMap

**函数原型**

```csharp
bool ExistTaskInAllMap(int tid);
```

**描述**

检查所有地图上是否存在指定任务。

**参数**

- `tid`: int类型，表示任务ID。

**返回值**

- `bool`: 是否存在该任务。

------

## SetTaskTargetCity

**函数原型**

```csharp
void SetTaskTargetCity(int tid, int mapId, int cityId);
```

**描述**

设置任务的目标城市。

**参数**

- `tid`: int类型，表示任务ID。
- `mapId`: int类型，表示地图ID。
- `cityId`: int类型，表示城市ID。

**返回值**

- NULL

------

## SetTaskTargetTrigger

**函数原型**

```csharp
void SetTaskTargetTrigger(int tid, int mapId, int triggerID);
```

**描述**

设置任务的目标触发器。

**参数**

- `tid`: int类型，表示任务ID。
- `mapId`: int类型，表示地图ID。
- `triggerID`: int类型，表示触发器ID。

**返回值**

- NULL

------

## TryGetTaskTrigger

**函数原型**

```csharp
bool TryGetTaskTrigger(int tid, int mapId, out int triggerId);
```

**描述**

尝试获取任务的触发器ID。

**参数**

- `tid`: int类型，表示任务ID。
- `mapId`: int类型，表示地图ID。
- `triggerId`: out int类型，输出触发器ID。

**返回值**

- `bool`: 操作是否成功。

------

## TryGetTaskCity

**函数原型**

```csharp
bool TryGetTaskCity(int taskId, int mapId, out int cityId);
```

**描述**

尝试获取任务的目标城市ID。

**参数**

- `taskId`: int类型，表示任务ID。
- `mapId`: int类型，表示地图ID。
- `cityId`: out int类型，输出城市ID。

**返回值**

- `bool`: 操作是否成功。