- [«Win32ServiceException](class.win32serviceexception.md)
- [win32service »](ref.win32service.md)

- [PHP Manual](index.md)
- [win32service](book.win32service.md)
- Приклади

# Приклади

**Приклад #1 Реєстрація скрипта PHP для запуску в якості служби**

` <?phpwin32_create_service(array(    'service'     => 'dummyphp',                                           # tимя службы    'display'     => 'sample dummy PHP service',                           # короткое описание    'description' => 'This is a dummy Windows service created using PHP. ', # длинное описание    'params'      => '"' . __FILE__ . '"  run',                            # путь к скрипту и параметрам));?> `

**Приклад #2 Видалення реєстрації служби**

` <?phpwin32_delete_service('dummyphp');?> `

**Приклад #3 Запуск як служба**

`<?phpif ($argv[1] == 'run') {  win32_start_service_ctrl_dispatcher('dummyphp'); while(WIN32_SERVICE_CONTROL_STOP != win32_get_last_control_message()) {    # тут творимо свої справи. # намагаємося створити их швидше, чем за 30 секунд. }}?> `
