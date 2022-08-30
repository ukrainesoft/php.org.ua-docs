Приклади

-   [« Обумовлені константи](eio.constants.md)
    
-   [Eio Функции »](ref.eio.md)
    
-   [PHP Manual](index.md)
    
-   [Eio](book.eio.md)
    
-   Приклади
    

# Приклади

**Приклад #1 Скасування запиту**

```php
<?php
 /* Вызывается после завершения eio_nop() */
 function my_nop_cb($data, $result) {
  echo "my_nop ", $data, "\n";
 }

// Этот eio_nop() будет отменён
$req = eio_nop(EIO_PRI_DEFAULT, "my_nop_cb", "1");
var_dump($req);
eio_cancel($req);

// Этот eio_nop() будет выполнен
eio_nop(EIO_PRI_DEFAULT, "my_nop_cb", "2");

// Выполнение запросов
eio_event_loop();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
resource(4) of type (EIO Request Descriptor)
my_nop 2
```

**Приклад #2 [eiochmod()](function.eio-chmod.html)**

```php
<?php
$temp_filename = dirname(__FILE__) ."/eio-temp-file.tmp";
touch($temp_filename);

/* Вызывается после завершения eio_chmod() */
function my_chmod_callback($data, $result) {
    global $temp_filename;

    if ($result == 0 && !is_readable($temp_filename) && is_writable($temp_filename)) {
        echo "eio_chmod_ok";
    }

    @unlink($temp_filename);
}

eio_chmod($temp_filename, 0200, EIO_PRI_DEFAULT, "my_chmod_callback");
eio_event_loop();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
eio_chmod_ok
```

**Приклад #3 Створення запиту користувача**

```php
<?php
/* Пользовательская функция обратного вызова */
function my_custom_callback($data, $result) {
    var_dump($data);
    var_dump(count($result));
    var_dump($result['data_modified']);
    var_dump($result['result']);
}

/* Пользовательский запрос */
function my_custom($data) {
    var_dump($data);

    $result  = array(
        'result'        => 1001,
        'data_modified' => "my custom data",
    );

    return $result;
}

$data = "my_custom_data";
$req = eio_custom("my_custom", EIO_PRI_DEFAULT, "my_custom_callback", $data);
var_dump($req);
eio_event_loop();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
resource(4) of type (EIO Request Descriptor)
string(14) "my_custom_data"
string(14) "my_custom_data"
int(2)
string(14) "my custom data"
int(1001)
```

**Приклад #4 Угруповання запитів**

```php
<?php
/*
 * Создание группы запросов для открытия, чтения и закрытия файла
 */

$temp_filename = dirname(__FILE__) ."/eio-file.tmp";
$fp = fopen($temp_filename, "w");
fwrite($fp, "some data");
fclose($fp);

/* Вызывается, когда группа запросов будет выполнена */
function my_grp_done($data, $result) {
 global $temp_filename;
 var_dump($result == 0);
 @unlink($temp_filename);
}

/* Вызывается после выполнения eio_open() */
function my_grp_file_opened_callback($data, $result) {
 global $my_file_fd, $grp;

 $my_file_fd = $result;

 var_dump($result > 0);

 // Создание запроса eio_read() и добавление в группу
 $req = eio_read($my_file_fd, 4, 0, EIO_PRI_DEFAULT, "my_grp_file_read_callback");
 eio_grp_add($grp, $req);
}

/* Вызывается после выполнения eio_read() */
function my_grp_file_read_callback($data, $result) {
 global $my_file_fd, $grp;

 var_dump($result);

 // Создание запроса eio_close() и добавление в группу
 $req = eio_close($my_file_fd);
 eio_grp_add($grp, $req);
}

$grp = eio_grp("my_grp_done", "my_grp_data");

// Создание запроса eio_open() и добавление в группу
$req = eio_open($temp_filename, EIO_O_RDWR | EIO_O_APPEND , NULL,
  EIO_PRI_DEFAULT, "my_grp_file_opened_callback", NULL);
eio_grp_add($grp, $req);
var_dump($grp);

eio_event_loop();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
resource(6) of type (EIO Group Descriptor)
bool(true)
string(4) "some"
bool(true)
```

**Приклад #5 Використання eio спільно з модулем libevent**

```php
<?php
function my_eio_poll($fd, $events, $arg) {
    /* Некоторые действия с libevent могут быть здесь */
    if (eio_nreqs()) {
        eio_poll();
    }
    /* .. и здесь */
}

function my_nop_cb($d, $r) {
    var_dump($r); var_dump($d);
}

$base = event_base_new();
$event = event_new();

$fd = eio_get_event_stream();
var_dump($fd);

eio_nop(EIO_PRI_DEFAULT, "my_nop_cb", "nop data");
eio_mkdir("/tmp/abc-eio-temp", 0750, EIO_PRI_DEFAULT, "my_nop_cb", "nop data");
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

Результатом виконання цього прикладу буде щось подібне:

```
int(3)
int(0)
string(8) "nop data"
int(0)
string(10) "mkdir data"
```

**Приклад #6 Використання eio з модулем event**

```php
<?php
$base = new EventBase();

// Получаем поток опроса eio.
// Обратите внимание, что эта переменная должна быть жива все время
// пока запущен цикл событий
$eio_stream = eio_get_event_stream();

// Связываем поток опроса eio polling с циклом событий.
$poll_event = new Event($base, $eio_stream, Event::READ, function () {
  if (eio_nreqs()) {
    eio_poll();
  }
});
$poll_event->add();

// Добавляем задачу eio
eio_nop(EIO_PRI_DEFAULT, function () {
  echo "eio_nop\n";
});

// Добавляем события
$timer = Event::timer($base, function () {
  echo "прошло 2 секунды\n";
});
$timer->add(2);

// Отправляем события
$base->dispatch();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
eio_nop
прошло 2 секунды
```