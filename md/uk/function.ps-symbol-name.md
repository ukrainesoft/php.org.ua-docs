Отримує ім'я гліфа

-   [«psstroke](function.ps-stroke.html)
    
-   [псsymbolwidth »](function.ps-symbol-width.html)
    
-   [PHP Manual](index.md)
    
-   [Функції PS](ref.ps.md)
    
-   Отримує ім'я гліфа
    

# псsymbolname

(PECL ps >= 1.2.0)

псsymbolname — Отримує ім'я гліфа

### Опис

```methodsynopsis
ps_symbol_name(resource $psdoc, int $ord, int $fontid = 0): string
```

Для функції необхідний файл метрик шрифтів Adobe, щоб знати, які гліфи доступні.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.html)

`ord`

Параметр `ord` - це позиція гліфа у векторі кодування шрифту.

`fontid`

Ідентифікатор шрифту. Якщо шрифт не вказано, використовуватиметься поточний шрифт.

### Значення, що повертаються

Ім'я гліфа у заданому шрифті.

### Дивіться також

-   [псsymbol()](function.ps-symbol.html) - Виводить гліф
-   [псsymbolwidth()](function.ps-symbol-width.html) - Отримує ширину гліфа