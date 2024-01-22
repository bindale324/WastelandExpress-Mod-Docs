## GetCurrentBattle

**函数原型**

```csharp
CurrentDungeonBattle GetCurrentBattle();
```

**描述**

获取当前的地牢战斗信息。

**参数**

- NULL

**返回值**

- `CurrentDungeonBattle`: 当前地牢战斗的详细信息。

------

## StartDungeonBattle

**函数原型**

```csharp
void StartDungeonBattle(string _teamId, string _enemyPosId, bool isSurprise, bool activeBattle, bool hasStunGrenade);
```

**描述**

开始一场地牢战斗。

**参数**

- `_teamId`: string类型，表示队伍ID。
- `_enemyPosId`: string类型，表示敌人位置ID。
- `isSurprise`: bool类型，表示是否是突袭。
- `activeBattle`: bool类型，表示战斗是否主动。
- `hasStunGrenade`: bool类型，表示是否有眩晕手雷。

**返回值**

- NULL

------

## CheckInDungeonBattle

**函数原型**

```csharp
bool CheckInDungeonBattle();
```

**描述**

检查是否处于地牢战斗中。

**参数**

- NULL

**返回值**

- `bool`: 是否处于地牢战斗中。

------

## SwitchTurn

**函数原型**

```csharp
void SwitchTurn(bool toPlayer);
```

**描述**

切换战斗回合。

**参数**

- `toPlayer`: bool类型，表示是否切换到玩家回合。

**返回值**

- NULL

------

## CheckAreaState

**函数原型**

```csharp
AreaState CheckAreaState(int areaIndex);
```

**描述**

检查特定区域的状态。

**参数**

- `areaIndex`: int类型，表示区域索引。

**返回值**

- `AreaState`: 指定区域的状态。

------

## SelectMember

**函数原型**

```csharp
void SelectMember(int id = -1);
```

**描述**

选择地牢中的成员。

**参数**

- `id`: int类型，表示成员ID，默认为-1。

**返回值**

- NULL

------

## TryGetCurrentMember

**函数原型**

```csharp
bool TryGetCurrentMember(out DungeonPersonal personal);
```

**描述**

尝试获取当前地牢成员的信息。

**参数**

- `personal`: out DungeonPersonal类型，输出当前成员的信息。

**返回值**

- `bool`: 操作是否成功。

------

## SwitchAttackMode

**函数原型**

```csharp
void SwitchAttackMode(int memberId, AttackMode mode = AttackMode.None);
```

**描述**

切换成员的攻击模式。

**参数**

- `memberId`: int类型，表示成员ID。
- `mode`: AttackMode类型，表示攻击模式，默认为None。

**返回值**

- NULL

------

## TryGetMemberPos

**函数原型**

```csharp
bool TryGetMemberPos(int personal_Id, out int areaIndex, out int areaPos);
```

**描述**

尝试获取地牢成员的位置信息。

**参数**

- `personal_Id`: int类型，表示个人ID。
- `areaIndex`: out int类型，输出区域索引。
- `areaPos`: out int类型，输出区域位置。

**返回值**

- `bool`: 操作是否成功。

---

## CanMemberMoveForward

**函数原型**

```csharp
bool CanMemberMoveForward(int personalId, out int originAreaIndex);
```

**描述**

检查特定成员是否能向前移动。

**参数**

- `personalId`: int类型，表示个人ID。
- `originAreaIndex`: out int类型，输出原始区域索引。

**返回值**

- `bool`: 成员是否能向前移动。

------

## TryMemberMoveForward

**函数原型**

```csharp
bool TryMemberMoveForward(int personalId);
```

**描述**

尝试让特定成员向前移动。

**参数**

- `personalId`: int类型，表示个人ID。

**返回值**

- `bool`: 操作是否成功。

------

## CanMemberMoveBackward

**函数原型**

```csharp
bool CanMemberMoveBackward(int personalId, out int originAreaIndex);
```

**描述**

检查特定成员是否能向后移动。

**参数**

- `personalId`: int类型，表示个人ID。
- `originAreaIndex`: out int类型，输出原始区域索引。

**返回值**

- `bool`: 成员是否能向后移动。

------

## TryMemberMoveBackward

**函数原型**

```csharp
bool TryMemberMoveBackward(int personalId);
```

**描述**

尝试让特定成员向后移动。

**参数**

- `personalId`: int类型，表示个人ID。

**返回值**

- `bool`: 操作是否成功。

------

## CanMemberDefend

**函数原型**

```csharp
bool CanMemberDefend(int personal_Id);
```

**描述**

检查特定成员是否能防御。

**参数**

- `personal_Id`: int类型，表示个人ID。

**返回值**

