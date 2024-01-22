## AllMapDatas

**函数原型**

```csharp
Dictionary<int, MapData> AllMapDatas();
```

**描述**

获取所有地图数据。

**参数**

- NULL

**返回值**

- `Dictionary<int, MapData>`: 包含所有地图数据的字典，其中键为地图ID。

------

## GetCurrentMap

**函数原型**

```csharp
MapData GetCurrentMap();
```

**描述**

获取当前地图的数据。

**参数**

- NULL

**返回值**

- `MapData`: 当前地图的数据。

------

## Context

**属性**

```
MapSystem.MapCentext Context { get; }
```

**描述**

获取地图系统的上下文。

**用法**

- 通过该属性可以访问地图系统的上下文信息。

------

## MainRunner

**属性**

```
MapRunner MainRunner { get; }
```

**描述**

获取地图系统的主运行器。

**用法**

- 通过该属性可以访问地图系统的主运行器。

------

## InitTrigger

**函数原型**

```csharp
void InitTrigger(MapTrigger mapTrigger);
```

**描述**

初始化地图触发器。

**参数**

- `mapTrigger`: MapTrigger类型，表示地图触发器。

**返回值**

- NULL

------

## GetPathPointList

**函数原型**

```csharp
List<Vector2> GetPathPointList();
```

**描述**

获取路径点列表。

**参数**

- NULL

**返回值**

- `List<Vector2>`: 路径点的列表。

------

## RegisterHighLight

**函数原型**

```csharp
void RegisterHighLight(Predicate<MapTrigger> checkId);
```

**描述**

注册高亮显示特定触发器。

**参数**

- `checkId`: Predicate<MapTrigger>类型，表示检查触发器的条件。

**返回值**

- NULL

------

## GetHighLightList

**函数原型**

```csharp
List<int> GetHighLightList(List<int> outputList = null);
```

**描述**

获取高亮触发器的ID列表。

**参数**

- `outputList`: List<int>类型，表示输出列表，可选。

**返回值**

- `List<int>`: 高亮触发器的ID列表。

------

## AddPathPoint

**函数原型**

```csharp
void AddPathPoint(Vector2 pos, int index = -1);
```

**描述**

添加路径点。

**参数**

- `pos`: Vector2类型，表示路径点的位置。
- `index`: int类型，表示路径点的索引，默认为-1。

**返回值**

- NULL

------

## SetMaxIndex

**函数原型**

```csharp
void SetMaxIndex(MapRunner mapRunner, int index);
```

**描述**

设置地图运行器的最大索引。

**参数**

- `mapRunner`: MapRunner类型，表示地图运行器。
- `index`: int类型，表示最大索引。

**返回值**

- NULL

------

## FindRunner

**函数原型**

```csharp
MapRunner FindRunner(int id);
```

**描述**

根据ID查找地图运行器。

**参数**

- `id`: int类型，表示运行器ID。

**返回值**

- `MapRunner`: 找到的地图运行器。

---

## RemoveRunner

**函数原型**

```csharp
bool RemoveRunner(int id);
```

**描述**

根据ID移除地图运行器。

**参数**

- `id`: int类型，表示运行器ID。

**返回值**

- `bool`: 操作是否成功。

------

## UpdateMainRunner

**函数原型**

```csharp
void UpdateMainRunner();
```

**描述**

更新主地图运行器的状态。

**参数**

- NULL

**返回值**

- NULL

------

## ResetPath

**函数原型**

```csharp
void ResetPath();
```

**描述**

重置路径。

**参数**

- NULL

**返回值**

- NULL

------

## ContainsPathDrive

**函数原型**

```csharp
bool ContainsPathDrive();
```

**描述**

检查是否包含路径驱动。

**参数**

- NULL

**返回值**

- `bool`: 是否包含路径驱动。

------

## StopDriveAndTime

**函数原型**

```csharp
void StopDriveAndTime();
```

**描述**

停止驱动和计时。

**参数**

- NULL

**返回值**

- NULL

------

## BeginDriveAndTime

**函数原型**

```csharp
void BeginDriveAndTime();
```

**描述**

开始驱动和计时。

**参数**

- NULL

**返回值**

- NULL

------

## SetMainSpeed

