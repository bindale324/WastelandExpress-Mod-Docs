## GetDungeonsData

**函数原型**

```csharp
DungeonsData GetDungeonsData();
```

**描述**

获取地牢数据。

**参数**

- NULL

**返回值**

- `DungeonsData`: 地牢数据。

------

## CityCanEnterDungeon

**函数原型**

```csharp
bool CityCanEnterDungeon(int cityId);
```

**描述**

检查城市是否可以进入地牢。

**参数**

- `cityId`: int类型，表示城市ID。

**返回值**

- `bool`: 城市是否可以进入地牢。

------

## CityCanEnterDungeon (重载)

**函数原型**

```csharp
bool CityCanEnterDungeon(int cityId, out int dungeonId);
```

**描述**

检查城市是否可以进入地牢，并获取地牢ID。

**参数**

- `cityId`: int类型，表示城市ID。
- `dungeonId`: out int类型，输出地牢ID。

**返回值**

- `bool`: 城市是否可以进入地牢。

------

## CityCanEnterDungeon (重载)

**函数原型**

```csharp
bool CityCanEnterDungeon(int mapID, int cityId, out int dungeonId);
```

**描述**

检查特定地图上的城市是否可以进入地牢，并获取地牢ID。

**参数**

- `mapID`: int类型，表示地图ID。
- `cityId`: int类型，表示城市ID。
- `dungeonId`: out int类型，输出地牢ID。

**返回值**

- `bool`: 城市是否可以进入地牢。

------

## TryGetDungeon

**函数原型**

```csharp
bool TryGetDungeon(int mapId, int cityId, out Dungeon dungeon);
```

**描述**

尝试获取特定地图和城市的地牢信息。

**参数**

- `mapId`: int类型，表示地图ID。
- `cityId`: int类型，表示城市ID。
- `dungeon`: out Dungeon类型，输出地牢信息。

**返回值**

- `bool`: 是否成功获取地牢信息。

------

## TryGetDungeon (重载)

**函数原型**

```csharp
bool TryGetDungeon(int dungeonId, out Dungeon dungeon);
```

**描述**

尝试获取特定ID的地牢信息。

**参数**

- `dungeonId`: int类型，表示地牢ID。
- `dungeon`: out Dungeon类型，输出地牢信息。

**返回值**

- `bool`: 是否成功获取地牢信息。

------

## GetProperty

**函数原型**

```csharp
List<Items> GetProperty(int _personalId = -1);
```

**描述**

获取特定人物的财产列表。

**参数**

- `_personalId`: int类型，表示人物ID，默认为-1。

**返回值**

- `List<Items>`: 财产列表。

------

## GetPropertyFood

**函数原型**

```csharp
List<Items> GetPropertyFood(int _personalId = -1);
```

**描述**

获取特定人物的食物财产列表。

**参数**

- `_personalId`: int类型，表示人物ID，默认为-1。

**返回值**

- `List<Items>`: 食物财产列表。

------

## GetPropertyIconSprite

**函数原型**

```csharp
Sprite GetPropertyIconSprite(Items property);
```

**描述**

获取财产项的图标精灵。

**参数**

- `property`: Items类型，表示财产项。

**返回值**

- `Sprite`: 财产图标精灵。

---

## GetTotalWeight

**函数原型**

```csharp
int GetTotalWeight(Personal _personal);
```

**描述**

获取特定人物的总重量。

**参数**

- `_personal`: Personal类型，表示人物。

**返回值**

- `int`: 人物的总重量。

------

## CanAfford

**函数原型**

```csharp
bool CanAfford(Personal _personal, int weight);
```

**描述**

检查特定人物是否能负担给定重量。

**参数**

- `_personal`: Personal类型，表示人物。
- `weight`: int类型，表示重量。

**返回值**

- `bool`: 人物是否能负担这个重量。

------

## ExchangePersonalProperty

**函数原型**

```csharp
void ExchangePersonalProperty(Items item, int count, int IdFrom, int IdTo);
```

**描述**

交换两个人物间的财产。

**参数**

- `item`: Items类型，表示交换的物品。
- `count`: int类型，表示交换的数量。
- `IdFrom`: int类型，表示交出物品的人物ID。
- `IdTo`: int类型，表示接收物品的人物ID。

