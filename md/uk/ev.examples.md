---
navigation:
  - ev.global.constants.md: « Обумовлені константи
  - ev.watchers.md: Спостерігачі »
  - index.md: PHP Manual
  - book.ev.md: Єв
title: Приклади
---
# Приклади

**Приклад #1 Прості таймери**

```php
<?php
// Создаём и запускаем таймер на 2 секунды
$w1 = new EvTimer(2, 0, function () {
    echo "2 секунды прошло\n";
});

// Создаём и запускаем таймер, который сработает через 2 секунды, после чего будет срабатывать
// раз в секунду, пока вы его вручную не остановите
$w2 = new EvTimer(2, 1, function ($w) {
    echo "вызывается раз в секунду, первое срабатывание через 2 секунды\n";
    echo "итерация = ", Ev::iteration(), PHP_EOL;

    // Останавливаем наблюдателя через 5 итераций
    Ev::iteration() == 5 and $w->stop();
    // Остановливаем наблюдателя, если следующий вызов приведёт к десятой (или больше) итерации
    Ev::iteration() >= 10 and $w->stop();
});

// Создаём остановленный таймер. Он будет неактивен, пока мы его не запустим
$w_stopped = EvTimer::createStopped(10, 5, function($w) {
    echo "Callback-функция таймера, созданного остановленным\n";

    // Останавливаем наблюдателя через 2 итерации
    Ev::iteration() >= 2 and $w->stop();
});

// Запускаем событийный цикл, пока работает хотя бы один наблюдатель или пока не вызван Ev::stop()
Ev::run();

// Запускаем и смотрим, как он работает
$w_stopped->start();
echo "Запускаем одну итерацию\n";
Ev::run(Ev::RUN_ONCE);

echo "Перезапускаем второго наблюдателя и пытаемся отловить те же события, но не блокируем\n";
$w2->again();
Ev::run(Ev::RUN_NOWAIT);

$w = new EvTimer(10, 0, function() {});
echo "Запускаем блокирующий цикл\n";
Ev::run();
echo "END\n";
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
2 секунды прошло
вызывается раз в секунду, первое срабатывание через 2 секунды
итерация = 1
вызывается раз в секунду, первое срабатывание через 2 секунды
итерация = 2
вызывается раз в секунду, первое срабатывание через 2 секунды
итерация = 3
вызывается раз в секунду, первое срабатывание через 2 секунды
итерация = 4
вызывается раз в секунду, первое срабатывание через 2 секунды
итерация = 5
Запускаем одну итерацию
Функция обратного вызова таймера, созданного остановленным
Перезапускаем второго наблюдателя и пытаемся отловить те же события, но не блокируем
Запускаем блокирующий цикл
вызывается раз в секунду, первое срабатывание через 2 секунды
итерация = 8
вызывается раз в секунду, первое срабатывание через 2 секунды
итерация = 9
вызывается раз в секунду, первое срабатывание через 2 секунды
итерация = 10
END
```

**Приклад #2 Періодичний таймер. Спрацьовує раз на 10.5 секунд**

```php
<?php
$w = new EvPeriodic(0., 10.5, NULL, function ($w, $revents) {
    echo time(), PHP_EOL;
});

Ev::run();
?>
```

**Приклад #3 Періодичний таймер. Використання callback-функції для перезавдання інтервалу**

```php
<?php
// Срабатывает раз в 10.5 секунд

function reschedule_cb ($watcher, $now) {
    return $now + (10.5. - fmod($now, 10.5));
}

$w = new EvPeriodic(0., 0., "reschedule_cb", function ($w, $revents) {
    echo time(), PHP_EOL;
});

Ev::run();
?>
```

**Приклад #4 Періодичний таймер. Спрацьовує кожні 10.5 секунд, починаючи з поточного моменту**

```php
<?php
// Срабатывает раз в 10.5 секунд начиная с текущего момента
$w = new EvPeriodic(fmod(Ev::now(), 10.5), 10.5, NULL, function ($w, $revents) {
    echo time(), PHP_EOL;
});

Ev::run();
?>
```

