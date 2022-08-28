Встановлює користувальницькі обробники зберігання сесії

-   [« session\_set\_cookie\_params](function.session-set-cookie-params.html)
    
-   [session\_start »](function.session-start.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с сессиями](ref.session.html)
    
-   Встановлює користувальницькі обробники зберігання сесії
    

# sessionsetsavehandler

(PHP 4, PHP 5, PHP 7, PHP 8)

sessionsetsavehandler - Встановлює користувальницькі обробники зберігання сесії

### Опис

```methodsynopsis
session_set_save_handler(    callable $open,    callable $close,    callable $read,    callable $write,    callable $destroy,    callable $gc,    callable $create_sid = ?,    callable $validate_sid = ?,    callable $update_timestamp = ?): bool
```

Також можна зареєструвати наступний прототип:

```methodsynopsis
session_set_save_handler(object $sessionhandler, bool $register_shutdown = true): bool
```

**sessionsetsavehandler()** встановлює користувальницькі обробники зберігання сесії, які використовуються для збереження та отримання даних, пов'язаних із сесією. Це особливо корисно, коли доцільним є метод зберігання, відмінний від тих, які надаються сесіями PHP, наприклад, зберігання даних сесії в локальній базі даних.

### Список параметрів

Ця функція має два визначення (прототипу).

`sessionhandler`

Примірник класу, що реалізує інтерфейс [SessionHandlerInterface](class.sessionhandlerinterface.html) та необов'язкові [SessionIdInterface](class.sessionidinterface.html) та/або [SessionUpdateTimestampHandlerInterface](class.sessionupdatetimestamphandlerinterface.html), такий як [SessionHandler](class.sessionhandler.html), Для реєстрації як оброблювач сесії.

`register_shutdown`

Зареєструвати [session\_write\_close()](function.session-write-close.html) як функцію [register\_shutdown\_function()](function.register-shutdown-function.html)

або

`open`

Callback-функція з наступною сигнатурою:

```methodsynopsis
open(string $savePath, string $sessionName): bool
```

Callback-функція `open` працює як конструктор у класах та виконується при відкритті сесії. Це перша callback-функція, яка виконується, коли сесія стартує автоматично або вручну через [session\_start()](function.session-start.html). Значення, що повертається **`true`** у разі успішного виконання, **`false`** у разі невдачі.

`close`

Callback-функція з наступною сигнатурою:

```methodsynopsis
close(): bool
```

Callback-функція `close` працює як деструктор у класах і виконується після того, як була викликана callback-функція `write`. Вона також викликається під час виклику [session\_write\_close()](function.session-write-close.html). Значення, що повертається, має бути **`true`** у разі успішного виконання, **`false`** у разі невдачі.

`read`

Callback-функція з наступною сигнатурою:

```methodsynopsis
read(string $sessionId): string
```

Callback-функція `read` повинна завжди повертати кодований (серіалізований) рядок сесії або порожній рядок, якщо немає даних для читання.

Ця callback-функція викликається внутрішнім механізмом PHP при старті сесії або виклику [session\_start()](function.session-start.html). Перед тим, як буде викликана ця callback-функція, PHP викличе callback-функцію `open`

Значення, що повертається даної callback-функції повинно бути в такому ж серіалізованому форматі, який спочатку передавався для зберігання в callback-функцію `write`. Значення, що повертається, буде автоматично десеріалізовано PHP і використано для заповнення суперглобальної змінної [$\_SESSION](reserved.variables.session.html). Навіть якщо дані схожі на результат [serialize()](function.serialize.html), варто пам'ятати, що це інший формат серіалізації, який визначений ini-директивою [session.serialize\_handler](session.configuration.html#ini.session.serialize-handler)

`write`

Callback-функція з наступною сигнатурою:

```methodsynopsis
write(string $sessionId, string $data): bool
```

