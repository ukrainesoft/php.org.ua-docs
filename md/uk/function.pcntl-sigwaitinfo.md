---
navigation:
  - function.pcntl-sigtimedwait.html: pcntlsigtimedwait
  - function.pcntl-strerror.html: pcntlstrerror »
  - index.html: PHP Manual
  - ref.pcntl.html: Функції PCNTL
title: pcntlsigwaitinfo
---
# pcntlsigwaitinfo

(PHP 5> = 5.3.0, PHP 7, PHP 8)

pcntlsigwaitinfo — Очікування сигналів

### Опис

```methodsynopsis
pcntl_sigwaitinfo(array $signals, array &$info = []): int|false
```

Функція **pcntlsigwaitinfo()** призупиняє виконання скрипту, що викликає, до тих пір, поки не буде доставлений один із сигналів, зазначених у `signals`. Якщо один із сигналів вже очікує обробки (наприклад, заблоковано [pcntlsigprocmask()](function.pcntl-sigprocmask.html)**pcntlsigwaitinfo()** негайно поверне управління.

### Список параметрів

`signals`

Масив очікуваних сигналів.

`info`

Аргумент `info` масив, що містить інформацію про сигнал.

Наступні ключі масиву (аргументу) застосовні всім сигналів

-   signo: Номер сигналу
-   errno: Номер помилки
-   код: Код сигналу

Наступні елементи масиву застосовуються для сигналу **`SIGCHLD`**

-   status: Статус виходу дочірнього процесу або сигнал, що змусив дочірній процес змінити стан
-   utime: Потрібний час користувача
-   stime: Потрібен системний час
-   pid: ID процесу-відправника
-   uid: ID користувача, що володіє процесом-відправником

Наступні елементи масиву застосовуються для сигналів **`SIGILL`** **`SIGFPE`** **`SIGSEGV`** і **`SIGBUS`**

-   addr: Адреса пам'яті, в якій стався збій

Наступні елементи масиву застосовуються для сигналу **`SIGPOLL`**

-   band: Подія введення-виводу
-   fd: Номер файлового дескриптора

### Значення, що повертаються

У разі успішного виконання функція **pcntlsigwaitinfo()** повертає номер сигналу або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **pcntlsigwaitinfo()****

```php
<?php
echo "Блокировка сигнала SIGHUP\n";
pcntl_sigprocmask(SIG_BLOCK, array(SIGHUP));

echo "Отправка сигнала SIGHUP самому себе\n";
posix_kill(posix_getpid(), SIGHUP);

echo "Ожидание сигналов\n";
$info = array();
pcntl_sigwaitinfo(array(SIGHUP), $info);
?>
```

### Дивіться також

-   [pcntlsigprocmask()](function.pcntl-sigprocmask.html) - Задає та витягує список сигналів, що блокуються.
-   [pcntlsigtimedwait()](function.pcntl-sigtimedwait.html) - Очікує сигнали протягом заданого часу
