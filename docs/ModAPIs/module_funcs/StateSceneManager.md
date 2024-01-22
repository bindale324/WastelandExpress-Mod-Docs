## 前置

**属性**

```
StateSceneResult ParamsResult { get; }
```

**描述**

获取场景状态的参数结果。

**用法**

- 通过该属性可以获取当前场景状态的参数结果。

------

## GetCommandState

**函数原型**

```csharp
string GetCommandState();
```

**描述**

获取当前命令状态。

**参数**

- NULL

**返回值**

- `string`: 当前命令状态的描述。

------

## ChangeCommandState

**函数原型**

```csharp
void ChangeCommandState(string name);
```

**描述**

更改当前命令状态。

**参数**

- `name`: string类型，表示命令状态的名称。

**返回值**

- NULL

------

## GetEnableCommand

**函数原型**

```csharp
void GetEnableCommand(List<CommandButtonInfo> enableCommands);
```

**描述**

获取可用的命令列表。

**参数**

- `enableCommands`: List<CommandButtonInfo>类型，表示可用命令的列表。

**返回值**

- NULL

------

## SetParams

**函数原型**

```csharp
void SetParams(string name, int value, string key = "");
```

**描述**

设置参数值。

**参数**

- `name`: string类型，表示参数名称。
- `value`: int类型，表示参数值。
- `key`: string类型，表示参数键，默认为空字符串。

**返回值**

- NULL

------

## RemoveParams

**函数原型**

```csharp
bool RemoveParams(string name, string key = "");
```

**描述**

移除特定参数。

**参数**

- `name`: string类型，表示参数名称。
- `key`: string类型，表示参数键，默认为空字符串。

**返回值**

- `bool`: 操作是否成功。

------

## GetCityId

**函数原型**

```csharp
int GetCityId();
```

**描述**

获取当前城市ID。

**参数**

- NULL

**返回值**

- `int`: 当前城市ID。

------

## SetCityId

**函数原型**

```csharp
void SetCityId(int id);
```

**描述**

设置当前城市ID。

**参数**

- `id`: int类型，表示城市ID。

**返回值**

- NULL

------

## GetEventId

**函数原型**

```csharp
int GetEventId();
```

**描述**

获取当前事件ID。

**参数**

- NULL

**返回值**

- `int`: 当前事件ID。

------

## SetEventId

**函数原型**

```csharp
void SetEventId(int eventId);
```

**描述**

设置当前事件ID。

**参数**

- `eventId`: int类型，表示事件ID。

**返回值**

- NULL

------

## TryGetParams

**函数原型**

```csharp
bool TryGetParams(string name, out int value);
```

**描述**

尝试获取特定参数的值。

**参数**

- `name`: string类型，表示参数名称。
- `value`: out int类型，输出参数值。

**返回值**

- `bool`: 操作是否成功。

------

## CheckUpdateCommand

**函数原型**

```csharp
void CheckUpdateCommand();
```

**描述**

检查并更新命令状态。

**参数**

- NULL

**返回值**

- NULL