**返回值**

- NULL

------

## CheckOverload

**函数原型**

```csharp
bool CheckOverload(int additionalLoad, int memberId);
```

**描述**

检查特定成员是否超载。

**参数**

- `additionalLoad`: int类型，表示额外的负载。
- `memberId`: int类型，表示成员ID。

**返回值**

- `bool`: 成员是否超载。

------

## ReturnAllProperty

**函数原型**

```csharp
void ReturnAllProperty();
```

**描述**

归还所有财产。

**参数**

- NULL

**返回值**

- NULL

------

## RemoveEquip

**函数原型**

```csharp
void RemoveEquip(int personId, string type);
```

**描述**

移除特定人物的装备。

**参数**

- `personId`: int类型，表示人物ID。
- `type`: string类型，表示装备类型。

**返回值**

- NULL

------

## TryMemberUseItem

**函数原型**

```csharp
bool TryMemberUseItem(int itemId, int personId);
```

**描述**

尝试让成员使用特定物品。

**参数**

- `itemId`: int类型，表示物品ID。
- `personId`: int类型，表示人物ID。

**返回值**

- `bool`: 使用是否成功。

------

## GetCurrentDungeon

**函数原型**

```csharp
CurrentDungeonData GetCurrentDungeon();
```

**描述**

获取当前地牢的数据。

**参数**

- NULL

**返回值**

- `CurrentDungeonData`: 当前地牢的数据。

------

## StartDungeon

**函数原型**

```csharp
void StartDungeon(int dungeonId);
```

**描述**

开始探索指定ID的地牢。

**参数**

- `dungeonId`: int类型，表示地牢ID。

**返回值**

- NULL

---

## DungeonRetreat

**函数原型**

```csharp
void DungeonRetreat(bool force = false);
```

**描述**

撤退出地牢。

**参数**

- `force`: bool类型，表示是否强制撤退，默认为false。

**返回值**

- NULL

------

## CheckInDungeon

**函数原型**

```csharp
bool CheckInDungeon();
```

**描述**

检查是否在地牢中。

**参数**

- NULL

**返回值**

- `bool`: 是否在地牢中。

------

## GetRouteIdsList

**函数原型**

```csharp
List<string> GetRouteIdsList(string startPos, string endPos, bool includingStart = false);
```

**描述**

获取从起始位置到终止位置的路线ID列表。

**参数**

- `startPos`: string类型，表示起始位置。
- `endPos`: string类型，表示终止位置。
- `includingStart`: bool类型，表示是否包括起始位置，默认为false。

**返回值**

- `List<string>`: 路线ID列表。

------

## GetRoute

**函数原型**

```csharp
List<Cell_Info> GetRoute(Dungeon dungeon, List<Node> nodeField, string startCell_Id, string destinationCell_Id, bool includingStart = false);
```

**描述**

获取地牢中从起始单元格到目的地单元格的路线。

**参数**

- `dungeon`: Dungeon类型，表示地牢。
- `nodeField`: List<Node>类型，表示节点场。
- `startCell_Id`: string类型，表示起始单元格ID。
- `destinationCell_Id`: string类型，表示目的地单元格ID。
- `includingStart`: bool类型，表示是否包括起始单元格，默认为false。

**返回值**

- `List<Cell_Info>`: 路线上的单元格信息列表。

------

## GetNearbyReachableCell

**函数原型**

```csharp
List<Cell_Info> GetNearbyReachableCell(string cell_Id);
```

**描述**

获取附近可达的单元格列表。

**参数**

- `cell_Id`: string类型，表示单元格ID。

**返回值**

- `List<Cell_Info>`: 附近可达的单元格列表。

------

## GetCellsInRange

**函数原型**

```csharp
List<string> GetCellsInRange(string originPos, int range);
```

**描述**

获取指定范围内的所有单元格ID。

**参数**

- `originPos`: string类型，表示原点位置。
- `range`: int类型，表示范围。

**返回值**

- `List<string>`: 范围内的单元格ID列表。

------

## CheckCellOccupiedByTeam

**函数原型**

```csharp
bool CheckCellOccupiedByTeam(string positionId);
```

**描述**

检查指定位置的单元格是否被团队占据。

**参数**

- `positionId`: string类型，表示位置ID。