**Приклад #5 Чекаємо, доки STDIN не стане читаним**

```php
<?php
// Ждём, пока STDIN не станет читаемым
$w = new EvIo(STDIN, Ev::READ, function ($watcher, $revents) {
    echo "STDIN is readable\n";
});

Ev::run(Ev::RUN_ONCE);
?>
```

**Приклад #6 Використовуємо асинхронне введення/виведення для доступу до сокету**

```php
<?php
/* Используем асинхронный ввод/вывод для доступа к сокету */

// Модуль `sockets' продолжит логировать предупреждения
// для EINPROGRESS, EAGAIN/EWOULDBLOCK etc.
error_reporting(E_ERROR);

$e_nonblocking = array (/*EAGAIN или EWOULDBLOCK*/11, /*EINPROGRESS*/115);

// Получаем порт для сервиса WWW
$service_port = getservbyname('www', 'tcp');

// Получаем IP-адрес целевого хоста
$address = gethostbyname('google.co.uk');

// Создаём сокет TCP/IP
$socket = socket_create(AF_INET, SOCK_STREAM, SOL_TCP);
if ($socket === FALSE) {
    echo "Ошибка при вызове socket_create(): причина: "
        .socket_strerror(socket_last_error()) . "\n";
}

// Устанавливаем флаг O_NONBLOCK
socket_set_nonblock($socket);

// Прерываем по превышению времени ожидания
$timeout_watcher = new EvTimer(10.0, 0., function () use ($socket) {
    socket_close($socket);
    Ev::stop(Ev::BREAK_ALL);
});

// Посылаем запрос HEAD когда сокет доступен для записи
$write_watcher = new EvIo($socket, Ev::WRITE, function ($w)
    use ($socket, $timeout_watcher, $e_nonblocking)
{
    // Останавливаем наблюдателя $timeout_watcher
    $timeout_watcher->stop();
    // Останавливаем наблюдателя $write_watcher
    $w->stop();

    $in = "HEAD / HTTP/1.1\r\n";
    $in .= "Host: google.co.uk\r\n";
    $in .= "Connection: Close\r\n\r\n";

    if (!socket_write($socket, $in, strlen($in))) {
        trigger_error("Ошибка записи $in в сокет", E_USER_ERROR);
    }

    $read_watcher = new EvIo($socket, Ev::READ, function ($w, $re)
        use ($socket, $e_nonblocking)
    {
        // Сокет доступен для чтения. Читаем 20 байт в неблокирующем режиме
        $ret = socket_recv($socket, $out, 20, MSG_DONTWAIT);

        if ($ret) {
            echo $out;
        } elseif ($ret === 0) {
            // Все прочтено
            $w->stop();
            socket_close($socket);
            return;
        }

        // Ловим EINPROGRESS, EAGAIN или EWOULDBLOCK
        if (in_array(socket_last_error(), $e_nonblocking)) {
            return;
        }

        $w->stop();
        socket_close($socket);
    });

    Ev::run();
});

$result = socket_connect($socket, $address, $service_port);

Ev::run();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
HTTP/1.1 301 Moved Permanently
Location: http://www.google.co.uk/
Content-Type: text/html; charset=UTF-8
Date: Sun, 23 Dec 2012 16:08:27 GMT
Expires: Tue, 22 Jan 2013 16:08:27 GMT
Cache-Control: public, max-age=2592000
Server: gws
Content-Length: 221
X-XSS-Protection: 1; mode=block
X-Frame-Options: SAMEORIGIN
Connection: close
```

**Приклад #7 Вбудовуємо один цикл в інший**

```php
<?php
/*
* Пытаемся получить встраиваемый цикл и встроить его в событийный цикл по умолчанию.
* Если это невозможно - используем цикл по умолчанию. Цикл по умолчанию
* хранится в $loop_hi, а встраиваемый в $loop_lo (который будет равен $loop_hi в случае
* если мы не будем использовать встраиваемый цикл).
*
* Пример взят из
* http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#Examples_CONTENT-9
*/
$loop_hi = EvLoop::defaultLoop();
$loop_lo = NULL;
$embed   = NULL;

