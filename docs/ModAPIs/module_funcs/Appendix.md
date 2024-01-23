# Appendix



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