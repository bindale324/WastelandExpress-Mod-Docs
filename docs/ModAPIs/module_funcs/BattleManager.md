## StartBattle

**函数原型**

```csharp
void StartBattle(object _tempArgs);
```

**描述**

开始一场战斗。

**参数**

- `_tempArgs`: object类型，表示战斗的临时参数。

**返回值**

- NULL

------

## AttentionFixEnemyValue

**函数原型**

```csharp
string AttentionFixEnemyValue(int RealValue);
```

**描述**

调整对敌人的关注度影响值。

**参数**

- `RealValue`: int类型，表示实际值。

**返回值**

- `string`: 调整后的关注度影响值。

------

## FallBackRate

**函数原型**

```csharp
int FallBackRate(int Infection, int TotalRate);
```

**描述**

计算战斗中的撤退率。

**参数**

- `Infection`: int类型，表示感染值。
- `TotalRate`: int类型，表示总撤退率。

**返回值**

- `int`: 撤退率。

------

## BattleValueFix

**函数原型**

```csharp
int BattleValueFix();
```

**描述**

调整战斗值。

**参数**

- NULL

**返回值**

- `int`: 调整后的战斗值。

------

## GetCurrentBattle

**函数原型**

```csharp
CurrentBattle GetCurrentBattle();
```

**描述**

获取当前的战斗信息。

**参数**

- NULL

**返回值**

- `CurrentBattle`: 当前战斗的信息。

------

## GetCurrentShotID

**函数原型**

```csharp
List<int> GetCurrentShotID();
```

**描述**

获取当前射击的ID列表。

**参数**

- NULL

**返回值**

- `List<int>`: 当前射击的ID列表。

------

## CreateBattle

**函数原型**

```csharp
void CreateBattle(List<int> a, object args);
```

**描述**

创建一场战斗。

**参数**

- `a`: List<int>类型，表示参与战斗的单位ID列表。
- `args`: object类型，表示战斗参数。

**返回值**

- NULL

------

## CreateBattle (重载)

**函数原型**

```csharp
void CreateBattle(BattleArg arg);
```

**描述**

创建一场战斗，使用特定的战斗参数。

**参数**

- `arg`: BattleArg类型，表示战斗参数。

**返回值**

- NULL

------

## CurEneShootNum

**函数原型**

```csharp
int CurEneShootNum();
```

**描述**

获取当前敌人的射击次数。

**参数**

- NULL

**返回值**

- `int`: 当前敌人的射击次数。

------

## CurEneAccuracy

**函数原型**

```csharp
int CurEneAccuracy();
```

**描述**

获取当前敌人的射击精准度。

**参数**

- NULL

**返回值**

- `int`: 当前敌人的射击精准度。

------

## CurEneShootDamage

**函数原型**

```csharp
int CurEneShootDamage(out string Text);
```

**描述**

获取当前敌人的射击伤害。

**参数**

- `Text`: out string类型，输出伤害相关的文本描述。

**返回值**

- `int`: 当前敌人的射击伤害。

------

## UpdatePeopleState

**函数原型**

```csharp
void UpdatePeopleState();
```

**描述**

更新人物状态。

**参数**

- NULL

**返回值**

- NULL

---

## PushToClose

**函数原型**

```csharp
void PushToClose();
```

**描述**

推动战斗进入近战阶段。

**参数**

- NULL

**返回值**

- NULL

------

## PushForward

**函数原型**

```csharp
void PushForward(bool defend = false, int SpeedPlus = 1);
```

**描述**

向前推进战斗位置，可选择是否进行防御。

**参数**

- `defend`: bool类型，表示是否进行防御，默认为false。
- `SpeedPlus`: int类型，表示速度增加，默认为1。

**返回值**

- NULL

------

## CloseCombat

**函数原型**

```csharp
void CloseCombat(out string Text);
```

**描述**

进行近战战斗。

**参数**

- `Text`: out string类型，输出战斗相关的文本描述。

**返回值**

- NULL

------

## PeopleShoot

**函数原型**

```csharp
void PeopleShoot(int PeopleID, out string Text);
```

**描述**

进行射击操作。

**参数**

- `PeopleID`: int类型，表示人物ID。
- `Text`: out string类型，输出射击相关的文本描述。

**返回值**

- NULL

------

## PeopleThrow

**函数原型**

```csharp
void PeopleThrow(int PeopleID, out string Text);
```

**描述**

进行投掷操作。

**参数**

- `PeopleID`: int类型，表示人物ID。
- `Text`: out string类型，输出投掷相关的文本描述。

**返回值**

- NULL

------

## CheckDieOfZombie

**函数原型**

```csharp
void CheckDieOfZombie();
```

**描述**

检查僵尸是否死亡。

**参数**

- NULL

**返回值**

- NULL

------

## BattleLost

**函数原型**

```csharp
void BattleLost();
```

**描述**

处理战斗失败的情况。

**参数**

- NULL

**返回值**

- NULL

------

## SelfCityLose

**函数原型**

```csharp
void SelfCityLose(string selfcity = "");
```

**描述**

处理自建城市的失败情况。

**参数**

- `selfcity`: string类型，表示自建城市的名称，默认为空字符串。

**返回值**

- NULL

------

## GetAllShootBullet

**函数原型**

```csharp
int GetAllShootBullet();
```

**描述**

获取所有射击的子弹数量。

**参数**

- NULL

**返回值**

- `int`: 所有射击的子弹数量。

------

## AllShoot

**函数原型**

```csharp
bool AllShoot();
```

**描述**

执行全部射击操作。

**参数**

- NULL

**返回值**

- `bool`: 操作是否成功。

---

## IsHuman

**函数原型**

```csharp
bool IsHuman(string args);
```

**描述**

判断给定参数是否表示人类。

**参数**

- `args`: string类型，表示需要判断的参数。

**返回值**

- `bool`: 参数是否表示人类。

------

## SpecialArgs

**函数原型**

```csharp
int SpecialArgs(string args);
```

**描述**

处理并返回特殊参数的值。

**参数**

- `args`: string类型，表示特殊参数。

**返回值**

- `int`: 特殊参数的值。

------

## EnemyShoot

**函数原型**

```csharp
bool EnemyShoot(out string Text, bool Defend = false);
```

**描述**

敌人进行射击操作。

**参数**

- `Text`: out string类型，输出射击相关的文本描述。
- `Defend`: bool类型，表示是否进行防御，默认为false。

**返回值**

- `bool`: 操作是否成功。

------

## TryAffectPeople

**函数原型**

```csharp
void TryAffectPeople(Personal p);
```

**描述**

尝试对特定人物产生影响。

**参数**

- `p`: Personal类型，表示人物。

**返回值**

- NULL