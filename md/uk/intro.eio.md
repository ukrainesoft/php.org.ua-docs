---
navigation:
  - book.eio.md: « Eio
  - eio.setup.md: Встановлення та налаштування »
  - index.md: PHP Manual
  - book.eio.md: Eio
title: Вступ
---
# Вступ

Модуль реалізує підсистему введення-виведення POSIX I/O засобів [» libeio](http://software.schmorp.de/pkg/libeio.md) Бібліотека C Написана Марком Леманном (Marc Lehmann).

> **Зауваження**: Для Windows-платформ цей модуль недоступний.

**Увага**

Слід врахувати, кожен запит виконується окремому потоці, у своїй виконання запитів безперервно, які порядок у черзі виконання непередбачуваний. Наприклад, наведений нижче приклад коду невірний.

**Приклад #1 Приклад неправильних запитів**

```php
<?php
// Запрос на создание символической ссылки $link на файл $filename
eio_symlink($filename, $link);

// Запрос на переименование файла $filename в $new_filename
eio_rename($filename, $new_filename);

// Выполнение запросов
eio_event_loop();
?>
```

У наведеному вище прикладі запит [eiorename()](function.eio-rename.html) може бути виконаний перед [eiosymlink()](function.eio-symlink.html). Правильним рішенням буде виклик [eiorename()](function.eio-rename.html) callback-функцією в [eiosymlink()](function.eio-symlink.md)

**Приклад #2 Створення запиту за допомогою callback-функції**

```php
<?php
function my_symlink_done($filename, $result) {
 // Запрос на переменование $filename в $new_filename
 eio_rename($filename, "/path/to/new-name");

 // Выполнение запросов
 eio_event_loop();
}

// Запрос на создание символической ссылки $link на файл $filename
eio_symlink($filename, $link, EIO_PRI_DEFAULT, "my_symlink_done", $filename);

// Выполнение запросов
eio_event_loop();
?>
```

Альтернативним рішенням є створення групи запитів:

**Приклад #3 Створення запиту за допомогою callback-функції**

```php
<?php
/* Функция вызывается после выполнения группы запросов */
function my_grp_done($data, $result) {
 // ...
}

function my_symlink_done($filename, $result) {
 // Создание запроса eio_rename и добавление его в группу
 $req = eio_rename($filename, "/path/to/new-name");
 eio_grp_add($grp, $req);
 // Возможно, вы захотите добавить больше запросов...
}

// Создание группы запросов
$grp = eio_grp("my_grp_done", "my_grp_data");

// Создание запроса eio_symlink request и добавление в группу
// Передача $filename в callback-функцию
$req = eio_symlink($filename, $link,
  EIO_PRI_DEFAULT, "my_symlink_done", $filename);
eio_grp_add($grp, $req);

// Выполнение запросов
eio_event_loop();
?>
```

Група – це спеціальний вид запиту, що дозволяє створити набір звичайних. *eio*запитів. Це може бути використане для створення складних запитів, які відкривають, читають та закривають файл.

Починаючи з версії 0.3.0 alpha, змінна, що використовується для внутрішньої взаємодії з libeio, може бути отримана функцією [eiogeteventstream()](function.eio-get-event-stream.md). Змінна може бути використана для прив'язки до циклу обробки, що поставляється стороннім модулем. Можливо організувати простий цикл обробки, де eio і libevent працюють спільно.

**Приклад #4 Використання eio спільно з libevent**

```php
<?php
function my_eio_poll($fd, $events, $arg) {
    /* Некоторые действия с libevent могут быть здесь */
    if (eio_nreqs()) {
        eio_poll();
    }
    /* .. и здесь */
}

function my_res_cb($d, $r) {
    var_dump($r); var_dump($d);
}

$base = event_base_new();
$event = event_new();

// Этот поток требуется для привязки к libevent
$fd = eio_get_event_stream();

eio_nop(EIO_PRI_DEFAULT, "my_res_cb", "nop data");
eio_mkdir("/tmp/abc-eio-temp", 0750, EIO_PRI_DEFAULT, "my_res_cb", "mkdir data");
/* Прочие eio_* запросы  ... */


// Установка флагов события
event_set($event, $fd, EV_READ /*| EV_PERSIST*/, "my_eio_poll", array($event, $base));

// Установка основы события
event_base_set($event, $base);

// Включение события
event_add($event);

// Запуск цикла обработки
event_base_loop($base);

/* То же самое доступно через интерфейс буфера libevent */
?>
```
