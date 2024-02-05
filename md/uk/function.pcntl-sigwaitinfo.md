---
navigation:
  - function.pcntl-sigtimedwait.md: « pcntl\_sigtimedwait
  - function.pcntl-strerror.md: pcntl\_strerror »
  - index.md: PHP Manual
  - ref.pcntl.md: Функції PCNTL
title: pcntl\_sigwaitinfo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pcntl\_sigwaitinfo

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

pcntl\_sigwaitinfo — Очікування сигналів

### Опис

```methodsynopsis
pcntl_sigwaitinfo(array $signals, array &$info = []): int|false
```

Функция**pcntl\_sigwaitinfo()** призупиняє виконання скрипту, що викликає, до тих пір, поки не буде доставлений один із сигналів, зазначених у `signals`. Якщо один із сигналів вже очікує обробки (наприклад, заблоковано [pcntl\_sigprocmask()](function.pcntl-sigprocmask.md)),**pcntl\_sigwaitinfo()** негайно поверне управління.

### Список параметрів

`signals`

Масив очікуваних сигналів.

`info`

Аргумент`info`массив, содержащий информацию о сигнале.

Наступні ключі масиву (аргументу) застосовні всім сигналів

-   signo: Номер сигналу
-   errno: Номер помилки
-   код: Код сигналу

Наступні елементи масиву застосовуються для сигналу **`SIGCHLD`** :

-   status: Статус виходу дочірнього процесу або сигнал, що змусив дочірній процес змінити стан
-   utime: Потрібний час користувача
-   stime: Потрібен системний час
-   pid: ID процесу-відправника
-   uid: ID користувача, що володіє процесом-відправником

Наступні елементи масиву застосовуються для сигналів **`SIGILL`** **`SIGFPE`** **`SIGSEGV`**и**`SIGBUS`** :

-   addr: Адреса пам'яті, в якій стався збій

Наступні елементи масиву застосовуються для сигналу **`SIGPOLL`**

-   band: Подія введення-виводу
-   fd: Номер файлового дескриптора

### Значення, що повертаються

У разі успішного виконання функція **pcntl\_sigwaitinfo()** повертає номер сигналу або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**pcntl\_sigwaitinfo()\*\*\*\*

```php
<?php
echo "Блокировка сигнала SIGHUP\n";
pcntl_sigprocmask(SIG_BLOCK, array(SIGHUP));

echo "Отправка сигнала SIGHUP самому себе\n";
posix_kill(posix_getpid(), SIGHUP);

echo "Ожидание сигналов\n";
$info = array();
pcntl_sigwaitinfo(array(SIGHUP), $info);
?>
```

### Дивіться також

-   [pcntl\_sigprocmask()](function.pcntl-sigprocmask.md) \- Задає та витягує список сигналів, що блокуються.
-   [pcntl\_sigtimedwait()](function.pcntl-sigtimedwait.md) \- Очікує сигнали протягом заданого часу
