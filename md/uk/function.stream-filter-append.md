---
navigation:
  - function.stream-copy-to-stream.md: « streamcopyтоstream
  - function.stream-filter-prepend.md: streamfilterprepend »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: streamfilterappend
---
# streamfilterappend

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

streamfilterappend — Прикріпити фільтр до потоку

### Опис

```methodsynopsis
stream_filter_append(    resource $stream,    string $filtername,    int $read_write = ?,    mixed $params = ?): resource
```

Додає `filtername` до списку фільтрів, прикріплених до `stream`

### Список параметрів

`stream`

Цільовий потік.

`filtername`

Назва фільтра.

`read_write`

За замовчуванням **streamfilterappend()** буде прикріплювати фільтр до `цепочке фильтров чтения`, якщо файл був відкритий для читання (тобто режим файлу: `r`, та/або `+`). Фільтр також буде прикріплений до `цепочке фильтров записи`, якщо файл був відкритий для запису (тобто режим файлу: `w` `a`, та/або `+`). Константи **`STREAM_FILTER_READ`** **`STREAM_FILTER_WRITE`** та/або **`STREAM_FILTER_ALL`** також можуть бути передані у параметрі `read_write`, щоб перевизначити цю поведінку.

`params`

Цей фільтр буде додано із зазначеними `params` до *кінцю* списку і, таким чином, буде викликано останнім у списку потокових операцій. Щоб додати фільтр до початку списку, використовуйте [streamfilterprepend()](function.stream-filter-prepend.md)

### Значення, що повертаються

Повертає ресурс у разі успішного виконання або **`false`** при невдачі. Ресурс повинен бути використаний для посилання на цей екземпляр фільтра під час виклику [streamfilterremove()](function.stream-filter-remove.md)

Поверне **`false`**, якщо `stream` не є ресурсом або якщо `filtername` НЕ знайдений.

### Приклади

**Приклад #1 Контроль застосування фільтрів**

```php
<?php
/* Открываем тестовый файл для чтения и записи */
$fp = fopen('test.txt', 'w+');

/* Прикрепляем фильтр ROT13 к
 * цепочке фильтров записи, но не к
 * цепочке фильтров чтения */
stream_filter_append($fp, "string.rot13", STREAM_FILTER_WRITE);

/* Запишем простую строку в файл
 * она будет преобразована при помощи ROT13
 * на выходе */
fwrite($fp, "This is a test\n");

/* Назад к началу файла */
rewind($fp);

/* Прочитаем содержимое файла.
 * Если фильтр также был бы прикреплён к
 * цепочке фильтров чтения, мы бы увидели
 * преобразованный при помощи ROT13 текст в исходном состоянии */
fpassthru($fp);

fclose($fp);

/* Ожидаемый вывод
   ---------------

Guvf vf n grfg

 */
?>
```

### Примітки

> **Зауваження** **При використанні фільтрів користувача**  
> Спочатку має бути викликана функція [streamfilterregister()](function.stream-filter-register.md) для того, щоб зареєструвати бажаний фільтр користувача на ім'я `filtername`

> **Зауваження**: Поточні дані читаються з ресурсів (як локальних, так і віддалених) по шматках, і будь-які незатребувані дані зберігаються у внутрішніх буферах. Коли новий фільтр додається в кінець потоку, дані у внутрішніх буферах обробляються через новий фільтр. Це відрізняється від поведінки функції [streamfilterprepend()](function.stream-filter-prepend.md)

> **Зауваження**: Коли фільтр додається для читання та запису, створюються два екземпляри фільтра. Функція **streamfilterappend()** повинна бути викликана двічі з **`STREAM_FILTER_READ`** і **`STREAM_FILTER_WRITE`** щоб отримати обидва ресурси фільтра.

### Дивіться також

-   [streamfilterregister()](function.stream-filter-register.md) - Реєструє потоковий фільтр, визначений користувачем
-   [streamfilterprepend()](function.stream-filter-prepend.md) - Прикріплює фільтр до потоку
-   [streamgetfilters()](function.stream-get-filters.md) - Отримати список зареєстрованих фільтрів
