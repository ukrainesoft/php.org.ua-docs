---
navigation:
  - function.ps-open-memory-image.md: «psopenmemoryimage
  - function.ps-rect.md: псrect »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псplaceimage
---
# псplaceimage

(PECL ps >= 1.1.0)

псplaceimage — Розміщує зображення на сторінці

### Опис

```methodsynopsis
ps_place_image(    resource $psdoc,    int $imageid,    float $x,    float $y,    float $scale): bool
```

Поміщає раніше завантажене зображення на сторінку. Зображення можна масштабувати. Якщо зображення теж необхідно повернути, потрібно буде спочатку повернути систему координат за допомогою [псrotate()](function.ps-rotate.md)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.md)

`imageid`

Ідентифікатор ресурсу зображення, повернутий [псopenimage()](function.ps-open-image.md) або [псopenimagefile()](function.ps-open-image-file.md)

`x`

Координата X лівого нижнього кута зображення.

`y`

Координата Y лівого нижнього кута зображення.

`scale`

Коефіцієнт масштабування зображення. Масштаб 1.0 дасть роздільну здатність 72 точки на дюйм, тому що кожен піксель еквівалентний 1 точці.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псopenimage()](function.ps-open-image.md) - Зчитує зображення для подальшого розміщення
-   [псopenimagefile()](function.ps-open-image-file.md) - Відкриває зображення із файлу
