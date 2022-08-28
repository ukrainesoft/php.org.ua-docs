Отримує ширину рядка

-   [« ps\_string\_geometry](function.ps-string-geometry.html)
    
-   [ps\_stroke »](function.ps-stroke.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Отримує ширину рядка
    

# псstringwidth

(PECL ps >= 1.1.0)

псstringwidth — Отримує ширину рядка

### Опис

```methodsynopsis
ps_stringwidth(    resource $psdoc,    string $text,    int $fontid = 0,    float $size = 0.0): float
```

Обчислює ширину рядка в пунктах, якщо вона виводилася із заданим шрифтом і розміром шрифту. Функції потрібен файл метрик шрифтів Adobe для розрахунку точної ширини. Якщо ввімкнено інтервал між літерами, він також буде врахований.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [ps\_new()](function.ps-new.html)

`text`

Текст, котрому потрібно розрахувати ширину.

`fontid`

Ідентифікатор шрифту. Якщо шрифт не вказано, використовується поточний шрифт.

`size`

Розмір шрифту. Якщо розмір не вказано, використовується поточний розмір.

### Значення, що повертаються

Ширина рядка у пунктах.

### Дивіться також

-   [ps\_string\_geometry()](function.ps-string-geometry.html) - Отримує геометрію рядка