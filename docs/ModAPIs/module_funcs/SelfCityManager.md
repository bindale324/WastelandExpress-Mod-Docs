## GetAllSelfcity

**函数原型**

```csharp
CurrentSelfCityData GetAllSelfcity();
```

**描述**

获取所有自建城市的当前数据。

**参数**

- NULL

**返回值**

- `CurrentSelfCityData`: 所有自建城市的当前数据。

------

## UpdateCityData

**函数原型**

```csharp
void UpdateCityData(CityData t, int mapID);
```

**描述**

更新特定地图上城市的数据。

**参数**

- `t`: CityData类型，表示城市数据。
- `mapID`: int类型，表示地图ID。

**返回值**

- NULL

------

## GetCityData

**函数原型**

```csharp
SelfCity GetCityData(int cityID, int MapID);
```

**描述**

获取特定地图上特定ID的城市数据。

**参数**

- `cityID`: int类型，表示城市ID。
- `MapID`: int类型，表示地图ID。

**返回值**

- `SelfCity`: 特定城市的数据。

------

## GetCityBySelf

**函数原型**

```csharp
CityData GetCityBySelf(SelfCity selfCity);
```

**描述**

根据自建城市获取城市数据。

**参数**

- `selfCity`: SelfCity类型，表示自建城市。

**返回值**

- `CityData`: 对应的城市数据。

------

## GetCityBySelf (重载)

**函数原型**

```csharp
CityData GetCityBySelf(SelfCity selfCity, out string cityID);
```

**描述**

根据自建城市获取城市数据，同时获取城市ID。

**参数**

- `selfCity`: SelfCity类型，表示自建城市。
- `cityID`: out string类型，输出城市ID。

**返回值**

- `CityData`: 对应的城市数据。

------

## GetAttackRate

**函数原型**

```csharp
float GetAttackRate(SelfCity SC);
```

**描述**

获取自建城市的攻击率。

**参数**

- `SC`: SelfCity类型，表示自建城市。

**返回值**

- `float`: 自建城市的攻击率。

------

## ChangeCityResource

**函数原型**

```csharp
void ChangeCityResource(CityData cityData, int Cost, int Type);
```

**描述**

更改城市的资源。

**参数**

- `cityData`: CityData类型，表示城市数据。
- `Cost`: int类型，表示成本。
- `Type`: int类型，表示资源类型。

**返回值**

- NULL

------

## UpgradeBuilding

**函数原型**

```csharp
void UpgradeBuilding(int cityID, int mapID, string BuildingName);
```

**描述**

升级特定城市中的建筑。

**参数**

- `cityID`: int类型，表示城市ID。
- `mapID`: int类型，表示地图ID。
- `BuildingName`: string类型，表示建筑名称。

**返回值**

- NULL

------

## GetBuildingLevel

**函数原型**

```csharp
int GetBuildingLevel(int cityID, string BuildingName);
```

**描述**

获取特定城市中特定建筑的等级。

**参数**

- `cityID`: int类型，表示城市ID。
- `BuildingName`: string类型，表示建筑名称。

**返回值**

- `int`: 建筑的等级。

------

## GetCityProsperity

**函数原型**

```csharp
int GetCityProsperity(int cityID);
```

**描述**

获取特定城市的繁荣度。

**参数**

- `cityID`: int类型，表示城市ID。

**返回值**

- `int`: 城市的繁荣度。

------

## GetCityProsperity (重载)

**函数原型**

```csharp
int GetCityProsperity(int cityID, int mapID);
```

**描述**

获取特定地图上特定城市的繁荣度。

**参数**

- `cityID`: int类型，表示城市ID。
- `mapID`: int类型，表示地图ID。

**返回值**

- `int`: 城市的繁荣度。

------

## GetCityMaxPeople

**函数原型**

```csharp
int GetCityMaxPeople(int cityID, int mapID);
```

**描述**

获取特定地图上特定城市的最大人口数。

**参数**

- `cityID`: int类型，表示城市ID。
- `mapID`: int类型，表示地图ID。

**返回值**

- `int`: 城市的最大人口数。

------

## GetCityPeopleCurrentCount

**函数原型**

```csharp
int GetCityPeopleCurrentCount(int cityID, int mapID);
```

**描述**

获取特定地图上特定城市的当前人口数。

**参数**

- `cityID`: int类型，表示城市ID。
- `mapID`: int类型，表示地图ID。

**返回值**

