Отримує ширину гліфа

-   [«pssymbolname](function.ps-symbol-name.html)
    
-   [псsymbol »](function.ps-symbol.html)
    
-   [PHP Manual](index.html)
    
-   [Функції PS](ref.ps.html)
    
-   Отримує ширину гліфа
    

# псsymbolwidth

(PECL ps >= 1.2.0)

псsymbolwidth — Отримує ширину гліфа

### Опис

```methodsynopsis
ps_symbol_width(    resource $psdoc,    int $ord,    int $fontid = 0,    float $size = 0.0): float
```

Обчислює ширину гліфа в точках, якщо він був виведений із заданим шрифтом та розміром шрифту. Функції потрібен файл метрик шрифтів Adobe для розрахунку точної ширини.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.html)

`ord`

Положення гліфа у векторному шрифт кодування.

`fontid`

Ідентифікатор шрифту. Якщо шрифт не вказано, використовуватиметься поточний шрифт.

`size`

Розмір шрифту. Якщо розмір не вказано, використовується поточний розмір.

### Значення, що повертаються

Ширина гліфа у точках.

### Дивіться також

-   [псsymbol()](function.ps-symbol.html) - Виводить гліф
-   [псsymbolname()](function.ps-symbol-name.html) - Отримує ім'я гліфа