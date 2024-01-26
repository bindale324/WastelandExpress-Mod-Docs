# Wasteland Express Data Interface Description

## `uiname`

顾名思义，游戏中到底有哪些UI

+ "NewEventUI"
+ "WaitTime"
+ "BattleWindow"
+ "UnderAttackUI"
+ "FallBackUI", 
+ "DialogWindowUI", 
+ "NewMapUI", 
+ "TeamWindow", 
+ "FractionPanel", 
+ "MissionPanelUI",
+ "TaskPanelUI", 
+ "WareHouseWindow", 
+ "PartsPanel", 
+ "Synthesis", 
+ "HeroWindow", 
+ "HuntUI", 
+ "CookUI", 
+ "FishingUI", 
+ "EatFoodUI", 
+ "SCBattleWindow",
+ "CureSelfCityUI", 
+ "CaravanShopWindow", 
+ "RoadBuildUI", 
+ "BuildPointUI", 
+ "DungeonPrepareUI", 
+ "MissionAndTaskMapUI"

如何通过Lua脚本打开他们：

> CS.QxFramework.Core.UIManager.Instance:Open("xxx")   // 这里填您想要打开的UI名



## `Food`

`Food`类型中，到底有多少属性呢？

+ `taste`: string
+ `FullName`: string  带品质说明的字符串，例如：“【普通】西红柿鸡蛋汤”
+ `Name`: string  普通的菜名，例如：“西红柿鸡蛋汤”
+ `Description`: string
+ `HungryReduce`: int
+ `MoodReduce`: int 



> `Food`, `Item`等类型，在Lua中，如果使用`type`关键字打印出来，将会打印`userdata`，你是看不出来它到底是什么类型的。



## `List<>`

`List`类型，同理，打印出来也是`userdata`

`List`是链表，在Lua中，**不遵守** `table`类型的约束，**下标从`0`开始！！**