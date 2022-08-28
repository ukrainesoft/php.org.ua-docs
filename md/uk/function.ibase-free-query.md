Звільняє пам'ять, виділену для підготовки запиту

-   [« ibase\_free\_event\_handler](function.ibase-free-event-handler.html)
    
-   [ibase\_free\_result »](function.ibase-free-result.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Firebird/InterBase](ref.ibase.html)
    
-   Звільняє пам'ять, виділену для підготовки запиту
    

# ibasefreequery

(PHP 5, PHP 7 < 7.4.0)

ibasefreequery — Звільняє пам'ять, виділену для підготовки запиту

### Опис

```methodsynopsis
ibase_free_query(resource $query): bool
```

Звільняє підготовлений запит.

### Список параметрів

`query`

Запит, підготовлений за допомогою [ibase\_prepare()](function.ibase-prepare.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.