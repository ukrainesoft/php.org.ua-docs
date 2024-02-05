---
navigation:
  - function.ps-open-memory-image.md: « ps\_open\_memory\_image
  - function.ps-rect.md: ps\_rect »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_place\_image
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_place\_image

(PECL ps >= 1.1.0)

ps\_place\_image — Розміщує зображення на сторінці

### Опис

```methodsynopsis
ps_place_image(    resource $psdoc,    int $imageid,    float $x,    float $y,    float $scale): bool
```

Поміщає раніше завантажене зображення на сторінку. Зображення можна масштабувати. Якщо зображення також необхідно повернути, потрібно буде спочатку повернути систему координат за допомогою [ps\_rotate()](function.ps-rotate.md)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

`imageid`

Ідентифікатор ресурсу зображення, повернутий [ps\_open\_image()](function.ps-open-image.md) або [ps\_open\_image\_file()](function.ps-open-image-file.md)

`x`

Координата X лівого нижнього кута зображення.

`y`

Координата Y лівого нижнього кута зображення.

`scale`

Коефіцієнт масштабування зображення. Масштаб 1.0 дасть роздільну здатність 72 точки на дюйм, тому що кожен піксель еквівалентний 1 точці.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_open\_image()](function.ps-open-image.md) \- Зчитує зображення для подальшого розміщення
-   [ps\_open\_image\_file()](function.ps-open-image-file.md) \- Відкриває зображення із файлу