**函数原型**

```csharp
void SetMainSpeed(float v);
```

**描述**

设置主运行器的速度。

**参数**

- `v`: float类型，表示速度值。

**返回值**

- NULL

------

## TrgGetPlayerNextDistance

**函数原型**

```csharp
bool TrgGetPlayerNextDistance(out float nextDis);
```

**描述**

获取玩家到下一个触发点的距离。

**参数**

- `nextDis`: out float类型，输出到下一个触发点的距离。

**返回值**

- `bool`: 操作是否成功。

------

## FindTrigger

**函数原型**

```csharp
bool FindTrigger(Predicate<MapTrigger> func, float dis, List<MapTrigger> outputList = null);
```

**描述**

根据条件和距离查找触发器。

**参数**

- `func`: Predicate<MapTrigger>类型，表示查找条件。
- `dis`: float类型，表示距离。
- `outputList`: List<MapTrigger>类型，表示输出列表，可选。

**返回值**

- `bool`: 操作是否成功。

------

## GetDisance

**函数原型**

```csharp
float GetDisance(int triggerId);
```

**描述**

获取到特定触发器的距离。

**参数**

- `triggerId`: int类型，表示触发器ID。

**返回值**

- `float`: 到触发器的距离。

---

## GetDisance（重载）

**函数原型**

```csharp
float GetDisance(int triggerId, int triggerId2);
```

**描述**

获取两个触发器之间的距离。

**参数**

- `triggerId`: int类型，表示第一个触发器ID。
- `triggerId2`: int类型，表示第二个触发器ID。

**返回值**

- `float`: 两个触发器之间的距离。

------

## GetTriggersFromPoint

**函数原型**

```csharp
List<MapTrigger> GetTriggersFromPoint(Vector2 point, List<MapTrigger> output = null);
```

**描述**

从特定点获取触发器列表。

**参数**

- `point`: Vector2类型，表示特定点的位置。
- `output`: List<MapTrigger>类型，表示输出的触发器列表，可选。

**返回值**

- `List<MapTrigger>`: 从特定点获取的触发器列表。

------

## AddEventRegion

**函数原型**

```csharp
void AddEventRegion(int tid, Vector2 position, float size = 30f);
```

**描述**

添加事件区域。

**参数**

- `tid`: int类型，表示事件ID。
- `position`: Vector2类型，表示区域位置。
- `size`: float类型，表示区域大小，默认为30f。

**返回值**

- NULL

------

## AddRunnerEventRegion

**函数原型**

```csharp
void AddRunnerEventRegion(int tid, Vector2 position, float size, float speed, float radius, int runtime, int stoptime);
```

**描述**

为运行器添加事件区域。

**参数**

- `tid`: int类型，表示事件ID。
- `position`: Vector2类型，表示区域位置。
- `size`: float类型，表示区域大小。
- `speed`: float类型，表示速度。
- `radius`: float类型，表示半径。
- `runtime`: int类型，表示运行时间。
- `stoptime`: int类型，表示停止时间。

**返回值**

- NULL

------

## EnableRegion

**函数原型**

```csharp
bool EnableRegion(string regionName, bool enable);
```

**描述**

启用或禁用特定区域。

**参数**

- `regionName`: string类型，表示区域名称。
- `enable`: bool类型，表示是否启用。

**返回值**

- `bool`: 操作是否成功。

------

## RemoveTrigger

**函数原型**

```csharp
bool RemoveTrigger(int triggerId, int mapId = -1);
```

**描述**

移除特定地图上的触发器。

**参数**

- `triggerId`: int类型，表示触发器ID。
- `mapId`: int类型，表示地图ID，默认为-1。

**返回值**

- `bool`: 操作是否成功。

------

## GetTrigger

**函数原型**

```csharp
MapTrigger GetTrigger(int triggerId, int mapID = -1);
```

**描述**

获取特定地图上的触发器。

**参数**

- `triggerId`: int类型，表示触发器ID。
- `mapID`: int类型，表示地图ID，默认为-1。

**返回值**

- `MapTrigger`: 找到的触发器。

------

## CheckOrCreateTaskRegion

**函数原型**

