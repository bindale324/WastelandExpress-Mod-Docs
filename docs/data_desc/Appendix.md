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

比如说，如果您在逆向之后查看到了一个`List`类型数据的源码，并且在Lua中接收到了这样的数据接口，您应该这样使用：

```lua
function OnCook(ingredients, results)
	-- 比如说在这里，`results`就是一个`List<Food>`类型的数据
    -- 您可以：
    local food1 = results[0];
    local food1Name = food1.Name;
    print(food1Name);
end
```







## `Personal`

`Personal`类中的属性如下：

+ **public** **int** *_image*;
+ **public** **int** *_battle*;
+ **public** **int** *_body*;
+ **public** **int** *_defence*;
+ **public** **int** *Gender*;
+ **public** **int** *Aptitude*;
+ **public** **int** *_body2*;
+ **public** **int** *_attention*;
+ **public** **int** *_eloquence*;
+ **public** **int** *_craft*;
+ **public** **int** *_intelligence*;
+ **public** **int** *_morality*;
+ **public** **int** *_farm*;
+ **public** **int** *_cook*;
+ **public** **int** *_cultivation*;
+ **public** **int** *_hunt*;
+ **public** **int** *_fishing*;
+ **public** **int** *_collect*;
+ **public** **int** *_charm*;
+ **public** **int** *_shoot*;
+ **public** **int** *_accuracy*;
+ **public** **int** *PeopleID*;
+ **public** string *_name*;
+ **public** string *_realname* = "";
+ **public** **int** *Rarity*;
+ **public** string *Taste*;
+ **public** **int** *Hungry*;
+ **public** **GameDateTime** *HungryTime*;
+ **public** **int** *Thirsty*;
+ **public** **GameDateTime** *ThirstyTime*;
+ **public** **int** *Appetite*;
+ **public** **int** *Fatigue*;
+ **private** **int** *_mood*;
+ **public** **int** *PeopleState*;
+ **public** **int** *PeopleDrunk*;
+ **public** **GameDateTime** *HurtTime*;
+ **public** **GameDateTime** *CalmTime*;
+ **public** **int** *Identity*;
+ **public** Exp *Experience* = **new** Exp();
+ **public** Exp *HateExperience* = **new** Exp();
+ **public** Exp *LikeExperience* = **new** Exp();
+ **public** **int** *Couple*;
+ **public** **GameDateTime** *CoupleTime*;
+ **public** string *FractionID* = "";
+ **public** Dictionary<string, Equip> *Equip* = **new** Dictionary<string, Equip>();
+ **public** Dictionary<string, PeopleBuff> *PeopleBuff* = **new** Dictionary<string, PeopleBuff>();
+ **public** List<string> *SelfAttitude* = **new** List<string>();
+ **public** Dictionary<**int**, **int**> *PeoplaAttitude* = **new** Dictionary<**int**, **int**>();
+ **public** List<**int**> *RejectedPeople* = **new** List<**int**>();
+ **public** SeedPool *seedPool* = **new** SeedPool();
+ **public** **bool** *IsYou*;
+ **public** PayData *payData* = **new** PayData();