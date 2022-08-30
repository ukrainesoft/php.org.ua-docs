Додає тег, отриманий у запиті

-   [« Функції RpmInfo](ref.rpminfo.html)
    
-   [rpmdbinfo »](function.rpmdbinfo.html)
    
-   [PHP Manual](index.html)
    
-   [Функції RpmInfo](ref.rpminfo.html)
    
-   Додає тег, отриманий у запиті
    

# rpmaddtag

(PECL rpminfo >= 0.5.0)

rpmaddtag ​​— Додає тег, отриманий у запиті

### Опис

```methodsynopsis
rpmaddtag(int $tag): bool
```

Додає додатковий витягнутий тег у наступних запитах.

### Список параметрів

`tag`

Одна з констант RPMTAG, перегляньте сторінку [константы rpminfo](rpminfo.constants.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [rpminfo()](function.rpminfo.html) - Витягти інформацію з RPM-файлу
-   [rpmdbinfo()](function.rpmdbinfo.html) - Отримує інформацію від встановленого RPM
-   [rpmdbsearch()](function.rpmdbsearch.html) - Пошук RPM-пакетів