Знищує сесію

-   [« SessionHandlerInterface::close](sessionhandlerinterface.close.md)
    
-   [SessionHandlerInterface::gc »](sessionhandlerinterface.gc.md)
    
-   [PHP Manual](index.md)
    
-   [SessionHandlerInterface](class.sessionhandlerinterface.md)
    
-   Знищує сесію
    

# SessionHandlerInterface::destroy

(PHP 5> = 5.4.0, PHP 7, PHP 8)

SessionHandlerInterface::destroy — Знищує сесію

### Опис

```methodsynopsis
public SessionHandlerInterface::destroy(string $id): bool
```

Знищує сесію. Викликається функціями [sessionregenerateid()](function.session-regenerate-id.html) (З $destroy = **`true`** [sessiondestroy()](function.session-destroy.html) та при невдалому завершенні функції [sessiondecode()](function.session-decode.html)

### Список параметрів

`id`

Ідентифікатор сесії знищується.

### Значення, що повертаються

Значення сесійного сховища, що повертається (зазвичай **`true`** у разі успішного виконання, **`false`** у разі виникнення помилки). Це значення повертається назад до PHP для внутрішньої обробки.