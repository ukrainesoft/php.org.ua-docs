---
navigation:
  - function.ps-open-image-file.md: «psopenimagefile
  - function.ps-open-memory-image.md: псopenmemoryimage »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псopenimage
---
# псopenimage

(PECL ps >= 1.1.0)

псopenimage — Зчитує зображення для подальшого розміщення

### Опис

```methodsynopsis
ps_open_image(    resource $psdoc,    string $type,    string $source,    string $data,    int $lenght,    int $width,    int $height,    int $components,    int $bpc,    string $params): int
```

Зчитує зображення, яке вже є у пам'яті. Параметр `source` в даний час не використовується і передбачається, що це `memory`. Дані зображення є послідовністю пікселів, що починається у верхньому лівому куті і закінчується в правому нижньому кутку. Кожен піксель складається з компонентів кольору (`components`) і у кожного компонента є біти `bpc`

### Список параметрів

`psdoc`

Ідентифікатор ресурсу PostScript-файлу, повернутий функцією [псnew()](function.ps-new.md)

`type`

Тип зображення. Можливі значення: `png` `jpeg` або `eps`

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

-   [псopenimagefile()](function.ps-open-image-file.md) - Відкриває зображення із файлу
-   [псplaceimage()](function.ps-place-image.md) - Розміщує зображення на сторінці
-   [псcloseimage()](function.ps-close-image.md) - Закриває зображення та звільняє пам'ять
