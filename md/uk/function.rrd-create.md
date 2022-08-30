Створити файл rrd

-   [« Функції RRD](ref.rrd.html)
    
-   [rrderror »](function.rrd-error.html)
    
-   [PHP Manual](index.html)
    
-   [Функції RRD](ref.rrd.html)
    
-   Створити файл rrd
    

# rrdcreate

(PECL rrd >= 0.9.0)

rrdcreate — Створити файл rrd

### Опис

```methodsynopsis
rrd_create(string $filename, array $options): bool
```

Створює файл rrd.

### Список параметрів

`filename`

Ім'я файлу, що створюється.

`options`

Опції для створення rrd – список рядків. Дивіться сторінку посібника rrd для повного списку.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.