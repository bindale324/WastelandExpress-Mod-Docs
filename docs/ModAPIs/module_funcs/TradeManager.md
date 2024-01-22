## InitTraderAllData

**函数原型**

```csharp
void InitTraderAllData();
```

**描述**

初始化所有交易者的数据。

**参数**

- NULL

**返回值**

- NULL

------

## GetCurrentTraderData

**函数原型**

```csharp
List<Items> GetCurrentTraderData(int ID);
```

**描述**

获取当前交易者的商品数据。

**参数**

- `ID`: int类型，表示交易者ID。

**返回值**

- `List<Items>`: 当前交易者的商品列表。

------

## CheckValueRate

**函数原型**

```csharp
float CheckValueRate(Dictionary<int, int> TradeSellContent, Dictionary<int, int> TradeBuyContent, int CurrentTrader);
```

**描述**

检查交易内容的价值比率。

**参数**

- `TradeSellContent`: Dictionary<int, int>类型，表示卖出的商品及其数量。
- `TradeBuyContent`: Dictionary<int, int>类型，表示买入的商品及其数量。
- `CurrentTrader`: int类型，表示当前交易者ID。

**返回值**

- `float`: 交易的价值比率。

------

## TradeAction

**函数原型**

```csharp
void TradeAction(Dictionary<int, int> TradeSellContent, Dictionary<int, int> TradeBuyContent, int CurrentTraderID);
```

**描述**

执行交易行为。

**参数**

- `TradeSellContent`: Dictionary<int, int>类型，表示卖出的商品及其数量。
- `TradeBuyContent`: Dictionary<int, int>类型，表示买入的商品及其数量。
- `CurrentTraderID`: int类型，表示当前交易者ID。

**返回值**

- NULL

------

## IsWant

**函数原型**

```csharp
bool IsWant(int ID, int CurrentTrader);
```

**描述**

检查当前交易者是否需要特定商品。

**参数**

- `ID`: int类型，表示商品ID。
- `CurrentTrader`: int类型，表示当前交易者ID。

**返回值**

- `bool`: 当前交易者是否需要该商品。