```csharp
bool CheckOrCreateTaskRegion(out int triggerID, int tid, Vector2 startPos, float dis, float size = 20f, string regionName = "");
```

**描述**

检查或创建任务区域。

**参数**

- `triggerID`: out int类型，输出触发器ID。
- `tid`: int类型，表示任务ID。
- `startPos`: Vector2类型，表示开始位置。
- `dis`: float类型，表示距离。
- `size`: float类型，表示区域大小，默认为20f。
- `regionName`: string类型，表示区域名称，默认为空字符串。

**返回值**

- `bool`: 操作是否成功。

------

## CheckOrCreateTaskRegion (重载)

**函数原型**

```csharp
bool CheckOrCreateTaskRegion(out int triggerID, int tid, Vector2 startPos, float dis, float size = 20f, Predicate<MapTrigger> condition = null);
```

**描述**

在满足特定条件的情况下检查或创建任务区域。

**参数**

- `triggerID`: out int类型，输出触发器ID。
- `tid`: int类型，表示任务ID。
- `startPos`: Vector2类型，表示开始位置。
- `dis`: float类型，表示距离。
- `size`: float类型，表示区域大小，默认为20f。
- `condition`: Predicate<MapTrigger>类型，表示区域创建条件，可选。

**返回值**

- `bool`: 操作是否成功。

------

## CheckOrCreateTaskRegionInSpecificPosition

**函数原型**

```csharp
bool CheckOrCreateTaskRegionInSpecificPosition(int mapId, int taskId, float posX, float posY, out int triggerId, float size = 20f);
```

**描述**

在特定位置检查或创建任务区域。

**参数**

- `mapId`: int类型，表示地图ID。
- `taskId`: int类型，表示任务ID。
- `posX`: float类型，表示位置的X坐标。
- `posY`: float类型，表示位置的Y坐标。
- `triggerId`: out int类型，输出触发器ID。
- `size`: float类型，表示区域大小，默认为20f。

**返回值**

- `bool`: 操作是否成功。

---

## GetRandomTargetPosition

**函数原型**

```csharp
Vector2 GetRandomTargetPosition(Vector2 start, float dis, Predicate<MapTrigger> regionName = null);
```

**描述**

获取从起始点指定距离内的随机目标位置。

**参数**

- `start`: Vector2类型，表示起始点位置。
- `dis`: float类型，表示距离。
- `regionName`: Predicate<MapTrigger>类型，表示区域名称的条件判断，可选。

**返回值**

- `Vector2`: 随机目标位置。

------

## GotoCity

**函数原型**

```csharp
Vector2 GotoCity(int cityId);
```

**描述**

导航到指定城市的位置。

**参数**

- `cityId`: int类型，表示城市ID。

**返回值**

- `Vector2`: 指定城市的位置。

------

## GetCityPos

**函数原型**

```csharp
Vector2 GetCityPos(int cityId);
```

**描述**

获取特定城市的位置。

**参数**

- `cityId`: int类型，表示城市ID。

**返回值**

- `Vector2`: 特定城市的位置。

------

## GotoTrigger

**函数原型**

```csharp
Vector2 GotoTrigger(int triggerID);
```

**描述**

导航到指定触发器的位置。

**参数**

- `triggerID`: int类型，表示触发器ID。

**返回值**

- `Vector2`: 指定触发器的位置。

------

## GetCityPos (重载)

**函数原型**

```csharp
Vector2 GetCityPos(int mapId, int cityId);
```

**描述**

获取特定地图上特定城市的位置。

**参数**

- `mapId`: int类型，表示地图ID。
- `cityId`: int类型，表示城市ID。

**返回值**

- `Vector2`: 特定地图上特定城市的位置。

------

## GetTriggerPos

**函数原型**

```csharp
Vector2 GetTriggerPos(int mapId, int triggerId);
```

**描述**

获取特定地图上特定触发器的位置。

**参数**

- `mapId`: int类型，表示地图ID。
- `triggerId`: int类型，表示触发器ID。

**返回值**

- `Vector2`: 特定地图上特定触发器的位置。

------

## ExpandAllInffectedAreas

**函数原型**

```csharp
void ExpandAllInffectedAreas(float Rate);
```

**描述**

扩展所有受影响区域。

**参数**

