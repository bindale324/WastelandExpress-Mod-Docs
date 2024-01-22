## ChangeFractionInfection

**函数原型**

```csharp
void ChangeFractionInfection(CityData city, string FractionID, int value, bool Dialog);
```

**描述**

改变指定城市中特定派系的影响力。

**参数**

- `city`: CityData类型，表示城市数据。
- `FractionID`: string类型，表示派系ID。
- `value`: int类型，表示影响力变化值。
- `Dialog`: bool类型，表示是否显示对话，用于用户交互。

**返回值**

- NULL

------

## ChangeFractionFriendly

**函数原型**

```csharp
void ChangeFractionFriendly(string FractionID, int value, bool Hint = true);
```

**描述**

改变与特定派系的友好程度。

**参数**

- `FractionID`: string类型，表示派系ID。
- `value`: int类型，表示友好程度变化值。
- `Hint`: bool类型，表示是否显示提示，默认为true。

**返回值**

- NULL

------

## GetFractionInfectionPercentage

**函数原型**

```csharp
void GetFractionInfectionPercentage(CityData city, out Dictionary<string, float> InfluenceData);
```

**描述**

获取特定城市中各派系的影响力百分比。

**参数**

- `city`: CityData类型，表示城市数据。
- `InfluenceData`: out Dictionary<string, float>类型，输出各派系的影响力百分比。

**返回值**

- NULL

------

## GetInfluencePoint

**函数原型**

```csharp
int GetInfluencePoint(CityData city, int FractionID);
```

**描述**

获取特定城市中特定派系的影响力点数。

**参数**

- `city`: CityData类型，表示城市数据。
- `FractionID`: int类型，表示派系ID。

**返回值**

- `int`: 派系的影响力点数。

------

## GetCurrentCityController

**函数原型**

```csharp
string GetCurrentCityController(CityData city);
```

**描述**

获取特定城市当前的控制者。

**参数**

- `city`: CityData类型，表示城市数据。

**返回值**

- `string`: 当前城市控制者的名称。

------

## GetCurrentCityController (重载)

**函数原型**

```csharp
string GetCurrentCityController(int city);
```

**描述**

根据城市ID获取当前的城市控制者。

**参数**

- `city`: int类型，表示城市ID。

**返回值**

- `string`: 当前城市控制者的名称。

------

## GetFractionAttitude

**函数原型**

```csharp
int GetFractionAttitude(string ID);
```

**描述**

获取特定派系的态度值。

**参数**

- `ID`: string类型，表示派系ID。

**返回值**

- `int`: 派系的态度值。

------

## GetFractionName

**函数原型**

```csharp
string GetFractionName(string ID);
```

**描述**

获取特定派系的名称。

**参数**

- `ID`: string类型，表示派系ID。

**返回值**

- `string`: 派系的名称。

------

## GetFractionNews

**函数原型**

```csharp
void GetFractionNews();
```

**描述**

获取关于派系的最新消息。

**参数**

- NULL

**返回值**

- NULL

---

## BuyStop

**函数原型**

```csharp
void BuyStop(int CostValue, bool IsBuy, Action AffirmAction, Action RefuseAction);
```

**描述**

处理购买停止的情况，执行相应的确认或拒绝操作。

**参数**

- `CostValue`: int类型，表示成本值。
- `IsBuy`: bool类型，表示是否为购买行为。
- `AffirmAction`: Action类型，表示确认操作。
- `RefuseAction`: Action类型，表示拒绝操作。

**返回值**

- NULL

------

## ParticipantFraction

**函数原型**

```csharp
void ParticipantFraction(string FractionID);
```

**描述**

加入特定派系。

**参数**

- `FractionID`: string类型，表示派系ID。

**返回值**

- NULL

------

## LeaveFraction

**函数原型**

```csharp
void LeaveFraction();
```

**描述**

离开当前所在派系。

**参数**

- NULL

**返回值**

- NULL

------

## GetCurrentFraction

**函数原型**

```csharp
int GetCurrentFraction();
```

**描述**

获取当前所在派系的ID。

**参数**

- NULL

**返回值**

- `int`: 当前派系的ID。

------

## CheckCurrentCityFractionOrder

**函数原型**

```csharp
bool CheckCurrentCityFractionOrder(string FractionID);
```

**描述**

检查当前城市中特定派系的排序情况。

**参数**

- `FractionID`: string类型，表示派系ID。

**返回值**

- `bool`: 是否符合派系排序。

------

## CheckCityFractionOrder

**函数原型**

```csharp
bool CheckCityFractionOrder(string FractionID, CityData cityData);
```

**描述**

检查指定城市中特定派系的排序情况。

**参数**

- `FractionID`: string类型，表示派系ID。
- `cityData`: CityData类型，表示城市数据。

**返回值**

- `bool`: 是否符合派系排序。

------

## FractionData

**函数原型**

```csharp
FractionData fractionData();
```

**描述**

获取当前派系的数据信息。

**参数**

- NULL

**返回值**

- `FractionData`: 当前派系的数据信息。