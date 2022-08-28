Вимикається від диспетчера служб

-   [« ibase\_service\_attach](function.ibase-service-attach.html)
    
-   [ibase\_set\_event\_handler »](function.ibase-set-event-handler.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Firebird/InterBase](ref.ibase.html)
    
-   Вимикається від диспетчера служб
    

# ibaseservicedetach

(PHP 5, PHP 7 < 7.4.0)

ibaseservicedetach — Вимикається від диспетчера служб

### Опис

```methodsynopsis
ibase_service_detach(resource $service_handle): bool
```

### Список параметрів

`service_handle`

Раніше створене з'єднання із сервером бази даних.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **ibaseservicedetach()****

```php
<?php
    // Присоединение к удаленному серверу Firebird по IP-адресу
    if (($service = ibase_service_attach('10.1.1.199', 'sysdba', 'masterkey')) != FALSE) {

        // Присоединение прошло успешно.
        // Возврат версии сервера (что-то вроде 'LI-V3.0.4.33054 Firebird 3.0')
        $server_version  = ibase_server_info($service, IBASE_SVC_SERVER_VERSION);

        // Возврат реализации сервера (что-то вроде 'Firebird/Linux/AMD/Intel/x64')
        $server_implementation = ibase_server_info($service, IBASE_SVC_IMPLEMENTATION);

        // Отсоединение от сервера (отключение)
        if(ibase_service_detach($service) == FALSE) {
            echo "Ошибка при отсоединении от службы.";
        }
        else {
            echo "Отсоединение от службы прошло успешно.";
        }

    }
    else {
        // Вывод сообщения в случае возникновения ошибки
        $conn_error = ibase_errmsg();
        die($conn_error);
    }

?>
```