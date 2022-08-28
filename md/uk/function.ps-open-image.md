Зчитує зображення для подальшого розміщення

-   [« ps\_open\_image\_file](function.ps-open-image-file.html)
    
-   [ps\_open\_memory\_image »](function.ps-open-memory-image.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Зчитує зображення для подальшого розміщення
    

# псopenimage

(PECL ps >= 1.1.0)

псopenimage — Зчитує зображення для подальшого розміщення

### Опис

```methodsynopsis
ps_open_image(    resource $psdoc,    string $type,    string $source,    string $data,    int $lenght,    int $width,    int $height,    int $components,    int $bpc,    string $params): int
```

Зчитує зображення, яке вже є у пам'яті. Параметр `source` в даний час не використовується і передбачається, що це `memory`. Дані зображення є послідовністю пікселів, що починається у верхньому лівому куті і закінчується в правому нижньому кутку. Кожен піксель складається з компонентів кольору (`components`) і у кожного компонента є біти `bpc`

### Список параметрів

`psdoc`

Ідентифікатор ресурсу PostScript-файлу, повернутий функцією [ps\_new()](function.ps-new.html)

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

-   [ps\_open\_image\_file()](function.ps-open-image-file.html) - Відкриває зображення із файлу
-   [ps\_place\_image()](function.ps-place-image.html) - Розміщує зображення на сторінці
-   [ps\_close\_image()](function.ps-close-image.html) - Закриває зображення та звільняє пам'ять