/*
* Смотрим, есть ли возможность получить работающий
* (Значение 0 означает автоопределение)
*/
$loop_lo = Ev::embeddableBackends() & Ev::recommendedBackends()
    ? new EvLoop(Ev::embeddableBackends() & Ev::recommendedBackends())
    : 0;

if ($loop_lo) {
    $embed = new EvEmbed($loop_lo, function () {});
} else {
    $loop_lo = $loop_hi;
}
?>
```

**Приклад #8 Вбудовування циклу, створеного за допомогою kqueue у цикл за замовчуванням**

```php
<?php
/*
* Проверяем, что бэкенд kqueue доступен, но не рекомендован, и создаём его для
* работы с сокетами (которые обычно работают с любой реализацией kqueue).
* Сохраняем событийный цикл kqueue/socket-only в loop_socket. (Можно опционально
* использовать флаг EVFLAG_NOENV)
*
* Пример взят из
* http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#Examples_CONTENT-9
*/
$loop        = EvLoop::defaultLoop();
$socket_loop = NULL;
$embed       = NULL;

if (Ev::supportedBackends() & ~Ev::recommendedBackends() & Ev::BACKEND_KQUEUE) {
    if (($socket_loop = new EvLoop(Ev::BACKEND_KQUEUE))) {
        $embed = new EvEmbed($loop);
    }
}

if (!$socket_loop) {
    $socket_loop = $loop;
}

// теперь используем $socket_loop для всех сокетов, а $loop для всего остального
?>
```

**Приклад #9 Перехоплюємо сигнал SIGTERM**

```php
<?php
$w = new EvSignal(SIGTERM, function ($watcher) {
    echo "Получен сигнал SIGTERM\n";
    $watcher->stop();
});

Ev::run();
?>
```

**Приклад #10 Відстежуємо зміну /var/log/messages**

```php
<?php
// Используем интервал опроса в 10 секунд
$w = new EvStat("/var/log/messages", 8, function ($w) {
    echo "/var/log/messages изменён\n";

    $attr = $w->attr();

    if ($attr['nlink']) {
        printf("Текущий размер: %ld\n", $attr['size']);
        printf("Текущее значение atime: %ld\n", $attr['atime']);
        printf("Текущее значение mtime: %ld\n", $attr['mtime']);
    } else {
        fprintf(STDERR, "файл `messages` отсутствует!");
        $w->stop();
    }
});

Ev::run();
?>
```

**Приклад #11 Відслідковуємо зміну /var/log/messages. Уникаємо пропуску оновлень за допомогою затримки за одну секунду**

```php
<?php
$timer = EvTimer::createStopped(0., 1.02, function ($w) {
    $w->stop();

    $stat = $w->data;

    // 1 секунду после последнего изменения файла
    printf("Текущий размер: %ld\n", $stat->attr()['size']);
});

$stat = new EvStat("/var/log/messages", 0., function () use ($timer) {
    // Сбрасываем наблюдателя $timer
    $timer->again();
});

$timer->data = $stat;

Ev::run();
?>
```

**Приклад #12 Відслідковуємо зміни статусу процесу**

```php
<?php
$pid = pcntl_fork();

if ($pid == -1) {
    fprintf(STDERR, "pcntl_fork failed\n");
} elseif ($pid) {
    $w = new EvChild($pid, FALSE, function ($w, $revents) {
        $w->stop();

        printf("Процесс %d вышел с кодом %d\n", $w->rpid, $w->rstatus);
    });

    Ev::run();

    // Защита от зомби процессов
    pcntl_wait($status);
} else {
    // Порождённый потомок
    exit(2);
}
?>
```
