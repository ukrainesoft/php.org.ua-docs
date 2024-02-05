---
navigation:
  - function.ps-open-image-file.md: « ps\_open\_image\_file
  - function.ps-open-memory-image.md: ps\_open\_memory\_image »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_open\_image
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_open\_image

(PECL ps >= 1.1.0)

ps\_open\_image — Зчитує зображення для подальшого розміщення

### Опис

```methodsynopsis
ps_open_image(    resource $psdoc,    string $type,    string $source,    string $data,    int $lenght,    int $width,    int $height,    int $components,    int $bpc,    string $params): int
```

Зчитує зображення, яке вже є у пам'яті. Параметр `source` в даний час не використовується і передбачається, що це `memory`. Дані зображення є послідовністю пікселів, що починається у верхньому лівому куті і закінчується в правому нижньому кутку. Кожен піксель складається з компонентів кольору (`components`) і у кожного компонента є біти `bpc`

### Список параметрів

`psdoc`

Ідентифікатор ресурсу PostScript-файлу, повернутий функцією [ps\_new()](function.ps-new.md)

`type`

Тип зображення. Можливі значення: `png` `jpeg`или`eps`

`source`

Не використовується.

`data`

Дані зображення.

`length`

Довжина даних зображення.

`width`

Ширина зображення.

`height`

Висота зображення.

`components`

Кількість компонентів кожного пікселя. Можливо: 1 (зображення в градаціях сірого), 3 (зображення RGB) або 4 (зображення cmyk, rgba).

`bpc`

Кількість біт на компонент (найчастіше 8).

`params`

### Значення, що повертаються

Повертає ідентифікатор зображення або нуль у разі помилки. Ідентифікатор – позитивне число більше 0.

### Дивіться також

-   [ps\_open\_image\_file()](function.ps-open-image-file.md) \- Відкриває зображення із файлу
-   [ps\_place\_image()](function.ps-place-image.md) \- Розміщує зображення на сторінці
-   [ps\_close\_image()](function.ps-close-image.md) \- Закриває зображення та звільняє пам'ять
