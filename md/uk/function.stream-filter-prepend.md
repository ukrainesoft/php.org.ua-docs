Прикріплює фільтр до потоку

-   [« stream\_filter\_append](function.stream-filter-append.html)
    
-   [stream\_filter\_register »](function.stream-filter-register.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с потоками](ref.stream.html)
    
-   Прикріплює фільтр до потоку
    

# streamfilterprepend

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

streamfilterprepend — Прикріплює фільтр до потоку

### Опис

```methodsynopsis
stream_filter_prepend(    resource $stream,    string $filtername,    int $read_write = ?,    mixed $params = ?): resource
```

Додає `filtername` до списку фільтрів, прикріплених до стелі `stream`

### Список параметрів

`stream`

Цільовий потік.

`filtername`

Назва потоку.

`read_write`

За замовчуванням функція **streamfilterprepend()** буде прикріплювати фільтр до `цепочке фильтров чтения`, якщо файл був відкритий для читання (тобто режим файлу: `r`, та/або `+`). Фільтр також буде прикріплений до `цепочке фильтров записи`, якщо файл був відкритий для запису (тобто режим файлу: `w` `a`, та/або `+`). Константи **`STREAM_FILTER_READ`** **`STREAM_FILTER_WRITE`** та/або **`STREAM_FILTER_ALL`** також можуть бути передані у параметрі `read_write`, щоб перевизначити цю поведінку. Дивіться функцію [stream\_filter\_append()](function.stream-filter-append.html) для використання цього параметра.

`params`

Цей фільтр буде додано із зазначеними параметрами `params` до *початку* списку і, таким чином, буде викликано першим під час потокових операцій. Щоб додати фільтр до кінця списку, використовуйте [stream\_filter\_append()](function.stream-filter-append.html)

### Значення, що повертаються

Повертає ресурс у разі успішного виконання або **`false`** у разі виникнення помилки. Ресурс повинен бути використаний для посилання на цей екземпляр фільтра під час виклику [stream\_filter\_remove()](function.stream-filter-remove.html)

Поверне **`false`**, якщо `stream` не є ресурсом або якщо `filtername` НЕ знайдений.

### Примітки

> **Зауваження** **При використанні фільтрів користувача**  
> Спочатку має бути викликана функція [stream\_filter\_register()](function.stream-filter-register.html) для того, щоб зареєструвати бажаний фільтр користувача на ім'я `filtername`

> **Зауваження**: Поточні дані читаються з ресурсів (як локальних, так і віддалених) по шматках, і будь-які незатребувані дані зберігаються у внутрішніх буферах. Коли новий фільтр додається на початок потоку, дані у внутрішніх буферах, який вже були оброблені через інші фільтри, *не* будуть оброблені через новий фільтр. Це відрізняється від поведінки функції [stream\_filter\_append()](function.stream-filter-append.html)

> **Зауваження**: Коли фільтр додається для читання та запису, створюються два екземпляри фільтра. Функція [stream\_filter\_append()](function.stream-filter-append.html) повинна бути викликана двічі з **`STREAM_FILTER_READ`** і **`STREAM_FILTER_WRITE`** щоб отримати обидва ресурси фільтра.

### Дивіться також

-   [stream\_filter\_register()](function.stream-filter-register.html) - Реєструє потоковий фільтр, визначений користувачем
-   [stream\_filter\_append()](function.stream-filter-append.html) - Прикріпити фільтр до потоку