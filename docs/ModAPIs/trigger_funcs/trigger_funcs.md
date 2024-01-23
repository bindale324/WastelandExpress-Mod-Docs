# 简介
在执行某一函数的之前或之后，触发对应的lua函数。

例如，在游戏中，角色每次吃东西之前，都会预先触发`OnEat`函数。

我们可以直接改变这些触发函数，从而在每一次角色/游戏进行某个动作之前，都会有相应的效果发生。



**使用方法**

**只需要在脚本中重新定义这些方法**即可，重定义的方法会嵌入/重载到游戏的函数中。

例如：

```lua
-- main.lua

-- 当吃东西时会触发OnEat函数，people是吃的人，item是吃的东西
function OnEat(people, item)
	--如果吃了ID为1054的物品（火腿）
	if (item.ID == 1054) then
		--print出来的信息可以在游戏右上角日志中查看
		print("吃了火腿，战斗力加10");
		local notFound = true;
		--table里缓存了曾经吃过火腿的人，如果是相同的人吃只刷新时间
		for i, n in pairs(table) do
			if (i.PeopleID == people.PeopleID) then
				notFound = false;
				table[people] = 600;
				break;
			end
		end
		--如果table里面没找到这个人，说明他没吃过火腿或者时间过了，产生效果并记录时间
		if notFound then
			table[people] = 600;
			people._battle = people._battle + effect;
		end
	end
	return false;
end
```



以下是每一个触发函数的详细介绍。

## OnInit

**函数定义**

```lua
function OnInit()
    -- your code here...
end
```



**描述**

在加载脚本的时候触发。

> 虽然直接在脚本最外面写逻辑也可以直接执行，但推荐将加载脚本的初始化内容写在这个函数里，防止出问题。



**参数**

+ NULL



## Update

**函数定义**

```lua
function Update()
    -- your code here...
end
```



**描述**

每帧触发。



**参数**

+ NULL

## OnGUI

**函数定义**

```lua
function OnGUI()
    -- your code here...
end
```



**描述**

用于实现自己的GUI，参考Unity GUI。



**参数**

+ NULL

## OnSave

**函数定义**

```lua
function OnSave(filename)
    -- your code here...
end
```



**描述**

保存存档之前执行。

> 你可以在这里将用`固有函数`-`Save`函数将Mod的数据保存进存档。



**参数**

+ `filename`: string，存档名称

## OnLoad

**函数定义**

```lua
function OnLoad(filename)
    -- your code here...
end
```



**描述**

加载存档之后执行。

加载存档后，先执行`OnLoad`，再执行`OnInit`。

> 1. 如果是新开存档则不会执行`OnLoad`。
> 2. 建议读取数据写在`OnInit`里。



**参数**

+ `filename`: string，存档名称



## OnLog

**函数定义**

```lua
function OnLog(log)
    -- your code here...
end
```



**描述**

当有log打印出来时执行。

也就是说，**当使用Lua的`print`函数后会执行`OnLog`。**



**参数**

+ `log`: string，触发这个函数的所有log字符串



## OnCook

**函数定义**

```lua
function OnCook(ingredients, result)
    -- your code here...
    return false
end
```



**描述**

烹饪之后执行。

> 如果此函数返回true，则会阻止获得物品（菜谱和成就还是会正常获得）。



**参数**

+ `ingredients`: table数组，含有5个元素的数组，代表合成原料的ID
+ `result`: table数组，存放的元素是`Food`，表示烹饪结果。

## OnEat

**函数定义**

```lua
function OnEat(personal, item)
    -- your code here...
    return false
end
```



**描述**

吃东西之前触发。

> 如果此函数返回true，则会阻止之后的行为。



**参数**

+ `personal`: `Personal`类型，吃东西的人
+ `item`: `Item`或`Food`类型，表示吃的东西

## OnDrinkOil

**函数定义**

```lua
function OnDrinkOil(personal, value)
    -- your code here...
    return false
end
```



**描述**

机器人喝汽油时触发。

> 如果此函数返回true，则会阻止之后的行为。



**参数**

+ `personal`: `Personal`类型，喝汽油的人
+ `value`: `int`类型，喝了多少汽油



## OnDrink

**函数定义**

```lua
function OnDrink(personal, item)
    -- your code here...
    return false
end
```



**描述**

喝酒时触发。注意，是喝酒，不是喝水！（喝水请见下一个触发函数）

> 如果此函数返回true，则会阻止之后的行为。



**参数**

+ `personal`: `Personal`类型，喝酒的人
+ `item`: `Item`或`Food`类型，表示喝的酒



## OnDrinkWater

**函数定义**

```lua
function OnDrinkWater(personal)
    -- your code here...
    return false
end
```



**描述**

喝水时触发。

> 如果此函数返回true，则会阻止之后的行为。



**参数**

+ `personal`: `Personal`类型，喝水的人



## OnCure

**函数定义**

```lua
function OnCure(personal，item)
    -- your code here...
    return false
end
```



**描述**

治疗人时触发。

> 如果此函数返回true，则会阻止之后的行为。



**参数**

+ `personal`: `Personal`类型，喝水的人
+ `item`: `Item`类型，用的什么东西治疗



## OnFixPeople

**函数定义**

```lua
function OnFixPeople(personal，value)
    -- your code here...
    return false
end
```



**描述**

修机器人的时候触发。

> 如果此函数返回true，则会阻止之后的行为。



**参数**

+ `personal`: `Personal`类型，喝水的人
+ `value`: `int`类型，修理花了多少零件



## OnOpenUI

**函数定义**

```lua
function OnOpenUI(uiname)
    -- your code here...
    return false
end
```



**描述**

打开UI时触发。

> 如果此函数返回true，则会阻止UI的打开。（警告：有可能会有意想不到的后果）



**参数**

+ `uiname`: `string`，被打开的UI的名字



## OnCloseUI

**函数定义**

```lua
function OnCloseUI(uiname)
    -- your code here...
    return false
end
```



**描述**

关闭UI时触发。

> 如果此函数返回true，则会阻止UI的关闭。（警告：有可能会有意想不到的后果）



**参数**

+ `uiname`: `string`，被关闭的UI的名字

## OnEvent

**函数定义**

```lua
function OnEvent(templateId, force, paramList)
    -- your code here...
end
```



**描述**

触发事件时触发。



**参数**

+ `templateID`: `int`，被触发的事件的ID
+ `force`:`bool`，是否无视触发条件
+ `paramList`: table数组，参数列表