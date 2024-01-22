## GetEventContext

**函数原型**

```csharp
int GetEventContext();
```

**描述**

获取当前事件的上下文信息。

**参数**

- NULL

**返回值**

- `int`: 当前事件的上下文信息标识。

------

## OverwriteTemplate

**函数原型**

```csharp
void OverwriteTemplate(ConditionEventTemplate conditionEventTemplate);
```

**描述**

覆盖现有的条件事件模板。

**参数**

- `conditionEventTemplate`: ConditionEventTemplate类型，表示要覆盖的条件事件模板。

**返回值**

- NULL

------

## ForceEvent

**函数原型**

```csharp
void ForceEvent(int templateId, List<int> paramList = null);
```

**描述**

强制触发指定模板ID的事件。

**参数**

- `templateId`: int类型，表示事件模板ID。
- `paramList`: List<int>类型，表示事件参数列表，可选。

**返回值**

- NULL

------

## TryEvent

**函数原型**

```csharp
bool TryEvent(int templateId, List<int> paramList = null);
```

**描述**

尝试触发指定模板ID的事件。

**参数**

- `templateId`: int类型，表示事件模板ID。
- `paramList`: List<int>类型，表示事件参数列表，可选。

**返回值**

- `bool`: 事件是否成功触发。

------

## DelayEvent

**函数原型**

```csharp
void DelayEvent(int templateId, GameDateTime delayTime, bool force, List<int> paramList = null);
```

**描述**

延迟触发指定模板ID的事件。

**参数**

- `templateId`: int类型，表示事件模板ID。
- `delayTime`: GameDateTime类型，表示延迟时间。
- `force`: bool类型，表示是否强制延迟。
- `paramList`: List<int>类型，表示事件参数列表，可选。

**返回值**

- NULL

------

## CancleDelay

**函数原型**

```csharp
void CancleDelay(int templateId);
```

**描述**

取消指定模板ID事件的延迟。

**参数**

- `templateId`: int类型，表示事件模板ID。

**返回值**

- NULL

------

## PickRandomEvent

**函数原型**

```csharp
void PickRandomEvent(string from = "");
```

**描述**

从指定来源随机挑选一个事件。

**参数**

- `from`: string类型，表示事件来源，可选。

**返回值**

- NULL

------

## GetAllConditionEventTemplate

**函数原型**

```csharp
List<ConditionEventTemplate> GetAllConditionEventTemplate();
```

**描述**

获取所有条件事件模板的列表。

**参数**

- NULL

**返回值**

- `List<ConditionEventTemplate>`: 所有条件事件模板的列表。

---

## ContainsEventHistory

**函数原型**

```csharp
bool ContainsEventHistory(int templateId, int selected, int count = 1);
```

**描述**

检查特定事件模板在历史记录中是否存在，并满足指定的选择和数量条件。

**参数**

- `templateId`: int类型，表示事件模板ID。
- `selected`: int类型，表示选定条件。
- `count`: int类型，表示满足条件的次数，默认为1。

**返回值**

- `bool`: 历史记录中是否包含符合条件的事件。

------

## FastTryCondition

**函数原型**

```csharp
bool FastTryCondition(int tid);
```

**描述**

快速尝试满足特定条件。

**参数**

- `tid`: int类型，表示条件ID。

**返回值**

- `bool`: 条件是否被满足。

------

## InitRandomEvents

**函数原型**

```csharp
void InitRandomEvents();
```

**描述**

初始化随机事件。

**参数**

- NULL

**返回值**

- NULL

------

## GetTemplateText

**函数原型**

```csharp
string GetTemplateText(int templateId);
```

**描述**

获取特定事件模板的文本描述。

**参数**

- `templateId`: int类型，表示事件模板ID。

**返回值**

- `string`: 事件模板的文本描述。

------

## GetTemplateName

**函数原型**

```csharp
string GetTemplateName(int templateId);
```

**描述**

获取特定事件模板的名称。

**参数**

- `templateId`: int类型，表示事件模板ID。

**返回值**

- `string`: 事件模板的名称。

------

## GetTemplate

**函数原型**

```csharp
ConditionEventTemplate GetTemplate(int templateId);
```

**描述**

获取特定事件模板的详细信息。

**参数**

- `templateId`: int类型，表示事件模板ID。

**返回值**

- `ConditionEventTemplate`: 事件模板的详细信息。

------

## GetConditionText

**函数原型**

```csharp
string GetConditionText(int templateId);
```

**描述**

获取特定条件模板的文本描述。

**参数**

- `templateId`: int类型，表示条件模板ID。

**返回值**

- `string`: 条件模板的文本描述。