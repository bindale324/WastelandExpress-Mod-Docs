## GetCityId

**函数原型**

```csharp
int GetCityId();
```

**描述**

获取当前城市的ID。

**参数**

- NULL

**返回值**

- `int`: 当前城市的ID。

------

## ShowEnterCity

**函数原型**

```csharp
void ShowEnterCity(int cityId, bool ignoreMoral);
```

**描述**

显示进入特定城市的界面，可选择是否忽略道德考虑。

**参数**

- `cityId`: int类型，表示城市ID。
- `ignoreMoral`: bool类型，表示是否忽略道德考虑。

**返回值**

- NULL

------

## ShowExitCity

**函数原型**

```csharp
void ShowExitCity();
```

**描述**

显示离开城市的界面。

**参数**

- NULL

**返回值**

- NULL

------

## ExitCityDirectly

**函数原型**

```csharp
void ExitCityDirectly();
```

**描述**

直接离开城市。

**参数**

- NULL

**返回值**

- NULL

------

## ExchangeItems

**函数原型**

```csharp
void ExchangeItems(int cityid, int ItemID, int Count, out bool IsFull, string type = "Objects", object args = null);
```

**描述**

在城市中交换物品。

**参数**

- `cityid`: int类型，表示城市ID。
- `ItemID`: int类型，表示物品ID。
- `Count`: int类型，表示数量。
- `IsFull`: out bool类型，输出是否已满。
- `type`: string类型，表示物品类型，默认为"Objects"。
- `args`: object类型，表示额外参数，可选。

**返回值**

- NULL

------

## GetWeightLimit

**函数原型**

```csharp
int GetWeightLimit(int cityID, int mapID = -1);
```

**描述**

获取特定城市的重量限制。

**参数**

- `cityID`: int类型，表示城市ID。
- `mapID`: int类型，表示地图ID，默认为-1。

**返回值**

- `int`: 城市的重量限制。

------

## CountTotalWeight

**函数原型**

```csharp
int CountTotalWeight(int cityID, int mapID = -1);
```

**描述**

计算特定城市的总重量。

**参数**

- `cityID`: int类型，表示城市ID。
- `mapID`: int类型，表示地图ID，默认为-1。

**返回值**

- `int`: 城市的总重量。

------

## UpdateCityStore

**函数原型**

```csharp
void UpdateCityStore(int cityID);
```

**描述**

更新特定城市的商店存货。

**参数**

- `cityID`: int类型，表示城市ID。

**返回值**

- NULL

------

## SetCityModule

**函数原型**

```csharp
void SetCityModule(int cityId, CityModule cityModule);
```

**描述**

设置特定城市的模块。

**参数**

- `cityId`: int类型，表示城市ID。
- `cityModule`: CityModule类型，表示城市模块。

**返回值**

- NULL

---

## FindCity

**函数原型**

```csharp
bool FindCity(int cityId, out CityData city);
```

**描述**

根据城市ID查找城市并获取城市数据。

**参数**

- `cityId`: int类型，表示城市ID。
- `city`: out CityData类型，输出城市数据。

**返回值**

- `bool`: 操作是否成功。

------

## FindCity (重载)

**函数原型**

```csharp
bool FindCity(int cityId, int mapId, out CityData city);
```

**描述**

在特定地图上根据城市ID查找城市并获取城市数据。

**参数**

- `cityId`: int类型，表示城市ID。
- `mapId`: int类型，表示地图ID。
- `city`: out CityData类型，输出城市数据。

**返回值**

- `bool`: 操作是否成功。

------

## TryGetCurrent

**函数原型**

```csharp
bool TryGetCurrent(out CityData city);
```

**描述**

尝试获取当前城市的数据。

**参数**

- `city`: out CityData类型，输出当前城市数据。

**返回值**

- `bool`: 操作是否成功。

------

## TryGetCityModule

**函数原型**

```csharp
bool TryGetCityModule<T>(int cityId, out T cityModule) where T : CityModule;
```

**描述**

尝试获取特定城市的特定类型的模块。

**参数**

- `cityId`: int类型，表示城市ID。
- `cityModule`: out T类型，输出城市模块，T为CityModule派生类。

**返回值**

- `bool`: 操作是否成功。

------

## TryGetCityModule (重载)

**函数原型**

```csharp
bool TryGetCityModule<T>(int cityId, int MapID, out T cityModule) where T : CityModule;
```

**描述**

在特定地图上尝试获取特定城市的特定类型的模块。

**参数**

- `cityId`: int类型，表示城市ID。
- `MapID`: int类型，表示地图ID。
- `cityModule`: out T类型，输出城市模块，T为CityModule派生类。

**返回值**

- `bool`: 操作是否成功。

------

## CityContainsBaseCommand

**函数原型**

```csharp
bool CityContainsBaseCommand(int cityId, string commandName);
```

**描述**

检查特定城市是否包含特定的基础命令。

**参数**

- `cityId`: int类型，表示城市ID。
- `commandName`: string类型，表示命令名称。

**返回值**

- `bool`: 是否包含该命令。

------

## GetRandomCityByDisance

**函数原型**

```csharp
bool GetRandomCityByDisance(Predicate<CityData> func, float dis, out int cityId);
```

**描述**

根据给定的距离和条件随机获取城市ID。

**参数**

- `func`: Predicate<CityData>类型，表示筛选条件。
- `dis`: float类型，表示距离。
- `cityId`: out int类型，输出城市ID。

**返回值**

- `bool`: 操作是否成功。

------

## GetCityDistance

**函数原型**

```csharp
bool GetCityDistance(int cityId, out float dis);
```

**描述**

获取到特定城市的距离。

**参数**

- `cityId`: int类型，表示城市ID。
- `dis`: out float类型，输出距离。

**返回值**

- `bool`: 操作是否成功。

------

## GetCityByDistanceSort

**函数原型**

```csharp
bool GetCityByDistanceSort(int closeIndex, int farIndex, out int cityId);
```

**描述**

根据距离排序获取城市ID。

**参数**

- `closeIndex`: int类型，表示最近距离索引。
- `farIndex`: int类型，表示最远距离索引。
- `cityId`: out int类型，输出城市ID。

**返回值**

- `bool`: 操作是否成功。