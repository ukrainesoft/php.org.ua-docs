Знищує сесію

-   [« SessionHandlerInterface::close](sessionhandlerinterface.close.html)
    
-   [SessionHandlerInterface::gc »](sessionhandlerinterface.gc.html)
    
-   [PHP Manual](index.html)
    
-   [SessionHandlerInterface](class.sessionhandlerinterface.html)
    
-   Знищує сесію
    

# SessionHandlerInterface::destroy

(PHP 5> = 5.4.0, PHP 7, PHP 8)

SessionHandlerInterface::destroy — Знищує сесію

### Опис

```methodsynopsis
public SessionHandlerInterface::destroy(string $id): bool
```

Знищує сесію. Викликається функціями [session\_regenerate\_id()](function.session-regenerate-id.html) (З $destroy = **`true`** [session\_destroy()](function.session-destroy.html) та при невдалому завершенні функції [session\_decode()](function.session-decode.html)

### Список параметрів

`id`

Ідентифікатор сесії знищується.

### Значення, що повертаються

Значення сесійного сховища, що повертається (зазвичай **`true`** у разі успішного виконання, **`false`** у разі виникнення помилки). Це значення повертається назад до PHP для внутрішньої обробки.