# InventorySystem

### Функции у Inventory.cs

```C#
// Ивенты
Inventory.OnChangeItems(); // Вызывается когда меняется кол-во предметов
Inventory.OnClickCell(ItemCell); // Вызывается при нажатии на ячейку (Не вызывается когда происходит Drag)
Inventory.OnEnterCell(ItemCell); // Вызывается когда навели на ячейку

// Функции 
Inventory.RemoveItem(Item targetItem, int count = 1, bool useMetaData = true) return bool; // Удалить предмет
Inventory.AddItem(Item targetItem, int count = 1); // Добавить предмет в инвентарь
Inventory.Clear(); // Очистить инвентарь
Inventory.GetNullCell() return ItemCell; // Найти свободную ячейку
Inventory.FindItems(Item targetItem, bool useMetaData = true) return List<ItemCell>; // Найти определенный предмет
Inventory.GetCountItem(Item targetItem) return int; // Получить кол-во определенных предметов
Inventory.GetAllItems() return List<ItemCell>; // Получить все предметы которые лежат в инвенторе
Inventory.GetSizeGrid() return Vector2Int; // Получить размер сетки
Inventory.GetSizeCell() return float; // Вернет размер ячейки
Inventory.MetadataComparison(Item oneMetaData, Item twoMetaData) return bool; // Проверка на совместимость мета данных

// Перемещение
Inventory.ItemDragCount(ItemCell fromCell, ItemCell whereCell, int count = 1); // Перемещает определенное кол-во предметов за раз
Inventory.ItemDragSplitter(ItemCell fromCell, ItemCell whereCell, float splitter = 1); // Перемещает разделенный предмет
```

### Функции у Item.cs
```C#
Item.SetMetaData(string key, string value); // Установить мета данные
Item.GetMetaData(string key) return string; // Получить мета данные
Item.HasMetaData(string key) return bool; // Проверить существует ли мета данная под данным ключем
Item.GetMetaDatas() return Dictionary<string, string>; // Получить весь список мета данных предмета
Item.SetMetaDatas(Dictionary<string, string> metaData); // Установить список мета данных
Item.DeleteMetaData(string key); // Удалить мета данные
```

### Функции у ItemCell.cs

```C#
ItemCell.SetCount(int count = 1); // Установить кол-во предметов
ItemCell.SetItem(Item targetItem, int count = 1); // Установить предмет и кол-во
ItemCell.SetBlock(bool flag); // Заблокировать/разблокировать ячейку
ItemCell.DeleteItem(); // Удалить предмет
ItemCell.ReloadVisual(); // Обновить отоброжение
```