- `bool`: 成员是否能进行防御。

------

## TryMemberDefend

**函数原型**

```csharp
bool TryMemberDefend(int personalId);
```

**描述**

尝试让特定成员进行防御。

**参数**

- `personalId`: int类型，表示个人ID。

**返回值**

- `bool`: 操作是否成功。

------

## TryMemberAttack

**函数原型**

```csharp
bool TryMemberAttack(int personalId, int enemyId);
```

**描述**

尝试让特定成员攻击敌人。

**参数**

- `personalId`: int类型，表示个人ID。
- `enemyId`: int类型，表示敌人ID。

**返回值**

- `bool`: 操作是否成功。

------

## CheckEnemyInAttackRange

**函数原型**

```csharp
bool CheckEnemyInAttackRange(int memberId, int enemyUniqueId);
```

**描述**

检查敌人是否在成员的攻击范围内。

**参数**

- `memberId`: int类型，表示成员ID。
- `enemyUniqueId`: int类型，表示敌人唯一ID。

**返回值**

- `bool`: 敌人是否在攻击范围内。

------

## CanMemberHit

**函数原型**

```csharp
bool CanMemberHit(int personal_Id, out string Reason);
```

**描述**

检查特定成员是否能命中目标，并提供原因。

**参数**

- `personal_Id`: int类型，表示个人ID。
- `Reason`: out string类型，输出不能命中的原因。

**返回值**

- `bool`: 成员是否能命中目标。

---

## CanMemberStrike

**函数原型**

```csharp
bool CanMemberStrike(int personal_Id, out string Reason);
```

**描述**

检查特定成员是否能进行打击攻击，并提供原因。

**参数**

- `personal_Id`: int类型，表示个人ID。
- `Reason`: out string类型，输出不能进行打击攻击的原因。

**返回值**

- `bool`: 成员是否能进行打击攻击。

------

## CanMemberShoot

**函数原型**

```csharp
bool CanMemberShoot(int personal_Id, out string Reason);
```

**描述**

检查特定成员是否能进行射击，并提供原因。

**参数**

- `personal_Id`: int类型，表示个人ID。
- `Reason`: out string类型，输出不能进行射击的原因。

**返回值**

- `bool`: 成员是否能进行射击。

------

## CanMemberThrow

**函数原型**

```csharp
bool CanMemberThrow(int personal_Id, out string Reason);
```

**描述**

检查特定成员是否能进行投掷，并提供原因。

**参数**

- `personal_Id`: int类型，表示个人ID。
- `Reason`: out string类型，输出不能进行投掷的原因。

**返回值**

- `bool`: 成员是否能进行投掷。

------

## CanMemberUseItem

**函数原型**

```csharp
bool CanMemberUseItem(int personal_Id);
```

**描述**

检查特定成员是否能使用物品。

**参数**

- `personal_Id`: int类型，表示个人ID。

**返回值**

- `bool`: 成员是否能使用物品。

------

## TryMemberUseItemInBattle

**函数原型**

```csharp
bool TryMemberUseItemInBattle(int itemId, int memberId);
```

**描述**

尝试让特定成员在战斗中使用物品。

**参数**

- `itemId`: int类型，表示物品ID。
- `memberId`: int类型，表示成员ID。

**返回值**

- `bool`: 操作是否成功。

------

## TryCureMemberInBattle

**函数原型**

```csharp
bool TryCureMemberInBattle(int memberId, Items Medicine);
```

**描述**

尝试在战斗中治疗特定成员。

**参数**

- `memberId`: int类型，表示成员ID。
- `Medicine`: Items类型，表示使用的药物。

**返回值**

- `bool`: 操作是否成功。

------

## TryRemoveMember

**函数原型**

```csharp
bool TryRemoveMember(int memberId);
```

**描述**

尝试移除特定成员。

**参数**

- `memberId`: int类型，表示成员ID。

**返回值**

- `bool`: 操作是否成功。

------

## GetLastMemberAreaPos

**函数原型**

```csharp
int GetLastMemberAreaPos();
```

**描述**

获取最后一个成员的区域位置。

**参数**

- NULL

**返回值**

- `int`: 最后一个成员的区域位置。

------

## GetFirstMemberAreaPos

**函数原型**

```csharp
int GetFirstMemberAreaPos();
```

**描述**

获取第一个成员的区域位置。

**参数**

- NULL

**返回值**

- `int`: 第一个成员的区域位置。

------

## SelectEnemy

**函数原型**

```csharp
void SelectEnemy(int id = -1);
```

**描述**

选择一个敌人。

**参数**

- `id`: int类型，表示敌人ID，默认为-1。

**返回值**

- NULL

---

## TryGetEnemyPos

**函数原型**