Callback-функція `write` викликається, коли сесія має бути збережена та закрита. Ця callback-функція приймає ідентифікатор поточної сесії та серіалізовану версію суперглобальної змінної [$\_SESSION](reserved.variables.session.html). Метод серіалізації, що використовується всередині PHP, визначений ini-директивою. [session.serialize\_handler](session.configuration.html#ini.session.serialize-handler)

Передані у цю callback-функцію серіалізовані дані сесії мають бути збережені у зв'язку з переданим ідентифікатором сесії. При отриманні цих даних, callback-функція `read` повинна повернути те саме значення, що було передано в callback-функцію `write`

Ця callback-функція викликається, коли PHP завершує роботу або явно під час виклику [session\_write\_close()](function.session-write-close.html). Слід пам'ятати, що після виконання цієї callback-функції PHP виконає callback-функцію `close`

> **Зауваження**
> 
> Обробник "write" не виконається доти, доки вихідний потік не буде закрито. Таким чином, виведення налагоджувальних операторів в обробнику "write" ніколи не відобразиться у браузері. Якщо потрібно вивести налагоджувальну інформацію, рекомендується записувати налагоджувальні дані у файл.

`destroy`

Callback-функція з наступною сигнатурою:

```methodsynopsis
destroy(string $sessionId): bool
```

Ця callback-функція викликається, коли сесія знищується за допомогою [session\_destroy()](function.session-destroy.html) або під час виклику [session\_regenerate\_id()](function.session-regenerate-id.html) з параметром destroy, встановленим у **`true`**. Значення, що повертається, має бути **`true`** у разі успішного виконання, **`false`** у разі невдачі.

`gc`

Callback-функція з наступною сигнатурою:

```methodsynopsis
gc(int $lifetime): bool
```

Callback-функція збирача сміття періодично викликається PHP для очищення даних старих сесій. Частота контролюється директивами [session.gc\_probability](session.configuration.html#ini.session.gc-probability) і [session.gc\_divisor](session.configuration.html#ini.session.gc-divisor). Значення lifetime, яке передається в дану callback-функцію, може бути встановлено в [session.gc\_maxlifetime](session.configuration.html#ini.session.gc-maxlifetime). Значення, що повертається, має бути **`true`** у разі успішного виконання, **`false`** у разі невдачі.

`create_sid`

Callback-функція з наступною сигнатурою:

```methodsynopsis
create_sid(): string
```

Ця callback-функція виконується, коли потрібний новий ідентифікатор сесії. Не передбачає параметрів, а значення, що повертається, має бути рядком, який є допустимим ідентифікатором сесії для вашого оброблювача.

`validate_sid`

Callback-функція з наступною сигнатурою:

```methodsynopsis
validate_sid(string $key): bool
```

Callback-функція виконується, коли має бути запущена сесія, надається ідентифікатор сесії та вмикається [session.use\_strict\_mode](session.configuration.html#ini.session.use-strict-mode). . `key` – це ідентифікатор сесії для перевірки. Ідентифікатор сесії є дійсним, якщо сесія з таким ідентифікатором вже існує. Значення, що повертається, має бути **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

`update_timestamp`

Callback-функція з наступною сигнатурою:

```methodsynopsis
update_timestamp(string $key, string $val): bool
```

Callback-функція виконується під час сесії . `key` - це ідентифікатор сесії, `val` - Це дані сесії. Значення, що повертається, має бути **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Користувальницький обробник сесії: повний код дивіться в описі [SessionHandlerInterface](class.sessionhandlerinterface.html)**

Тут лише продемонстровано виклик sessionsetsavehandler, повний приклад можна подивитися в описі [SessionHandlerInterface](class.sessionhandlerinterface.html)

Зауважте, що з **sessionsetsavehandler()** ми використовуємо ООП-прототип і реєструємо функцію завершення, використовуючи прапорець параметра функції. Це зазвичай рекомендується під час реєстрації об'єктів як оброблювачів зберігання сесії.

```php
<?php
class MySessionHandler implements SessionHandlerInterface
{
    // здесь реализация интерфейса
}

$handler = new MySessionHandler();
session_set_save_handler($handler, true);
session_start();

// устанавливаем и получаем значения по ключу из $_SESSION
```

### Примітки

**Увага**

Оброблювачі `write` і `close` викликаються після деструктора об'єкта і тому можуть використовувати його контекст чи кидати винятки. Винятки не можуть бути оброблені, тому що не будуть спіймані, не буде відображено трасування стека виключення і виконання просто припиниться несподівано. Однак при цьому деструктори об'єкта можуть використовувати сесії.

Можна викликати [session\_write\_close()](function.session-write-close.html) з деструктора, щоб вирішити цю проблему "курки та яйця", але найнадійніший спосіб - це реєструвати функцію завершення, як описано вище.

**Увага**

Поточний робочий каталог змінюється деякими SAPI, якщо сесія закривається після завершення скрипта. Завершити сесію можна раніше за допомогою [session\_write\_close()](function.session-write-close.html)

### Дивіться також

-   Директива [session.save\_handler](session.configuration.html#ini.session.save-handler)
-   Директива [session.serialize\_handler](session.configuration.html#ini.session.serialize-handler)
-   [register\_shutdown\_function()](function.register-shutdown-function.html) - Реєструє функцію, яка виконається після завершення роботи скрипту
-   [session\_register\_shutdown()](function.session-register-shutdown.html) - функція завершення сесії
-   Зверніться до [» save\_handler.inc](https://github.com/php/php-src/blob/master/ext/session/tests/save_handler.inc) для повного набору рекомендацій щодо реалізації