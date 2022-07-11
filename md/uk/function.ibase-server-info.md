- [« ibase_rollback](function.ibase-rollback.md)
- [ibase_service_attach »](function.ibase-service-attach.md)

- [PHP Manual](index.md)
- [Функції Firebird/InterBase](ref.ibase.md)
- Запитує інформацію про сервер бази даних

# ibase_server_info

(PHP 5, PHP 7 \< 7.4.0)

ibase_server_info — Запитує інформацію про сервер бази даних

### Опис

**ibase_server_info**(resource `$service_handle`, int `$action`): string

### Список параметрів

`service_handle`
Раніше створене з'єднання із сервером бази даних.

`action`
Допустима константа.

### Значення, що повертаються

Повертає змішані типи залежно від контексту.

### Приклади

**Приклад #1 Приклад використання
[ibase_service_attach()](function.ibase-service-attach.md)**

` <?php    // Присоединение к удаленному серверу Firebird    if (($service = ibase_service_attach('10.1.1.254/3050', 'sysdba', 'masterkey')) != FALSE) {        // Присоединение прошло успешно. // Висновок інформації        echo "Версія сервера: " . ibase_server_info($service, IBASE_SVC_SERVER_VERSION) . "
";        echo "Реалізація сервера: " . ibase_server_info($service, IBASE_SVC_IMPLEMENTATION) . "
";        echo "Користувачі сервера: " . print_r(ibase_server_info($service, IBASE_SVC_GET_USERS), true) . "
";        echo "Директорія сервера: " . ibase_server_info($service, IBASE_SVC_GET_ENV) . "
";        echo "Шлях блокування сервера: " . ibase_server_info($service, IBASE_SVC_GET_ENV_LOCK) . "
";        echo "Шлях до бібліотекам сервера: " . ibase_server_info($service, IBASE_SVC_GET_ENV_MSG) . "
";        echo "Шлях користувача бази даних: " . ibase_server_info($service, IBASE_SVC_USER_DBPATH) . "
";        echo "Встановлені з'єднання: " . print_r(ibase_server_info($service, IBASE_SVC_SVR_DB_INFO),true) . "
";        // Отсоединение от сервера (отключение)        ibase_service_detach($service);    }    else {        // Вывод сообщения в случае возникновения ошибки        $conn_error = ibase_errmsg();        die($conn_error);    }?> `

Результат виконання цього прикладу:

Версія сервера: LI-V3.0.4.33054 Firebird 3.0
Реалізація сервера: Firebird/Linux/AMD/Intel/x64
Користувачі сервера: Array
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

Директорія сервера: /etc/firebird/
Шлях блокування сервера: /tmp/firebird/
Шлях до бібліотек сервера: /usr/lib64/firebird/lib/
Шлях користувача бази даних: /var/lib/firebird/secdb/security3.fdb
Встановлені з'єднання: Array
(
[attachments] => 3
[databases] => 2
[0] => /srv/firebird/poss.fdb
[1] => /srv/firebird/employees.fdb
)
