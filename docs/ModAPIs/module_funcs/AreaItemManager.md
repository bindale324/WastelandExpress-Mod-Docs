## Unlocked

**函数原型**

```csharp
bool Unlocked(string regionName, string str, int id);
```

**描述**

检查指定区域是否已解锁。

**参数**

- `regionName`: string类型，表示区域名称。
- `str`: string类型，表示附加字符串信息。
- `id`: int类型，表示区域ID。

**返回值**

- `bool`: 表示该区域是否已解锁。

------

## Unlock

**函数原型**

```csharp
void Unlock(string regionName, string str, int id);
```

**描述**

解锁指定区域。

**参数**

- `regionName`: string类型，表示区域名称。
- `str`: string类型，表示附加字符串信息。
- `id`: int类型，表示区域ID。

**返回值**

- NULL

------

## StartHunt

**函数原型**

```csharp
void StartHunt();
```

**描述**

开始狩猎。

**参数**

- NULL

**返回值**

- NULL

------

## GetCurrentShootRate

**函数原型**

```csharp
float GetCurrentShootRate();
```

**描述**

获取当前射击率。

**参数**

- NULL

**返回值**

- `float`: 当前射击率。

------

## Approach

**函数原型**

```csharp
bool Approach();
```

**描述**

接近目标。

**参数**

- NULL

**返回值**

- `bool`: 是否成功接近。

------

## Shoot

**函数原型**

```csharp
bool Shoot();
```

**描述**

射击。

**参数**

- NULL

**返回值**

- `bool`: 射击是否成功。

------

## HoldBreath

**函数原型**

```csharp
bool HoldBreath();
```

**描述**

屏息。

**参数**

- NULL

**返回值**

- `bool`: 是否成功屏息。

------

## EndHunt

**函数原型**

```csharp
void EndHunt();
```

**描述**

结束狩猎。

**参数**

- NULL

**返回值**

- NULL

---

## TryTrackHunt

**函数原型**

```csharp
bool TryTrackHunt();
```

**描述**

尝试跟踪狩猎目标。

**参数**

- NULL

**返回值**

- `bool`: 是否成功跟踪。

------

## Collect

**函数原型**

```csharp
void Collect();
```

**描述**

收集资源或物品。

**参数**

- NULL

**返回值**

- NULL

------

## InitFishingData

**函数原型**

```csharp
void InitFishingData(Action interruptAtion);
```

**描述**

初始化钓鱼数据。

**参数**

- `interruptAtion`: Action类型，表示中断动作。

**返回值**

- NULL

------

## EndFishing

**函数原型**

```csharp
void EndFishing();
```

**描述**

结束钓鱼。

**参数**

- NULL

**返回值**

- NULL

------

## UseRod

**函数原型**

```csharp
void UseRod();
```

**描述**

使用钓竿。

**参数**

- NULL

**返回值**

- NULL