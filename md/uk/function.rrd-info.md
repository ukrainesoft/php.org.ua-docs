Отримує інформацію про файл rrd

-   [« rrd\_graph](function.rrd-graph.html)
    
-   [rrd\_last »](function.rrd-last.html)
    
-   [PHP Manual](index.html)
    
-   [Функции RRD](ref.rrd.html)
    
-   Отримує інформацію про файл rrd
    

# rrdinfo

(PECL rrd >= 0.9.0)

rrdinfo — Отримує інформацію про файл rrd

### Опис

```methodsynopsis
rrd_info(string $filename): array
```

Повертає інформацію про вказаний файл бази даних RRD.

### Список параметрів

`file`

Назва файлу бази даних RRD.

### Значення, що повертаються

Масив, що містить інформацію про вказаний файл RRD або **`false`** у разі виникнення помилки.