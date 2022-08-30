Експортує інформацію про базу даних RRD

-   [« rrdversion](function.rrd-version.html)
    
-   [rrdcdisconnect »](function.rrdc-disconnect.html)
    
-   [PHP Manual](index.html)
    
-   [Функції RRD](ref.rrd.html)
    
-   Експортує інформацію про базу даних RRD
    

# rrdxport

(PECL rrd >= 0.9.0)

rrdxport — Експортує інформацію про базу даних RRD

### Опис

```methodsynopsis
rrd_xport(array $options): array
```

Експортує інформацію про файл бази даних RRD. Дані можуть бути перетворені в XML-файл за допомогою PHP-скрипта користувача, а потім відновлені у вигляді файлу бази даних RRD.

### Список параметрів

`options`

Масив опцій для експорту дивіться сторінку посібника з rrd xport.

### Значення, що повертаються

Масив з інформацією про файл бази даних RRD або **`false`** у разі виникнення помилки.