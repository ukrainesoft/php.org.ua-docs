Зчитує дані сесії

-   [« SessionHandler::open](sessionhandler.open.html)
    
-   [SessionHandler::write »](sessionhandler.write.html)
    
-   [PHP Manual](index.html)
    
-   [SessionHandler](class.sessionhandler.html)
    
-   Зчитує дані сесії
    

# SessionHandler::read

(PHP 5> = 5.4.0, PHP 7, PHP 8)

SessionHandler::read — Зчитує дані сесії

### Опис

```methodsynopsis
public SessionHandler::read(string $id): string|false
```

Зчитує дані сесії зі сховища та повертає результат назад у PHP для внутрішньої обробки. Цей метод викликається автоматично, коли PHP стартує сесію (або автоматично або безпосередньо викликом. [sessionstart()](function.session-start.html) з наступним викликом [SessionHandler::open()](sessionhandler.open.html)

Цей метод є обертанням внутрішнього обробника PHP, визначеного в параметрі ini-файлу [session.savehandler](session.configuration.html#ini.session.save-handler) який встановлюється до того, як буде визначено оброблювач сесії викликом [sessionsetsavehandler()](function.session-set-save-handler.html)

Якщо цей клас розширено шляхом успадкування, виклик батьківського методу `read` викликає обгортку для цього методу і, відповідно, виклик внутрішнього оброблювача. Це дозволяє методу бути перевантаженим, та/або перехопленим та відфільтрованим (наприклад для розшифровки, значення параметра `$data`, що повертає батьківський метод `read`

Для додаткової інформації дивіться документацію за методом [SessionHandlerInterface::read()](sessionhandlerinterface.read.html)

### Список параметрів

`id`

Ідентифікатор сесії, з якої необхідно рахувати дані.

### Значення, що повертаються

Повертає зашифрований рядок лічених даних. Якщо нічого не раховано, повертається **`false`**. Зверніть увагу, що це значення повертається до PHP для внутрішньої обробки.

### Дивіться також

-   Директива налаштування [session.serializehandler](session.configuration.html#ini.session.serialize-handler)