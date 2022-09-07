---
navigation:
  - function.ibase-server-info.md: « ibaseserverinfo
  - function.ibase-service-detach.md: ibaseservicedetach »
  - index.md: PHP Manual
  - ref.ibase.md: Функции Firebird/InterBase
title: ibaseserviceattach
---
# ibaseserviceattach

(PHP 5, PHP 7 < 7.4.0)

ibaseserviceattach — Підключається до диспетчера служб

### Опис

```methodsynopsis
ibase_service_attach(string $host, string $dba_username, string $dba_password): resource|false
```

### Список параметрів

`host`

Ім'я або IP-адреса хоста бази даних. Ви можете вказати порт, додавши '/' та номер порту. Якщо порт не вказано, використовуватиметься порт 3050.

`dba_username`

Ім'я будь-якого дійсного користувача.

`dba_password`

Пароль користувача.

### Значення, що повертаються

Повертає ідентифікатор посилання Interbase / Firebird у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **ibaseserviceattach()****

```php
<?php
    // Присоединение к удаленному серверу Firebird по IP-адресу
    if (($service = ibase_service_attach('10.1.1.199', 'sysdba', 'masterkey')) != FALSE) {

        // Присоединение прошло успешно.
        // Возврат версии сервера (что-то вроде 'LI-V3.0.4.33054 Firebird 3.0')
        $server_version  = ibase_server_info($service, IBASE_SVC_SERVER_VERSION);

        // Возврат реализации сервера (что-то вроде 'Firebird/Linux/AMD/Intel/x64')
        $server_implementation = ibase_server_info($service, IBASE_SVC_IMPLEMENTATION);

        // Отсоединение от сервера (отключение)
        ibase_service_detach($service);

        // Вывод информации
        echo "Версия сервера: " . $server_version . "<br/>";
        echo "Реализация сервера: " . $server_implementation;
    }
    else {
        // Вывод сообщения в случае возникновения ошибки
        $conn_error = ibase_errmsg();
        die($conn_error);
    }

?>
```

**Приклад #2 Приклад використання **ibaseserviceattach()** із синтаксисом `hostname/port`**

```php
<?php
    // Присоединение к удаленному серверу Firebird по имени. Используется порт 3050.
    if (($service = ibase_service_attach('FB-SRV-01.contoso.local/3050', 'sysdba', 'masterkey')) != FALSE) {

        // Присоединение прошло успешно.
        // Возврат версии сервера (что-то вроде 'LI-V3.0.4.33054 Firebird 3.0')
        $server_version  = ibase_server_info($service, IBASE_SVC_SERVER_VERSION);

        // Возврат реализации сервера (что-то вроде 'Firebird/Linux/AMD/Intel/x64')
        $server_implementation = ibase_server_info($service, IBASE_SVC_IMPLEMENTATION);

        // Отсоединение от сервера (отключение)
        ibase_service_detach($service);

        // Вывод информации
        echo "Версия сервера: " . $server_version . "<br/>";
        echo "Реализация сервера: " . $server_implementation;
    }
    else {
        // Вывод сообщения в случае возникновения ошибки
        $conn_error = ibase_errmsg();
        die($conn_error);
    }

?>
```

### Дивіться також

-   [ibaseservicedetach()](function.ibase-service-detach.md) - відключається від диспетчера служб
