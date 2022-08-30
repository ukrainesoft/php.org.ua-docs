Надіслати подію CTRL іншому процесу

-   [« sapiwindowsспset](function.sapi-windows-cp-set.html)
    
-   [sapiwindowssetctrlhandler »](function.sapi-windows-set-ctrl-handler.html)
    
-   [PHP Manual](index.md)
    
-   [Різні функції](ref.misc.md)
    
-   Надіслати подію CTRL іншому процесу
    

# sapiwindowsgeneratectrlevent

(PHP 7> = 7.4.0, PHP 8)

sapiwindowsgeneratectrlevent — Надіслати подію CTRL іншому процесу

### Опис

```methodsynopsis
sapi_windows_generate_ctrl_event(int $event, int $pid = 0): bool
```

Надіслати подію CTRL іншому процесу у тій самій групі процесів.

### Список параметрів

`event`

Подія `CTRL` **`PHP_WINDOWS_EVENT_CTRL_C`** або **`PHP_WINDOWS_EVENT_CTRL_BREAK`**

`pid`

Ідентифікатор процесу, якому необхідно надіслати подію. Якщо поставлено як `0`, то подія буде надіслано всім процесам групи.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Використання **sapiwindowsgeneratectrlevent()****

У цьому прикладі показано, як надіслати події `CTRL+BREAK` дочірнього процесу. У цьому випадку дочірній процес друкуватиме `Я всё ещё жив!` раз на секунду, доки користувач не натисне `CTRL+BREAK`. Після цього дочірній процес завершиться.

```php
<?php
// Пересылка событий CTRL+BREAK дочернему процессу
sapi_windows_set_ctrl_handler('sapi_windows_generate_ctrl_event');

// Создаём дочерний процесс
$cmd = ['php', '-r', 'while (true) { echo "Я всё ещё жив!\n"; sleep(1); }'];
$descspec = array(['pipe', 'r'], ['pipe', 'w'], ['pipe', 'w']);
$options = ['create_process_group' => true];
$proc = proc_open($cmd, $descspec, $pipes, null, null, $options);
while (true) {
    echo fgets($pipes[1]);
}
?>
```

### Дивіться також

-   [procopen()](function.proc-open.html) - Виконати команду та відкрити покажчик на файл для введення/виводу
-   [sapiwindowssetctrlhandler()](function.sapi-windows-set-ctrl-handler.html) - Встановити чи видалити обробник події CTRL