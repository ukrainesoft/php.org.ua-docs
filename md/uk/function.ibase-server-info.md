---
navigation:
  - function.ibase-rollback.md: « ibase\_rollback
  - function.ibase-service-attach.md: ibase\_service\_attach »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_server\_info
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_server\_info

(PHP 5, PHP 7 < 7.4.0)

ibase\_server\_info — Запитує інформацію про сервер бази даних

### Опис

```methodsynopsis
ibase_server_info(resource $service_handle, int $action): string
```

### Список параметрів

`service_handle`

Раніше створене з'єднання із сервером бази даних.

`action`

Допустима константа.

### Значення, що повертаються

Повертає змішані типи залежно від контексту.

### Приклади

**Приклад #1 Приклад использования[ibase\_service\_attach()](function.ibase-service-attach.md)**

```php
<?php
    // Присоединение к удаленному серверу Firebird
    if (($service = ibase_service_attach('10.1.1.254/3050', 'sysdba', 'masterkey')) != FALSE) {

        // Присоединение прошло успешно.

        // Вывод информации
        echo "Версия сервера: " . ibase_server_info($service, IBASE_SVC_SERVER_VERSION) . "\n";
        echo "Реализация сервера: " . ibase_server_info($service, IBASE_SVC_IMPLEMENTATION) . "\n";
        echo "Пользователи сервера: " . print_r(ibase_server_info($service, IBASE_SVC_GET_USERS), true) . "\n";
        echo "Директория сервера: " . ibase_server_info($service, IBASE_SVC_GET_ENV) . "\n";
        echo "Путь блокировки сервера: " . ibase_server_info($service, IBASE_SVC_GET_ENV_LOCK) . "\n";
        echo "Путь к библиотекам сервера: " . ibase_server_info($service, IBASE_SVC_GET_ENV_MSG) . "\n";
        echo "Путь пользователя базы данных: " . ibase_server_info($service, IBASE_SVC_USER_DBPATH) . "\n";
        echo "Установленные соединения: " . print_r(ibase_server_info($service, IBASE_SVC_SVR_DB_INFO),true) . "\n";

        // Отсоединение от сервера (отключение)
        ibase_service_detach($service);

    }
    else {
        // Вывод сообщения в случае возникновения ошибки
        $conn_error = ibase_errmsg();
        die($conn_error);
    }
?>
```

Результат виконання наведеного прикладу:

```
Версия сервера: LI-V3.0.4.33054 Firebird 3.0
Реализация сервера: Firebird/Linux/AMD/Intel/x64
Пользователи сервера: Array
(
    [0] => Array
        (
            [user_name] => SYSDBA
            [first_name] => Sql
            [middle_name] => Server
            [last_name] => Administrator
            [user_id] => 0
            [group_id] => 0
        )

)

Директория сервера: /etc/firebird/
Путь блокировки сервера: /tmp/firebird/
Путь к библиотекам сервера: /usr/lib64/firebird/lib/
Путь пользователя базы данных: /var/lib/firebird/secdb/security3.fdb
Установленные соединения: Array
(
    [attachments] => 3
    [databases] => 2
    [0] => /srv/firebird/poss.fdb
    [1] => /srv/firebird/employees.fdb
)
```
