Ініціалізує сесію

-   [« SessionHandler::gc](sessionhandler.gc.md)
    
-   [SessionHandler::read »](sessionhandler.read.md)
    
-   [PHP Manual](index.md)
    
-   [SessionHandler](class.sessionhandler.md)
    
-   Ініціалізує сесію
    

# SessionHandler::open

(PHP 5> = 5.4.0, PHP 7, PHP 8)

SessionHandler::open — Ініціалізує сесію

### Опис

```methodsynopsis
public SessionHandler::open(string $path, string $name): bool
```

Створює нову сесію чи повторно ініціалізує існуючу. Викликається зсередини PHP, коли сесія стартує автоматично або за допомогою виклику функції [sessionstart()](function.session-start.html)

Цей метод є обгорткою для внутрішнього обробника PHP, визначеного в налаштуванні ini-файлу [session.savehandler](session.configuration.html#ini.session.save-handler), який встановлюється до визначення обробника викликом функції [sessionsetsavehandler()](function.session-set-save-handler.html)

Якщо цей клас розширюється шляхом успадкування, виклик батьківського методу `open` виконає код обгортки для цього методу, а також внутрішній обробник. Це дозволить методу бути перевизначеним, або перехопленим та відфільтрованим.

Для додаткової інформації про те, що очікується від реалізації цього методу, дивіться документацію за методом [SessionHandlerInterface::open()](sessionhandlerinterface.open.md)

### Список параметрів

`path`

Шлях яким зберігається/відновлюється сесія.

`name`

Назва сесії.

### Значення, що повертаються

Значення сесійного сховища, що повертається (зазвичай **`true`** у разі успішного виконання, **`false`** у разі виникнення помилки). Це значення повертається назад до PHP для внутрішньої обробки.

### Дивіться також

-   Опція конфігурації [session.auto-start](session.configuration.html#ini.session.auto-start)