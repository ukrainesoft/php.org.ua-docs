---
navigation:
  - function.stream-copy-to-stream.md: « stream\_copy\_to\_stream
  - function.stream-filter-prepend.md: stream\_filter\_prepend »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_filter\_append
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_filter\_append

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

stream\_filter\_append — Прикріпити фільтр до потоку

### Опис

```methodsynopsis
stream_filter_append(    resource $stream,    string $filtername,    int $read_write = ?,    mixed $params = ?): resource
```

Добавляет`filtername` до списку фільтрів, прикріплених до `stream`

### Список параметрів

`stream`

Цільовий потік.

`filtername`

Назва фільтра.

`read_write`

По умолчанию\*\*stream\_filter\_append()\*\*будет прикреплять фильтр к`ланцюжку фільтрів читання`, якщо файл був відкритий для читання (тобто режим файлу: `r`, и/или`+` ). Фільтр також буде прикріплений до `ланцюжку фільтрів запису`, якщо файл був відкритий для запису (тобто режим файлу: `w` `a`, и/или`+` ). Константи **`STREAM_FILTER_READ`** **`STREAM_FILTER_WRITE`**и/или**`STREAM_FILTER_ALL`** також можуть бути передані у параметрі `read_write`, щоб перевизначити цю поведінку.

`params`

Цей фільтр буде додано із зазначеними `params`к*кінцю* списку і, таким чином, буде викликано останнім у списку потокових операцій. Щоб додати фільтр до початку списку, використовуйте [stream\_filter\_prepend()](function.stream-filter-prepend.md)

### Значення, що повертаються

Повертає ресурс у разі успішного виконання або **`false`** при невдачі. Ресурс повинен бути використаний для посилання на цей екземпляр фільтра під час виклику [stream\_filter\_remove()](function.stream-filter-remove.md)

Поверне **`false`**, якщо `stream` не є ресурсом або якщо `filtername`не найден.

### Приклади

**Приклад #1 Контроль застосування фільтрів**

```php
<?php
/* Открываем тестовый файл для чтения и записи */
$fp = fopen('test.txt', 'w+');

/* Прикрепляем фильтр ROT13 к
 * цепочке фильтров записи, но не к
 * цепочке фильтров чтения */
stream_filter_append($fp, "string.rot13", STREAM_FILTER_WRITE);

/* Запишем простую строку в файл
 * она будет преобразована при помощи ROT13
 * на выходе */
fwrite($fp, "This is a test\n");

/* Назад к началу файла */
rewind($fp);

/* Прочитаем содержимое файла.
 * Если фильтр также был бы прикреплён к
 * цепочке фильтров чтения, мы бы увидели
 * преобразованный при помощи ROT13 текст в исходном состоянии */
fpassthru($fp);

fclose($fp);

/* Ожидаемый вывод
   ---------------

Guvf vf n grfg

 */
?>
```

### Примітки

> **Зауваження** **При використанні фільтрів користувача**  
> Спочатку має бути викликана функція [stream\_filter\_register()](function.stream-filter-register.md) для того, щоб зареєструвати бажаний фільтр користувача на ім'я `filtername`

> **Зауваження**: Поточні дані читаються з ресурсів (як локальних, так і віддалених) по шматках, і будь-які незатребувані дані зберігаються у внутрішніх буферах. Коли новий фільтр додається в кінець потоку, дані у внутрішніх буферах обробляються через новий фільтр. Це відрізняється від поведінки функції [stream\_filter\_prepend()](function.stream-filter-prepend.md)

> **Зауваження**: Коли фільтр додається для читання та запису, створюються два екземпляри фільтра. Функція **stream\_filter\_append()** повинна бути викликана двічі з **`STREAM_FILTER_READ`**и**`STREAM_FILTER_WRITE`** щоб отримати обидва ресурси фільтра.

### Дивіться також

-   [stream\_filter\_register()](function.stream-filter-register.md) \- Реєструє потоковий фільтр, визначений користувачем
-   [stream\_filter\_prepend()](function.stream-filter-prepend.md) \- Прикріплює фільтр до потоку
-   [stream\_get\_filters()](function.stream-get-filters.md) \- Отримати список зареєстрованих фільтрів
