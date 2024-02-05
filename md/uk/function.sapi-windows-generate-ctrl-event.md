---
navigation:
  - function.sapi-windows-cp-set.md: « sapi\_windows\_cp\_set
  - function.sapi-windows-set-ctrl-handler.md: sapi\_windows\_set\_ctrl\_handler »
  - index.md: PHP Manual
  - ref.misc.md: Різні функції
title: sapi\_windows\_generate\_ctrl\_event
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sapi\_windows\_generate\_ctrl\_event

(PHP 7 >= 7.4.0, PHP 8)

sapi\_windows\_generate\_ctrl\_event — Надіслати подію CTRL іншому процесу

### Опис

```methodsynopsis
sapi_windows_generate_ctrl_event(int $event, int $pid = 0): bool
```

Надіслати подію CTRL іншому процесу у тій самій групі процесів.

### Список параметрів

`event`

Подія `CTRL` **`PHP_WINDOWS_EVENT_CTRL_C`**или**`PHP_WINDOWS_EVENT_CTRL_BREAK`**

`pid`

Ідентифікатор процесу, якому необхідно надіслати подію. Якщо поставлено як , то подія буде надіслано всім процесам групи.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Использование**sapi\_windows\_generate\_ctrl\_event()\*\*\*\*

У цьому прикладі показано, як надіслати події `CTRL+BREAK`дочернему процессу. В данном случае дочерний процесс будет печатать`Я все ще живий!` раз на секунду, доки користувач не натисне `CTRL+BREAK`. Після цього дочірній процес завершиться.

```php
<?php
// Пересылка событий CTRL+BREAK дочернему процессу
sapi_windows_set_ctrl_handler('sapi_windows_generate_ctrl_event');

// Создаём дочерний процесс
$cmd = ['php', '-r', 'while (true) { echo "Я всё ещё жив!\n"; sleep(1); }'];
$descspec = array(['pipe', 'r'], ['pipe', 'w'], ['pipe', 'w']);
$options = ['create_process_group' => true];
$proc = proc_open($cmd, $descspec, $pipes, null, null, $options);
while (true) {
    echo fgets($pipes[1]);
}
?>
```

### Дивіться також

-   [proc\_open()](function.proc-open.md) \- Виконати команду та відкрити покажчик на файл для введення/виводу
-   [sapi\_windows\_set\_ctrl\_handler()](function.sapi-windows-set-ctrl-handler.md) \- Встановити чи видалити обробник події CTRL