```csharp
bool TryGetEnemyPos(int enemy_Id, out int areaIndex, out int areaPos);
```

**描述**

尝试获取特定敌人的位置信息。

**参数**

- `enemy_Id`: int类型，表示敌人ID。
- `areaIndex`: out int类型，输出区域索引。
- `areaPos`: out int类型，输出区域位置。

**返回值**

- `bool`: 操作是否成功。

------

## CanEnemyMoveForward

**函数原型**

```csharp
bool CanEnemyMoveForward(int enemyUID, out int originAreaIndex);
```

**描述**

检查特定敌人是否能向前移动。

**参数**

- `enemyUID`: int类型，表示敌人唯一ID。
- `originAreaIndex`: out int类型，输出原始区域索引。

**返回值**

- `bool`: 敌人是否能向前移动。

------

## TryEnemyMoveForward

**函数原型**

```csharp
bool TryEnemyMoveForward(int enemyUID);
```

**描述**

尝试让特定敌人向前移动。

**参数**

- `enemyUID`: int类型，表示敌人唯一ID。

**返回值**

- `bool`: 操作是否成功。

------

## CanEnemyMoveBackward

**函数原型**

```csharp
bool CanEnemyMoveBackward(int enemyUID, out int originPos);
```

**描述**

检查特定敌人是否能向后移动。

**参数**

- `enemyUID`: int类型，表示敌人唯一ID。
- `originPos`: out int类型，输出原始位置。

**返回值**

- `bool`: 敌人是否能向后移动。

------

## TryEnemyMoveBackward

**函数原型**

```csharp
bool TryEnemyMoveBackward(int enemyUID);
```

**描述**

尝试让特定敌人向后移动。

**参数**

- `enemyUID`: int类型，表示敌人唯一ID。

**返回值**

- `bool`: 操作是否成功。

------

## TryChangeEnemyArea

**函数原型**

```csharp
bool TryChangeEnemyArea(int enemyUid, int targetAreaIndex);
```

**描述**

尝试更改特定敌人的区域位置。

**参数**

- `enemyUid`: int类型，表示敌人唯一ID。
- `targetAreaIndex`: int类型，表示目标区域索引。

**返回值**

- `bool`: 操作是否成功。

------

## CanEnemyAttack

**函数原型**

```csharp
bool CanEnemyAttack(int enemyUID, out List<int> targetList);
```

**描述**

检查特定敌人是否能进行攻击，并获取潜在的目标列表。

**参数**

- `enemyUID`: int类型，表示敌人唯一ID。
- `targetList`: out List<int>类型，输出潜在的目标ID列表。

**返回值**

- `bool`: 敌人是否能进行攻击。

------

## TryEnemyAttack

**函数原型**

```csharp
bool TryEnemyAttack(int uniqueId, int memberId);
```

**描述**

尝试让特定敌人攻击特定成员。

**参数**

- `uniqueId`: int类型，表示敌人唯一ID。
- `memberId`: int类型，表示成员ID。

**返回值**

- `bool`: 操作是否成功。

------

## TryRemoveEnemy

**函数原型**

```csharp
bool TryRemoveEnemy(int enemyUID);
```

**描述**

尝试移除特定敌人。

**参数**

- `enemyUID`: int类型，表示敌人唯一ID。

**返回值**

- `bool`: 操作是否成功。

---

## BattleWin

**函数原型**

```csharp
void BattleWin();
```

**描述**

处理战斗胜利的情况。

**参数**

- NULL

**返回值**

- NULL

------

## BattleRetreat

**函数原型**

```csharp
void BattleRetreat();
```

**描述**

处理战斗撤退的情况。

**参数**

- NULL

**返回值**

- NULL

------

## TryBattleRetreat

**函数原型**

```csharp
bool TryBattleRetreat();
```

**描述**

尝试在战斗中撤退。

**参数**

- NULL

**返回值**

- `bool`: 撤退操作是否成功。

------

## CanBattleRetreat

**函数原型**

```csharp
bool CanBattleRetreat(out List<int> memberIdCost);
```

**描述**

检查是否能进行战斗撤退，并获取可能的成员代价。

**参数**

- `memberIdCost`: out List<int>类型，输出可能受影响的成员ID列表。

**返回值**

- `bool`: 是否能进行战斗撤退。

------

## BattleLose

**函数原型**

```csharp
void BattleLose();
```

**描述**

处理战斗失败的情况。

**参数**

- NULL

**返回值**

- NULL

------

## ExecuteEnemyActions

**函数原型**

```csharp
IEnumerator ExecuteEnemyActions();
```

**描述**

执行敌人的行动序列。

**参数**

- NULL

**返回值**

- `IEnumerator`: 敌人行动的迭代器。