**返回值**

- `bool`: 单元格是否被团队占据。

------

## CheckCellOccupiedByEnemy

**函数原型**

```csharp
bool CheckCellOccupiedByEnemy(string positionId);
```

**描述**

检查指定位置的单元格是否被敌人占据。

**参数**

- `positionId`: string类型，表示位置ID。

**返回值**

- `bool`: 单元格是否被敌人占据。

---

## GetSelectedRoute

**函数原型**

```csharp
List<Cell_Info> GetSelectedRoute();
```

**描述**

获取选定的路线。

**参数**

- NULL

**返回值**

- `List<Cell_Info>`: 选定的路线上的单元格信息列表。

------

## ResetSelectedRoute

**函数原型**

```csharp
void ResetSelectedRoute(List<string> value);
```

**描述**

重置选定的路线。

**参数**

- `value`: List<string>类型，表示新的路线单元格ID列表。

**返回值**

- NULL

------

## GetSelectedRouteEnd

**函数原型**

```csharp
string GetSelectedRouteEnd();
```

**描述**

获取选定路线的终点。

**参数**

- NULL

**返回值**

- `string`: 选定路线的终点单元格ID。

------

## CheckSelectedRouteReachable

**函数原型**

```csharp
bool CheckSelectedRouteReachable();
```

**描述**

检查选定路线是否可达。

**参数**

- NULL

**返回值**

- `bool`: 选定路线是否可达。

------

## CheckSelectedRouteReachable

**函数原型**

```csharp
bool CheckSelectedRouteReachable(out int routeCost);
```

**描述**

检查选定路线是否可达，并获取路线成本。

**参数**

- `routeCost`: out int类型，输出路线成本。

**返回值**

- `bool`: 选定路线是否可达。

------

## GetRouteCost

**函数原型**

```csharp
int GetRouteCost(List<Cell_Info> route);
```

**描述**

获取指定路线的成本。

**参数**

- `route`: List<Cell_Info>类型，表示路线上的单元格信息列表。

**返回值**

- `int`: 路线的成本。

------

## ClearSelectedRoute

**函数原型**

```csharp
void ClearSelectedRoute();
```

**描述**

清除选定的路线。

**参数**

- NULL

**返回值**

- NULL

------

## GetSelectedMemberId

**函数原型**

```csharp
int GetSelectedMemberId();
```

**描述**

获取选定成员的ID。

**参数**

- NULL

**返回值**

- `int`: 选定成员的ID。

------

## SetSelectedMemberId

**函数原型**

```csharp
void SetSelectedMemberId(int value = -1);
```

**描述**

设置选定成员的ID。

**参数**

- `value`: int类型，表示成员ID，默认为-1。

**返回值**

- NULL

---

## TryRemoveMemberById

**函数原型**

```csharp
bool TryRemoveMemberById(int memberId, out bool needNewTeam, out Team newTeam);
```

**描述**

尝试通过ID移除队伍成员，并判断是否需要新的队伍。

**参数**

- `memberId`: int类型，表示成员ID。
- `needNewTeam`: out bool类型，输出是否需要新队伍。
- `newTeam`: out Team类型，输出新队伍。

**返回值**

- `bool`: 操作是否成功。

------

## TryMemberBreakDown

**函数原型**

```csharp
bool TryMemberBreakDown(int memberId);
```

**描述**

尝试让队伍成员解散。

**参数**

- `memberId`: int类型，表示成员ID。

**返回值**

- `bool`: 操作是否成功。

------

## TryCreateNewTeam

**函数原型**

```csharp
bool TryCreateNewTeam(List<Personal> members, string positionId, out Team team);
```

**描述**

尝试创建新的队伍。

**参数**

- `members`: List<Personal>类型，表示队伍成员。
- `positionId`: string类型，表示位置ID。
- `team`: out Team类型，输出新创建的队伍。

**返回值**

- `bool`: 操作是否成功。

------

## TryCreateStartTeam

**函数原型**

```csharp
bool TryCreateStartTeam(out Team team);
```

**描述**

尝试创建起始队伍。

**参数**

- `team`: out Team类型，输出新创建的起始队伍。

**返回值**

- `bool`: 操作是否成功。

------

## TryRemoveTeam

**函数原型**

