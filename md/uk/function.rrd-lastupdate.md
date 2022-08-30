Отримує інформацію про останні оновлені дані

-   [« rrdlast](function.rrd-last.html)
    
-   [rrdrestore »](function.rrd-restore.html)
    
-   [PHP Manual](index.md)
    
-   [Функції RRD](ref.rrd.md)
    
-   Отримує інформацію про останні оновлені дані
    

# rrdlastupdate

(PECL rrd >= 0.9.0)

rrdlastupdate — Отримує інформацію про останні оновлені дані

### Опис

```methodsynopsis
rrd_lastupdate(string $filename): array
```

Повертає масив позначки часу UNIX та значення, збережені для кожної дати в останньому оновленні файлу бази даних RRD.

### Список параметрів

`file`

Назва файлу бази даних RRD.

### Значення, що повертаються

Масив інформації про останнє оновлення або **`false`** у разі виникнення помилки.