- `Rate`: float类型，表示扩展比率。

**返回值**

- NULL

------

## GetAllRoads

**函数原型**

```csharp
List<MapTrigger> GetAllRoads(int mapId);
```

**描述**

获取特定地图上所有道路的列表。

**参数**

- `mapId`: int类型，表示地图ID。

**返回值**

- `List<MapTrigger>`: 所有道路的列表。

------

## AddRoad

**函数原型**

```csharp
bool AddRoad(int mapId, int cityId, int order, string name, RoadPoint startPoint, RoadPoint endPoint, out MapTrigger trigger);
```

**描述**

在特定地图上添加道路。

**参数**

- `mapId`: int类型，表示地图ID。
- `cityId`: int类型，表示城市ID。
- `order`: int类型，表示道路顺序。
- `name`: string类型，表示道路名称。
- `startPoint`: RoadPoint类型，表示起点。
- `endPoint`: RoadPoint类型，表示终点。
- `trigger`: out MapTrigger类型，输出道路触发器。

**返回值**

- `bool`: 操作是否成功。

------

## RemoveRoad

**函数原型**

```csharp
void RemoveRoad(int mapId, int triggerId);
```

**描述**

移除特定地图上的道路。

**参数**

- `mapId`: int类型，表示地图ID。
- `triggerId`: int类型，表示触发器ID。

**返回值**

- NULL

---

## CalRoadCost

**函数原型**

```csharp
StockInfo CalRoadCost(int mapId, int triggerId, out List<KeyValuePair<string, bool>> terrians);
```

**描述**

计算特定道路的成本，并获取不同地形的影响。

**参数**

- `mapId`: int类型，表示地图ID。
- `triggerId`: int类型，表示触发器ID。
- `terrians`: out List<KeyValuePair<string, bool>>类型，输出不同地形的影响情况。

**返回值**

- `StockInfo`: 道路的成本信息。

------

## CalRoadPoliticsCost

**函数原型**

```csharp
int CalRoadPoliticsCost(int mapId, int triggerId);
```

**描述**

计算特定道路的政治成本。

**参数**

- `mapId`: int类型，表示地图ID。
- `triggerId`: int类型，表示触发器ID。

**返回值**

- `int`: 道路的政治成本。

------

## CalRoadPoliticsReward

**函数原型**

```csharp
int CalRoadPoliticsReward(int mapId, int triggerId);
```

**描述**

计算特定道路的政治奖励。

**参数**

- `mapId`: int类型，表示地图ID。
- `triggerId`: int类型，表示触发器ID。

**返回值**

- `int`: 道路的政治奖励。

------

## ConfirmRoadBuild

**函数原型**

```csharp
void ConfirmRoadBuild(int mapId, int cityID, int triggerId);
```

**描述**

确认在特定地图上的特定城市建立道路。

**参数**

- `mapId`: int类型，表示地图ID。
- `cityID`: int类型，表示城市ID。
- `triggerId`: int类型，表示触发器ID。

**返回值**

- NULL

------

## BuildRoadPoint

**函数原型**

```csharp
bool BuildRoadPoint(int mapId, int triggerId, int index);
```

**描述**

在特定地图的特定道路上建立道路点。

**参数**

- `mapId`: int类型，表示地图ID。
- `triggerId`: int类型，表示触发器ID。
- `index`: int类型，表示道路点索引。

**返回值**

- `bool`: 操作是否成功。

------

## RefreshRoad

**函数原型**

```csharp
void RefreshRoad(int mapId, int triggerId);
```

**描述**

刷新特定地图上的特定道路。

**参数**

- `mapId`: int类型，表示地图ID。
- `triggerId`: int类型，表示触发器ID。

**返回值**

- NULL

------

## CalLinkScale

**函数原型**

```csharp
int CalLinkScale(int mapId, int triggerId, out HashSet<LinkedCity> linkedCities);
```

**描述**

计算特定道路的连接规模，并获取连接的城市。

**参数**

- `mapId`: int类型，表示地图ID。
- `triggerId`: int类型，表示触发器ID。
- `linkedCities`: out HashSet<LinkedCity>类型，输出连接的城市集合。

**返回值**

- `int`: 道路的连接规模。