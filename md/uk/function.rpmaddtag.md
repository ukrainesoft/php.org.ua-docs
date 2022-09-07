---
navigation:
  - ref.rpminfo.md: « Функції RpmInfo
  - function.rpmdbinfo.md: rpmdbinfo »
  - index.md: PHP Manual
  - ref.rpminfo.md: Функції RpmInfo
title: rpmaddtag
---
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

Одна з констант RPMTAG, перегляньте сторінку [константи rpminfo](rpminfo.constants.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [rpminfo()](function.rpminfo.md) - Витягти інформацію з RPM-файлу
-   [rpmdbinfo()](function.rpmdbinfo.md) - Отримує інформацію від встановленого RPM
-   [rpmdbsearch()](function.rpmdbsearch.md) - Пошук RPM-пакетів
