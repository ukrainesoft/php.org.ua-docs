Повертає позначку часу unix останнього зразка

-   [« rrd\_info](function.rrd-info.html)
    
-   [rrd\_lastupdate »](function.rrd-lastupdate.html)
    
-   [PHP Manual](index.html)
    
-   [Функции RRD](ref.rrd.html)
    
-   Повертає позначку часу unix останнього зразка
    

# rrdlast

(PECL rrd >= 0.9.0)

rrdlast — Повертає позначку часу unix останнього зразка

### Опис

```methodsynopsis
rrd_last(string $filename): int
```

Повертає позначку часу UNIX останнього оновлення бази даних RRD.

### Список параметрів

`filename`

Назва файлу бази даних RRD.

### Значення, що повертаються

Ціле число, що представляє позначку часу unix останніх даних з бази даних RRD.