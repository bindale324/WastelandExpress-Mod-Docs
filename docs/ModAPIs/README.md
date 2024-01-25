## 简介

欢迎使用Wasteland Express Lua脚本接口API文档！

本文档旨在为开发者提供必要的信息，以便在Mod开发过程中，高效地使用Lua脚本接口。

> 这些API为游戏开发者提供了强大的工具，以便创建、测试和部署富有创造性的游戏脚本。





## 概览

在每一个分支中，我们的API以`模块名`作为索引，内部是该模块包含的`函数名`。

例如，模块`PeopleMmanager`中的函数`GetPeopleByID`，您应该这样使用：

```lua
local p_info = PeopleManager:GetPeopleByID(123)
```

这样的调用方法，我们在[模块函数文档](https://bindale324.github.io/WastelandExpress-Mod-Docs/#/ModAPIs/module_funcs/README?id=_2-%ef%bc%88%e6%8e%a8%e8%8d%90%e6%96%b9%e6%b3%95%ef%bc%89%e6%a8%a1%e5%9d%97%e5%90%8d%e5%87%bd%e6%95%b0%e5%90%8d%e7%9b%b4%e6%8e%a5%e8%ae%bf%e9%97%ae%e5%87%bd%e6%95%b0)中，已经描述得非常详尽。



以下是我们提供的模块列表：

- AreaItemManager
- BankManager
- BattleManager
- CityManager
- CityPeopleManager
- CookManager
- DailyRecordManager
- DungeonBattleManager
- DungeonCityManager
- EventManager
- FractionManager
- GameTimer
- MapSystem
- MarketManager
- MissionManager
- PeopleEvent
- PeopleManager
- PeopleUpgradeManager
- SearchCityManager
- SelfCityManager
- StateSceneManager
- SynthesisController
- SystemLevelUp
- TaskManager
- TeamManager
- TradeManager
- WeatherManager



## 强调

在`Lua`中，如果您在**调用任何方法**的时候，遇到了`attempt to index a nil value`这种报错，大概率是因为：

**你没有使用`:`调用方法，而是直接使用了`.`符号。**

在Lua中，一定要在最后使用`:`连接您的方法，例如：

```lua
PeopleManager:GetPeopleByID(123)
item.Characteristic:ContainsKey("ItemBuff_DontAutoEat")
```

