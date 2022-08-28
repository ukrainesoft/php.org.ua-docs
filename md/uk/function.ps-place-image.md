Розміщує зображення на сторінці

-   [« ps\_open\_memory\_image](function.ps-open-memory-image.html)
    
-   [ps\_rect »](function.ps-rect.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Розміщує зображення на сторінці
    

# псplaceimage

(PECL ps >= 1.1.0)

псplaceimage — Розміщує зображення на сторінці

### Опис

```methodsynopsis
ps_place_image(    resource $psdoc,    int $imageid,    float $x,    float $y,    float $scale): bool
```

Поміщає раніше завантажене зображення на сторінку. Зображення можна масштабувати. Якщо зображення теж необхідно повернути, потрібно буде спочатку повернути систему координат за допомогою [ps\_rotate()](function.ps-rotate.html)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.html)

`imageid`

Ідентифікатор ресурсу зображення, повернутий [ps\_open\_image()](function.ps-open-image.html) або [ps\_open\_image\_file()](function.ps-open-image-file.html)

`x`

Координата X лівого нижнього кута зображення.

`y`

Координата Y лівого нижнього кута зображення.

`scale`

Коефіцієнт масштабування зображення. Масштаб 1.0 дасть роздільну здатність 72 точки на дюйм, тому що кожен піксель еквівалентний 1 точці.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ps\_open\_image()](function.ps-open-image.html) - Зчитує зображення для подальшого розміщення
-   [ps\_open\_image\_file()](function.ps-open-image-file.html) - Відкриває зображення із файлу