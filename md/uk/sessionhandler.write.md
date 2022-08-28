Записує дані сесії

-   [« SessionHandler::read](sessionhandler.read.html)
    
-   [SessionHandlerInterface »](class.sessionhandlerinterface.html)
    
-   [PHP Manual](index.html)
    
-   [SessionHandler](class.sessionhandler.html)
    
-   Записує дані сесії
    

# SessionHandler::write

(PHP 5> = 5.4.0, PHP 7, PHP 8)

SessionHandler::write — Записує дані сесії

### Опис

```methodsynopsis
public SessionHandler::write(string $id, string $data): bool
```

Записує дані сесії у сховище. Зазвичай викликається при завершенні скрипту, функцією [session\_write\_close()](function.session-write-close.html) або коли [session\_register\_shutdown()](function.session-register-shutdown.html) зазнає невдачі. PHP викликає [SessionHandler::close()](sessionhandler.close.html) відразу після цього методу.

Метод є обертанням внутрішнього обробника PHP, визначеного в параметрі ini-файлу [session.save\_handler](session.configuration.html#ini.session.save-handler) який встановлюється до того, як буде визначено оброблювач сесії викликом [session\_set\_save\_handler()](function.session-set-save-handler.html)

Якщо цей клас розширено шляхом успадкування, виклик батьківського методу `write` викликає обгортку для цього методу і, відповідно, виклик внутрішнього оброблювача. Це дозволяє методу бути перевантаженим або перехопленим та відфільтрованим (наприклад, для шифрування значення параметра `$data` перед відправкою його в батьківський метод `write`

Для додаткової інформації дивіться документацію за методом [SessionHandlerInterface::write()](sessionhandlerinterface.write.html)

### Список параметрів

`id`

Ідентифікатор сесії

`data`

Зашифровані дані сесії. Ці дані є результатом того, що PHP внутрішньо шифрує суперглобальну змінну. [$\_SESSION](reserved.variables.session.html) в серіалізований рядок і передає його як параметр. Зауважте, що сесії використовують альтернативний метод серіалізації.

### Значення, що повертаються

Значення сесійного сховища, що повертається (зазвичай **`true`** у разі успішного виконання, **`false`** у разі виникнення помилки). Це значення повертається назад до PHP для внутрішньої обробки.

### Дивіться також

-   Директива конфігурації [session.serialize\_handler](session.configuration.html#ini.session.serialize-handler)