```csharp
bool TryRemoveTeam(string teamId);
```

**描述**

尝试移除指定ID的队伍。

**参数**

- `teamId`: string类型，表示队伍ID。

**返回值**

- `bool`: 操作是否成功。

------

## TryReformTeam

**函数原型**

```csharp
bool TryReformTeam(string teamId, string stayTeamId);
```

**描述**

尝试重组队伍。

**参数**

- `teamId`: string类型，表示要重组的队伍ID。
- `stayTeamId`: string类型，表示留在原地的队伍ID。

**返回值**

- `bool`: 操作是否成功。

------

## TrySplitTeam

**函数原型**

```csharp
bool TrySplitTeam(string teamId, string newPosition);
```

**描述**

尝试分割队伍。

**参数**

- `teamId`: string类型，表示要分割的队伍ID。
- `newPosition`: string类型，表示新位置。

**返回值**

- `bool`: 操作是否成功。

------

## TryMoveTeamUpdate

**函数原型**

```csharp
bool TryMoveTeamUpdate(string teamId, out List<string> routeIds);
```

**描述**

尝试更新队伍的移动路线。

**参数**

- `teamId`: string类型，表示队伍ID。
- `routeIds`: out List<string>类型，输出路线ID列表。

**返回值**

- `bool`: 操作是否成功。

------

## EncounterSettlement

**函数原型**

```csharp
void EncounterSettlement();
```

**描述**

处理遭遇战后的结算。

**参数**

- NULL

**返回值**

- NULL

----

## TryRetreatTeam

**函数原型**

```csharp
bool TryRetreatTeam(string teamId);
```

**描述**

尝试撤退指定ID的队伍。

**参数**

- `teamId`: string类型，表示队伍ID。

**返回值**

- `bool`: 操作是否成功。

------

## TryGenerateEnemy

**函数原型**

```csharp
bool TryGenerateEnemy(string position, EnemyTeamType enemyTeamType);
```

**描述**

尝试在指定位置生成敌人。

**参数**

- `position`: string类型，表示位置。
- `enemyTeamType`: EnemyTeamType类型，表示敌人队伍类型。

**返回值**

- `bool`: 操作是否成功。

------

## TryRemoveEnemy

**函数原型**

```csharp
bool TryRemoveEnemy(string position);
```

**描述**

尝试移除指定位置的敌人。

**参数**

- `position`: string类型，表示位置。

**返回值**

- `bool`: 操作是否成功。

------

## TeamInitiativeExplore

**函数原型**

```csharp
void TeamInitiativeExplore(string teamId);
```

**描述**

使队伍主动探索。

**参数**

- `teamId`: string类型，表示队伍ID。

**返回值**

- NULL

------

## ExplorePosition

**函数原型**

```csharp
void ExplorePosition(string position);
```

**描述**

探索指定位置。

**参数**

- `position`: string类型，表示位置。

**返回值**

- NULL

------

## NextTurn

**函数原型**

```csharp
void NextTurn();
```

**描述**

进入下一个回合。

**参数**

- NULL

**返回值**

- NULL

------

## UpdateChest

**函数原型**

```csharp
void UpdateChest();
```

**描述**

更新宝箱信息。

**参数**

- NULL

**返回值**

- NULL

------

## TryRemoveChest

**函数原型**

```csharp
bool TryRemoveChest(string position);
```

**描述**

尝试移除指定位置的宝箱。

**参数**

- `position`: string类型，表示位置。

**返回值**

- `bool`: 操作是否成功。

------

## SavePreset

**函数原型**

```csharp
void SavePreset(int personID, int slot);
```

**描述**

保存特定人物的预设设置。

**参数**

- `personID`: int类型，表示人物ID。
- `slot`: int类型，表示预设槽位。

**返回值**

- NULL

------

## PastePreset

**函数原型**

```csharp
void PastePreset(int personID, int slot);
```

**描述**

粘贴预设到特定人物。

**参数**

- `personID`: int类型，表示人物ID。
- `slot`: int类型，表示预设槽位。

**返回值**

- NULL

------

## ResetAllDungeons

**函数原型**

```csharp
void ResetAllDungeons();
```

**描述**

重置所有地牢。

**参数**

- NULL

**返回值**

- NULL
