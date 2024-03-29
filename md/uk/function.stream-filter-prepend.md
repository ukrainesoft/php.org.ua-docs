---
navigation:
  - function.stream-filter-append.md: « stream\_filter\_append
  - function.stream-filter-register.md: stream\_filter\_register »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_filter\_prepend
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_filter\_prepend

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

stream\_filter\_prepend — Прикріплює фільтр до потоку

### Опис

```methodsynopsis
stream_filter_prepend(    resource $stream,    string $filtername,    int $read_write = ?,    mixed $params = ?): resource
```

Добавляет`filtername` до списку фільтрів, прикріплених до потоку `stream`

### Список параметрів

`stream`

Цільовий потік.

`filtername`

Назва потоку.

`read_write`

По умолчанию, функция\*\*stream\_filter\_prepend()\*\*будет прикреплять фильтр к`ланцюжку фільтрів читання`, якщо файл був відкритий для читання (тобто режим файлу: `r`, и/или`+` ). Фільтр також буде прикріплений до `ланцюжку фільтрів запису`, якщо файл був відкритий для запису (тобто режим файлу: `w` `a`, и/или`+` ). Константи **`STREAM_FILTER_READ`** **`STREAM_FILTER_WRITE`**и/или**`STREAM_FILTER_ALL`** також можуть бути передані у параметрі `read_write`, щоб перевизначити цю поведінку. Дивіться функцію [stream\_filter\_append()](function.stream-filter-append.md) для використання цього параметра.

`params`

Цей фільтр буде додано із зазначеними параметрами `params`к*початку* списку і, таким чином, буде викликано першим під час потокових операцій. Щоб додати фільтр до кінця списку, використовуйте [stream\_filter\_append()](function.stream-filter-append.md)

### Значення, що повертаються

Повертає ресурс у разі успішного виконання або **`false`** у разі виникнення помилки. Ресурс повинен бути використаний для посилання на цей екземпляр фільтра під час виклику [stream\_filter\_remove()](function.stream-filter-remove.md)

Поверне **`false`**, якщо `stream` не є ресурсом або якщо `filtername`не найден.

### Примітки

> **Зауваження** **При використанні фільтрів користувача**  
> Спочатку має бути викликана функція [stream\_filter\_register()](function.stream-filter-register.md) для того, щоб зареєструвати бажаний фільтр користувача на ім'я `filtername`

> **Зауваження**: Поточні дані читаються з ресурсів (як локальних, так і віддалених) по шматках, і будь-які незатребувані дані зберігаються у внутрішніх буферах. Коли новий фільтр додається на початок потоку, дані у внутрішніх буферах, який вже були оброблені через інші фільтри, *не* будуть оброблені через новий фільтр. Це відрізняється від поведінки функції [stream\_filter\_append()](function.stream-filter-append.md)

> **Зауваження**: Коли фільтр додається для читання та запису, створюються два екземпляри фільтра. Функція [stream\_filter\_append()](function.stream-filter-append.md) повинна бути викликана двічі з **`STREAM_FILTER_READ`** і **`STREAM_FILTER_WRITE`** щоб отримати обидва ресурси фільтра.

### Дивіться також

-   [stream\_filter\_register()](function.stream-filter-register.md) \- Реєструє потоковий фільтр, визначений користувачем
-   [stream\_filter\_append()](function.stream-filter-append.md) \- Прикріпити фільтр до потоку
