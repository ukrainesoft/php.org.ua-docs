Скасує зареєстрований обробник події

-   [« ibase\_field\_info](function.ibase-field-info.html)
    
-   [ibase\_free\_query »](function.ibase-free-query.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Firebird/InterBase](ref.ibase.html)
    
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

Ресурс події, створений [ibase\_set\_event\_handler()](function.ibase-set-event-handler.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ibase\_set\_event\_handler()](function.ibase-set-event-handler.html) - Реєструє callback-функцію, яка буде викликатись при публікації подій