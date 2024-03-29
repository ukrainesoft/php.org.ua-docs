---
navigation:
  - function.inotify-add-watch.md: « inotify\_add\_watch
  - function.inotify-queue-len.md: inotify\_queue\_len »
  - index.md: PHP Manual
  - ref.inotify.md: Функції Inotify
title: inotify\_init
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# inotify\_init

(PECL inotify >= 0.1.2)

inotify\_init - Ініціалізує екземпляр inotify

### Опис

```methodsynopsis
inotify_init(): resource
```

Ініціалізує екземпляр inotify для використання в [inotify\_add\_watch()](function.inotify-add-watch.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Потоковий ресурс або **`false`**

### Приклади

**Приклад #1 Приклад використання inotify**

```php
<?php
// Создаём экземпляр inotify
$fd = inotify_init();

// Отслеживаем __FILE__ на предмет изменения метаданных (наПриклад mtime)
$watch_descriptor = inotify_add_watch($fd, __FILE__, IN_ATTRIB);

// создаём событие
touch(__FILE__);

// Читаем события
$events = inotify_read($fd);
print_r($events);

// Следующие функции позволяют использовать функции inotify без блокировки на inotify_read():

// - Используем stream_select() для $fd:
$read = array($fd);
$write = null;
$except = null;
stream_select($read,$write,$except,0);

// - Используем stream_set_blocking() для $fd
stream_set_blocking($fd, 0);
inotify_read($fd); // Не блокируем и возвращаем false если нет ожидающих событий

// - Используем inotify_queue_len() для проверки, что очередь событий не пуста
$queue_len = inotify_queue_len($fd); // Если > 0, inotify_read() то не блокируем

// Заканчиваем наблюдать за __FILE__
inotify_rm_watch($fd, $watch_descriptor);

// Закрываем экземпляр inotify
// Все не закрытые наблюдатели будут закрыты
fclose($fd);

?>
```

Висновок наведеного прикладу буде схожим на:

```
array(
  array(
    'wd' => 1,     // Equals $watch_descriptor
    'mask' => 4,   // IN_ATTRIB bit is set
    'cookie' => 0, // unique id to connect related events (e.g.
                   // IN_MOVE_FROM and IN_MOVE_TO events)
    'name' => '',  // the name of a file (e.g. if we monitored changes
                   // in a directory)
  ),
);
```

### Дивіться також

-   [inotify\_add\_watch()](function.inotify-add-watch.md) \- Додати спостерігача для екземпляра inotify
-   [inotify\_rm\_watch()](function.inotify-rm-watch.md) \- Видалити спостерігача
-   [inotify\_queue\_len()](function.inotify-queue-len.md) \- Повертає кількість очікуваних подій у черзі
-   [inotify\_read()](function.inotify-read.md) \- Читає очікуючі повідомлення з черги
-   [fclose()](function.fclose.md) \- Закриває відкритий дескриптор файлу
