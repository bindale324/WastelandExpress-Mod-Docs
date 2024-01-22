## FlexibleRepair

**函数原型**

```csharp
bool FlexibleRepair(int _amount, int _price);
```

**描述**

执行灵活的修复操作。

**参数**

- `_amount`: int类型，表示修复的数量。
- `_price`: int类型，表示每单位的修复价格。

**返回值**

- `bool`: 操作是否成功。

------

## LevelUP

**函数原型**

```csharp
bool LevelUP(int LevelUPID);
```

**描述**

执行升级操作。

**参数**

- `LevelUPID`: int类型，表示升级ID。

**返回值**

- `bool`: 升级操作是否成功。

------

## GetCurrentLevel

**函数原型**

```csharp
int GetCurrentLevel();
```

**描述**

获取当前的等级。

**参数**

- NULL

**返回值**

- `int`: 当前等级。

------

## UnlockCart

**函数原型**

```csharp
bool UnlockCart(int ID);
```

**描述**

解锁特定的购物车。

**参数**

- `ID`: int类型，表示购物车ID。

**返回值**

- `bool`: 操作是否成功。

------

## SwitchCart

**函数原型**

```csharp
bool SwitchCart(int ID, bool needConsume);
```

**描述**

切换至特定的购物车。

**参数**

- `ID`: int类型，表示购物车ID。
- `needConsume`: bool类型，表示是否需要消耗资源。

**返回值**

- `bool`: 操作是否成功。

------

## GetLevelUpData

**函数原型**

```csharp
LevelUpData GetLevelUpData();
```

**描述**

获取升级数据。

**参数**

- NULL

**返回值**

- `LevelUpData`: 升级数据。