- `int`: 城市的当前人口数。

---

## CargoSituation

**函数原型**

```csharp
string CargoSituation(int cityID);
```

**描述**

获取特定城市的货物情况。

**参数**

- `cityID`: int类型，表示城市ID。

**返回值**

- `string`: 城市的货物情况描述。

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

## GetItemsInSelfCity

**函数原型**

```csharp
Items GetItemsInSelfCity(int cityID, int ID);
```

**描述**

获取自建城市中特定ID的物品。

**参数**

- `cityID`: int类型，表示城市ID。
- `ID`: int类型，表示物品ID。

**返回值**

- `Items`: 指定ID的物品。

------

## TryGetItemCount

**函数原型**

```csharp
int TryGetItemCount(int cityID, int ID);
```

**描述**

尝试获取特定城市中特定ID物品的数量。

**参数**

- `cityID`: int类型，表示城市ID。
- `ID`: int类型，表示物品ID。

**返回值**

- `int`: 物品数量。

------

## TryGetItemCount (重载)

**函数原型**

```csharp
int TryGetItemCount(int cityID, int mapID, int ID);
```

**描述**

尝试获取特定地图上特定城市中特定ID物品的数量。

**参数**

- `cityID`: int类型，表示城市ID。
- `mapID`: int类型，表示地图ID。
- `ID`: int类型，表示物品ID。

**返回值**

- `int`: 物品数量。

------

## NextOutputTime

**函数原型**

```csharp
string NextOutputTime();
```

**描述**

获取下一次产出的时间。

**参数**

- NULL

**返回值**

- `string`: 下一次产出的时间。

------

## ChangePeople

**函数原型**

```csharp
void ChangePeople(int cityID, CityJob job, Personal p);
```

**描述**

更换特定城市中的职位人员。

**参数**

- `cityID`: int类型，表示城市ID。
- `job`: CityJob类型，表示职位。
- `p`: Personal类型，表示人员。

**返回值**

- NULL

------

## FirePeople

**函数原型**

```csharp
void FirePeople(int cityID, int mapId, CityJob job, bool toCar = true);
```

**描述**

解雇特定城市中的职位人员。

**参数**

- `cityID`: int类型，表示城市ID。
- `mapId`: int类型，表示地图ID。
- `job`: CityJob类型，表示职位。
- `toCar`: bool类型，表示是否转移到车辆，默认为true。

**返回值**

- NULL

------

## GenerateTradeCities

**函数原型**

```csharp
void GenerateTradeCities(CityData cityData, SelfCity selfCity, int mapID);
```

**描述**

为特定城市生成贸易城市。

**参数**

- `cityData`: CityData类型，表示城市数据。
- `selfCity`: SelfCity类型，表示自建城市。
- `mapID`: int类型，表示地图ID。

**返回值**

- NULL

---

## SignCity

**函数原型**

```csharp
bool SignCity(CityData SelfCityData, CityData TradeCityData, int MapID, bool IsCheck, bool Hint = true);
```

**描述**

签署与特定贸易城市的协议。

**参数**

- `SelfCityData`: CityData类型，表示自建城市数据。
- `TradeCityData`: CityData类型，表示贸易城市数据。
- `MapID`: int类型，表示地图ID。
- `IsCheck`: bool类型，表示是否进行检查。
- `Hint`: bool类型，表示是否显示提示，默认为true。

**返回值**

- `bool`: 操作是否成功。

------

## GetTradePrice

**函数原型**

```csharp
int GetTradePrice(string ID, float Distance);
```

**描述**

获取特定物品在给定距离下的贸易价格。

**参数**

- `ID`: string类型，表示物品ID。
- `Distance`: float类型，表示贸易距离。

**返回值**

- `int`: 贸易价格。

------

## ChangeJobCraft

**函数原型**

```csharp
void ChangeJobCraft(CityJob job, int id, Action callback);
```

**描述**

更改城市中特定工作的职业技能。

**参数**

- `job`: CityJob类型，表示职位。
- `id`: int类型，表示技能ID。
- `callback`: Action类型，表示回调函数。

**返回值**

- NULL

------

## ChangeJob

**函数原型**

```csharp
void ChangeJob(CityJob job, string data, Action callback);
```

**描述**

更改城市中的职位数据。

**参数**

- `job`: CityJob类型，表示职位。
- `data`: string类型，表示职位数据。
- `callback`: Action类型，表示回调函数。

**返回值**

- NULL
