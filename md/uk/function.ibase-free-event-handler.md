Скасує зареєстрований обробник події

-   [« ibasefieldinfo](function.ibase-field-info.html)
    
-   [ibasefreequery »](function.ibase-free-query.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Firebird/InterBase](ref.ibase.md)
    
-   Скасує зареєстрований обробник події
    

# ibasefreeeventhandler

(PHP 5, PHP 7 < 7.4.0)

ibasefreeeventhandler — скасовує зареєстрований обробник події

### Опис

```methodsynopsis
ibase_free_event_handler(resource $event): bool
```

Функція скасовує, зареєстрований обробник події, зазначений у `event`. Callback-функція більше не буде викликатись для подій, для яких вона була зареєстрована.

### Список параметрів

`event`

Ресурс події, створений [ibaseseteventhandler()](function.ibase-set-event-handler.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ibaseseteventhandler()](function.ibase-set-event-handler.html) - Реєструє callback-функцію, яка буде викликатись при публікації подій