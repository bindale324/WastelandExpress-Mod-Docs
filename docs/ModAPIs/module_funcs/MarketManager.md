## InitMarket

**函数原型**

```csharp
void InitMarket();
```

**描述**

初始化市场。

**参数**

- NULL

**返回值**

- NULL

------

## PaidByOthers

**函数原型**

```csharp
void PaidByOthers(int city, int goodId, int amount, float price, bool IsBuy);
```

**描述**

代表其他方在市场上支付。

**参数**

- `city`: int类型，表示城市ID。
- `goodId`: int类型，表示商品ID。
- `amount`: int类型，表示数量。
- `price`: float类型，表示价格。
- `IsBuy`: bool类型，表示是否为购买行为。

**返回值**

- NULL

------

## Pay

**函数原型**

```csharp
void Pay(int city, int goodId, int amount, float price, bool IsBuy, float BarginRate);
```

**描述**

在市场上支付。

**参数**

- `city`: int类型，表示城市ID。
- `goodId`: int类型，表示商品ID。
- `amount`: int类型，表示数量。
- `price`: float类型，表示价格。
- `IsBuy`: bool类型，表示是否为购买行为。
- `BarginRate`: float类型，表示讨价还价率。

**返回值**

- NULL

------

## SelfCityPay

**函数原型**

```csharp
void SelfCityPay(int selfCityID, int tradeCityID, int mapID, int goodId, int amount, float price, bool IsBuy, float BarginRate);
```

**描述**

自建城市在市场上进行支付。

**参数**

- `selfCityID`: int类型，表示自建城市ID。
- `tradeCityID`: int类型，表示贸易城市ID。
- `mapID`: int类型，表示地图ID。
- `goodId`: int类型，表示商品ID。
- `amount`: int类型，表示数量。
- `price`: float类型，表示价格。
- `IsBuy`: bool类型，表示是否为购买行为。
- `BarginRate`: float类型，表示讨价还价率。

**返回值**

- NULL

------

## GetMarket

**函数原型**

```csharp
Market GetMarket(int cityId);
```

**描述**

获取特定城市的市场。

**参数**

- `cityId`: int类型，表示城市ID。

**返回值**

- `Market`: 特定城市的市场。

------

## GetMarket (重载)

**函数原型**

```csharp
Market GetMarket(int cityId, int mapId);
```

**描述**

获取特定地图上特定城市的市场。

**参数**

- `cityId`: int类型，表示城市ID。
- `mapId`: int类型，表示地图ID。

**返回值**

- `Market`: 特定地图上特定城市的市场。

------

## TryGetMarket

**函数原型**

```csharp
bool TryGetMarket(int cityID, out Market m);
```

**描述**

尝试获取特定城市的市场。

**参数**

- `cityID`: int类型，表示城市ID。
- `m`: out Market类型，输出市场。

**返回值**

- `bool`: 操作是否成功。

------

## TryGetMarket (重载)

**函数原型**

```csharp
bool TryGetMarket(int cityID, int mapID, out Market m);
```

**描述**

在特定地图上尝试获取特定城市的市场。

**参数**

- `cityID`: int类型，表示城市ID。
- `mapID`: int类型，表示地图ID。
- `m`: out Market类型，输出市场。

**返回值**

- `bool`: 操作是否成功。

---

## GetPrice

**函数原型**

```csharp
float GetPrice(int id, int citycount, int playercount, bool IsBuy);
```

**描述**

获取特定商品的价格。

**参数**

- `id`: int类型，表示商品ID。
- `citycount`: int类型，表示城市数量。
- `playercount`: int类型，表示玩家数量。
- `IsBuy`: bool类型，表示是否为购买操作。

**返回值**

- `float`: 商品的价格。

------

## GetPrice (重载)

**函数原型**

```csharp
float GetPrice(int cityID, int id, int citycount, int playercount, bool IsBuy);
```

**描述**

获取特定城市中特定商品的价格。

**参数**

- `cityID`: int类型，表示城市ID。
- `id`: int类型，表示商品ID。
- `citycount`: int类型，表示城市数量。
- `playercount`: int类型，表示玩家数量。
- `IsBuy`: bool类型，表示是否为购买操作。

**返回值**

- `float`: 商品的价格。

------

## GetPrice (重载)

**函数原型**

```csharp
float GetPrice(int cityID, int mapId, int id, int citycount, int playercount, bool IsBuy);
```

**描述**

获取特定地图上特定城市中特定商品的价格。

**参数**

- `cityID`: int类型，表示城市ID。
- `mapId`: int类型，表示地图ID。
- `id`: int类型，表示商品ID。
- `citycount`: int类型，表示城市数量。
- `playercount`: int类型，表示玩家数量。
- `IsBuy`: bool类型，表示是否为购买操作。

**返回值**

- `float`: 商品的价格。

------

## BuyMoney

**函数原型**

```csharp
void BuyMoney(int MoneyValue, int Cost, bool IsBuy);
```

**描述**

进行货币交易。

**参数**

- `MoneyValue`: int类型，表示货币价值。
- `Cost`: int类型，表示成本。
- `IsBuy`: bool类型，表示是否为购买操作。

**返回值**

- NULL

------

## BuyMoney (重载)

**函数原型**

```csharp
void BuyMoney(int MoneyValue, int Cost, bool IsBuy, SelfCity selfCity);
```

**描述**

在特定自建城市中进行货币交易。

**参数**

- `MoneyValue`: int类型，表示货币价值。
- `Cost`: int类型，表示成本。
- `IsBuy`: bool类型，表示是否为购买操作。
- `selfCity`: SelfCity类型，表示自建城市。

**返回值**

- NULL

------

## GetRamLackEvent

**函数原型**

```csharp
void GetRamLackEvent();
```

**描述**

获取随机缺乏事件。

**参数**

- NULL

**返回值**

- NULL