Повертають статус повідомлення про помилку, системний та/або zip-статус

-   [« ZipArchive::getNameIndex](ziparchive.getnameindex.html)
    
-   [ZipArchive::getStream »](ziparchive.getstream.html)
    
-   [PHP Manual](index.html)
    
-   [ZipArchive](class.ziparchive.html)
    
-   Повертають статус повідомлення про помилку, системний та/або zip-статус
    

# ZipArchive::getStatusString

(PHP 5> = 5.2.7, PHP 7, PHP 8)

ZipArchive::getStatusString — Повертають статус повідомлення про помилку, системний та/або zip-статус

### Опис

```methodsynopsis
public ZipArchive::getStatusString(): string
```

Повертають статус повідомлення про помилку, системний та/або zip-статус.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рядок (string) із повідомленням про статус.

### список змін

| Версия | Описание                                                        |
|--------|-----------------------------------------------------------------|
|        | Метод можна викликати у закритому архіві.                       |
|        | Метод більше не повертає **`false`** у разі виникнення помилки. |