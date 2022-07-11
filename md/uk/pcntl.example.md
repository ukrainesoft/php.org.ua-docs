- [« Приклади](pcntl.examples.md)
- [Функції PCNTL »](ref.pcntl.md)

- [PHP Manual](index.md)
- [Приклади](pcntl.examples.md)
- Базове застосування

## Базове застосування

Цей приклад породжує процес-демон із обробником сигналів.

**Приклад #1 Приклад Управління процесами**

`<?phpdeclare(ticks=1);$pid = pcntl_fork();if ($pid == -1) {     die("Не удалося породити процес");} else if ($pid) | // это код родителя} else {     // это дочерний код}// Открепление от управляющего терминалаif (posix_setsid() == -1) {    die("Не удалось открепить от терминала");}// Установка обработчиков сигналовpcntl_signal(SIGTERM, "sig_handler");pcntl_signal(SIGHUP, "sig_handler");// Бесконечный цикл выполнения задачwhile (1) {    // делаем тут что-то интересное}function sig_handler($signo){     switch ($signo) {         case SIGTERM:             / / обробка сигналу завершення             exit; break; case? default:               // обробка інших сигналів     }}?> `
