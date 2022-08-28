Отримує ім'я гліфа

-   [« ps\_stroke](function.ps-stroke.html)
    
-   [ps\_symbol\_width »](function.ps-symbol-width.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
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

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.html)

`ord`

Параметр `ord` - це позиція гліфа у векторі кодування шрифту.

`fontid`

Ідентифікатор шрифту. Якщо шрифт не вказано, використовуватиметься поточний шрифт.

### Значення, що повертаються

Ім'я гліфа у заданому шрифті.

### Дивіться також

-   [ps\_symbol()](function.ps-symbol.html) - Виводить гліф
-   [ps\_symbol\_width()](function.ps-symbol-width.html) - Отримує ширину гліфа