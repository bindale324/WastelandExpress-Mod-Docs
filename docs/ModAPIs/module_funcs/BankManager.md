## CheckBreak

**函数原型**

```csharp
bool CheckBreak();
```

**描述**

检查是否发生中断。

**参数**

- NULL

**返回值**

- `bool`: 是否发生了中断。

------

## CreateAnDeposite

**函数原型**

```csharp
void CreateAnDeposite(int principalGear);
```

**描述**

创建一个存款。

**参数**

- `principalGear`: int类型，表示存款的本金。

**返回值**

- NULL

------

## TakeDeposite

**函数原型**

```csharp
void TakeDeposite(int principalGear);
```

**描述**

取出存款。

**参数**

- `principalGear`: int类型，表示存款的本金。

**返回值**

- NULL

------

## GetBankData

**函数原型**

```csharp
BankData GetBankData();
```

**描述**

获取银行数据。

**参数**

- NULL

**返回值**

- `BankData`: 银行的数据信息。

------

## CreateAnLoan

**函数原型**

```csharp
void CreateAnLoan(int principalGear, int TimeMinutes);
```

**描述**

创建一个贷款。

**参数**

- `principalGear`: int类型，表示贷款的本金。
- `TimeMinutes`: int类型，表示贷款时间（分钟）。

**返回值**

- NULL

------

## PayLoan

**函数原型**

```csharp
void PayLoan();
```

**描述**

支付贷款。

**参数**

- NULL

**返回值**

- NULL

------

## LoanExpired

**函数原型**

```csharp
void LoanExpired();
```

**描述**

处理贷款到期的情况。

**参数**

- NULL

**返回值**

- NULL

------

## CreateAnFinance

**函数原型**

```csharp
void CreateAnFinance(int principalGear, int TimeMinutes, float HighProfit, float LowProfit);
```

**描述**

创建一个金融投资。

**参数**

- `principalGear`: int类型，表示投资的本金。
- `TimeMinutes`: int类型，表示投资时间（分钟）。
- `HighProfit`: float类型，表示高收益。
- `LowProfit`: float类型，表示低收益。

**返回值**

- NULL

------

## GetProfit

**函数原型**

```csharp
void GetProfit();
```

**描述**

获取投资收益。

**参数**

- NULL

**返回值**

- NULL

------

## FinaceExpired

**函数原型**

```csharp
void FinaceExpired();
```

**描述**

处理金融投资到期的情况。

**参数**

- NULL

**返回值**

- NULL

------

## GetInfo

**函数原型**

```csharp
void GetInfo();
```

**描述**

获取信息。

**参数**

- NULL

**返回值**

- NULL