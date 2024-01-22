## InitCityPeople

**函数原型**

```csharp
void InitCityPeople();
```

**描述**

初始化城市中的人物。

**参数**

- NULL

**返回值**

- NULL

------

## GetPeopleFromCity

**函数原型**

```csharp
bool GetPeopleFromCity(int PeopleID);
```

**描述**

从城市中获取特定ID的人物。

**参数**

- `PeopleID`: int类型，表示人物ID。

**返回值**

- `bool`: 操作是否成功。

------

## PutPeopleToCity

**函数原型**

```csharp
void PutPeopleToCity(Personal personal, int cityId);
```

**描述**

将特定人物放置到指定城市。

**参数**

- `personal`: Personal类型，表示人物。
- `cityId`: int类型，表示城市ID。

**返回值**

- NULL

------

## PutPeopleToClosetCity

**函数原型**

```csharp
void PutPeopleToClosetCity(Personal personal);
```

**描述**

将特定人物放置到最近的城市。

**参数**

- `personal`: Personal类型，表示人物。

**返回值**

- NULL

------

## PutTypePeopleToCity

**函数原型**

```csharp
void PutTypePeopleToCity(int type, int cityId, int Count, out bool restPeople);
```

**描述**

将特定类型的人物放置到指定城市。

**参数**

- `type`: int类型，表示人物类型。
- `cityId`: int类型，表示城市ID。
- `Count`: int类型，表示数量。
- `restPeople`: out bool类型，输出是否还有剩余人物。

**返回值**

- NULL

------

## GetCityPeopleData

**函数原型**

```csharp
CityPeole GetCityPeopleData(int cityId);
```

**描述**

获取特定城市的人物数据。

**参数**

- `cityId`: int类型，表示城市ID。

**返回值**

- `CityPeole`: 特定城市的人物数据。

------

## GetCityPeopleSeed

**函数原型**

```csharp
CityPeopleSeed GetCityPeopleSeed(int cityId);
```

**描述**

获取特定城市的人物种子数据。

**参数**

- `cityId`: int类型，表示城市ID。

**返回值**

- `CityPeopleSeed`: 特定城市的人物种子数据。

------

## RemovePeopleFromList

**函数原型**

```csharp
void RemovePeopleFromList(int id);
```

**描述**

从列表中移除特定ID的人物。

**参数**

- `id`: int类型，表示人物ID。

**返回值**

- NULL

------

## ArrivedMap

**函数原型**

```csharp
List<int> ArrivedMap();
```

**描述**

获取到达的地图列表。

**参数**

- NULL

**返回值**

- `List<int>`: 到达的地图ID列表。

------

## KnowPeople

**函数原型**

```csharp
bool KnowPeople(float Rate, int Attention);
```

**描述**

根据概率和关注度判断是否认识人物。

**参数**

- `Rate`: float类型，表示认识的概率。
- `Attention`: int类型，表示关注度。

**返回值**

- `bool`: 是否认识人物。

------

## GetCityPeopleDatas

**函数原型**

```csharp
CityPeopleData GetCityPeopleDatas();
```

**描述**

获取城市人物数据。

**参数**

- NULL

**返回值**

- `CityPeopleData`: 城市人物数据。