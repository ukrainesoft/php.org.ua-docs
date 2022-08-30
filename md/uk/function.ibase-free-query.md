Звільняє пам'ять, виділену для підготовки запиту

-   [« ibasefreeeventhandler](function.ibase-free-event-handler.html)
    
-   [ibasefreeresult »](function.ibase-free-result.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Firebird/InterBase](ref.ibase.md)
    
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

Запит, підготовлений за допомогою [ibaseprepare()](function.ibase-prepare.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.