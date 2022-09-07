---
navigation:
  - pcntl.examples.md: « Приклади
  - ref.pcntl.md: Функції PCNTL »
  - index.md: PHP Manual
  - pcntl.examples.md: Приклади
title: Базове застосування
---
## Базове застосування

Цей приклад породжує процес-демон із обробником сигналів.

**Приклад #1 Приклад Управління процесами**

```php
<?php
declare(ticks=1);

$pid = pcntl_fork();
if ($pid == -1) {
     die("Не удалось породить процесс");
} else if ($pid) {
     exit(); // это код родителя
} else {
     // это дочерний код
}

// Открепление от управляющего терминала
if (posix_setsid() == -1) {
    die("Не удалось открепить от терминала");
}

// Установка обработчиков сигналов
pcntl_signal(SIGTERM, "sig_handler");
pcntl_signal(SIGHUP, "sig_handler");

// Бесконечный цикл выполнения задач
while (1) {

    // делаем тут что-то интересное

}

function sig_handler($signo)
{

     switch ($signo) {
         case SIGTERM:
             // обработка сигнала завершения
             exit;
             break;
         case SIGHUP:
             // обработка перезапуска задач
             break;
         default:
             // обработка других сигналов
     }

}

?>
```
