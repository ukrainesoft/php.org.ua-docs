Оновлює базу даних RRD

-   [« rrdtune](function.rrd-tune.html)
    
-   [rrdversion »](function.rrd-version.html)
    
-   [PHP Manual](index.md)
    
-   [Функції RRD](ref.rrd.md)
    
-   Оновлює базу даних RRD
    

# rrdupdate

(PECL rrd >= 0.9.0)

rrdupdate — Оновлює базу даних RRD

### Опис

```methodsynopsis
rrd_update(string $filename, array $options): bool
```

Оновлює файл бази даних RRD. Вхідні дані - це час, інтерполіроване відповідно до властивостей файлу бази даних RRD.

### Список параметрів

`filename`

Назва файлу бази даних RRD. Ця база даних буде оновлена.

`options`

Опції поновлення бази даних RRD. Це перелік рядків. Повний список опцій дивіться на сторінці посібника з rrd update для отримання повного списку опцій.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.