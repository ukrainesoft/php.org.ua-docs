Повертає позначку першого зразка з файлу rrd

-   [« rrd\_fetch](function.rrd-fetch.html)
    
-   [rrd\_graph »](function.rrd-graph.html)
    
-   [PHP Manual](index.html)
    
-   [Функции RRD](ref.rrd.html)
    
-   Повертає позначку першого зразка з файлу rrd
    

# rrdfirst

(PECL rrd >= 0.9.0)

rrdfirst — Повертає позначку першого зразка з файлу rrd

### Опис

```methodsynopsis
rrd_first(string $file, int $raaindex = 0): int
```

Повертає перший зразок даних із вказаного RRA файлу RRD.

### Список параметрів

`file`

Назва файлу бази даних RRD.

`raaindex`

Номер індексу RRA, який має бути розглянутий. Значення за промовчанням - 0.

### Значення, що повертаються

Номер позначки часу unix у вигляді цілого чи числа **`false`** у разі виникнення помилки.