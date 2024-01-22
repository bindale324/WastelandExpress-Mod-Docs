## GetNow

**函数原型**

```csharp
GameDateTime GetNow();
```

**描述**

获取当前游戏时间。

**参数**

- NULL

**返回值**

- `GameDateTime`: 当前游戏时间。

------

## RegisterTimeRepeat

**函数原型**

```csharp
void RegisterTimeRepeat(TimeUpdate action, GameDateTime interval, GameTimerFuncTag tag = GameTimerFuncTag.Default);
```

**描述**

注册一个定期触发的函数，根据游戏时间周期性执行。

**参数**

- `action`: TimeUpdate委托，参数为`GameDateTime`（代表执行函数时的时间）；返回值为bool，返回true会打断时间的流逝。
- `interval`: `GameDateTime`类型，表示函数执行的时间间隔。
- `tag`: `GameTimerFuncTag`类型，用于过滤哪些函数会执行。详情见`StepMinute`方法。

**返回值**

- NULL

------

## StepMinute

**函数原型**

```csharp
bool StepMinute(float stepTime, GameTimerFuncTag filter = GameTimerFuncTag.OnlyNoDrive, bool showEffect = true);
```

**描述**

让游戏时间向前推进一段指定的时间。

**参数**

- `stepTime`: float类型，表示要度过的时间。
- `filter`: `GameTimerFuncTag`类型，表示过滤条件，用于决定哪些注册函数会在这段时间内触发，默认为`GameTimerFuncTag.OnlyNoDrive`。
- `showEffect`: bool类型，表示是否展示效果，默认为true。

**返回值**

- `bool`: 时间推进是否成功。

---

## StopStep

**函数原型**

```csharp
void StopStep();
```

**描述**

停止快进

**参数**

- NULL

**返回值**

- NULL