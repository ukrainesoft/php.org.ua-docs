---
navigation:
  - class.win32serviceexception.md: « Win32ServiceException
  - ref.win32service.md: win32service »
  - index.md: PHP Manual
  - book.win32service.md: win32service
title: Приклади
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Приклади

**Приклад #1 Реєстрація скрипту PHP для запуску як служба**

```php
<?php
win32_create_service(array(
    'service'     => 'dummyphp',                                           # tимя службы
    'display'     => 'sample dummy PHP service',                           # короткое описание
    'description' => 'This is a dummy Windows service created using PHP.', # длинное описание
    'params'      => '"' . __FILE__ . '"  run',                            # путь к скрипту и параметрам
));
?>
```

**Приклад #2 Видалення реєстрації служби**

```php
<?php
win32_delete_service('dummyphp');
?>
```

**Приклад #3 Запуск служби**

```php
<?php
if ($argv[1] == 'run') {
  win32_start_service_ctrl_dispatcher('dummyphp');

  while (WIN32_SERVICE_CONTROL_STOP != win32_get_last_control_message()) {
    # тут творим свои дела.
    # пытаемся сотворить их быстрее, чем за 30 секунд.
  }
}
?>
```
