Ініціалізує сесію

-   [« SessionHandlerInterface::gc](sessionhandlerinterface.gc.md)
    
-   [SessionHandlerInterface::read »](sessionhandlerinterface.read.md)
    
-   [PHP Manual](index.md)
    
-   [SessionHandlerInterface](class.sessionhandlerinterface.md)
    
-   Ініціалізує сесію
    

# SessionHandlerInterface::open

(PHP 5> = 5.4.0, PHP 7, PHP 8)

SessionHandlerInterface::open — Ініціалізує сесію

### Опис

```methodsynopsis
public SessionHandlerInterface::open(string $path, string $name): bool
```

Повторно ініціалізує існуючу сесію чи створює нову. Викликається коли сесія стартує або коли викликана функція [sessionstart()](function.session-start.html)

### Список параметрів

`path`

Шлях, яким зберігається/відновлюється сесія.

`name`

Назва сесії.

### Значення, що повертаються

Значення сесійного сховища, що повертається (зазвичай **`true`** у разі успішного виконання, **`false`** у разі виникнення помилки). Це значення повертається назад до PHP для внутрішньої обробки.

### Дивіться також

-   [sessionname()](function.session-name.html) - Отримати чи встановити ім'я поточної сесії
-   Опція конфігурації [session.auto-start](session.configuration.html#ini.session.auto-start)