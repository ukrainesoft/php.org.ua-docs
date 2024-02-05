---
navigation:
  - function.ssh2-auth-pubkey-file.md: « ssh2\_auth\_pubkey\_file
  - function.ssh2-disconnect.md: ssh2\_disconnect »
  - index.md: PHP Manual
  - ref.ssh2.md: Функції SSH2
title: ssh2\_connect
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ssh2\_connect

(PECL ssh2 >= 0.9.0)

ssh2\_connect — Підключення до SSH-сервера

### Опис

```methodsynopsis
ssh2_connect(    string $host,    int $port = 22,    array $methods = ?,    array $callbacks = ?): resource|false
```

Встановлює з'єднання з сервером SSH.

После соединения, пользователь должен проверить ключ сервера, используя функцию[ssh2\_fingerprint()](function.ssh2-fingerprint.md), і після цього авторизуватись, використовуючи пароль або відкритий ключ.

### Список параметрів

`host`

`port`

`methods`

Параметр`methods` може бути асоціативним масивом, що містить до чотирьох записів, наведених нижче.

**Параметр`methods` може бути асоціативним масивом, що містить від одного до чотирьох параметрів**

| Индекс | Что обозначает | Допустимые значения\* |
| --- | --- | --- |
| kex | Список методів обміну ключами, розділених комою, як перевагу. | `diffie-hellman-group1-sha1` `diffie-hellman-group14-sha1`, и`diffie-hellman-group-exchange-sha1` |
| hostkey | Список методів ключів хоста, розділених комою, як перевагу. | `ssh-rsa`и`ssh-dss` |
| client\_to\_server | Асоціативний масив, що містить налаштування шифрування, стиснення та методу імітівставки ("message authentication code" або MAC) для повідомлень, надісланих клієнтом серверу. |  |
| server\_to\_client | Асоціативний масив, що містить налаштування шифрування, стиснення та методу імітівставки ("message authentication code" або MAC) для повідомлень, надісланих сервером клієнту. |  |

\* - Значення, що підтримуються, залежать від методів, що підтримуються базовою бібліотекою. Детальніше читайте документацію з [» libssh2](http://libssh2.org/)

**`client_to_server`и`server_to_client` можуть бути асоціативними масивами, що містять будь-який або всі нижчеперелічені параметри.**

| Индекс | Что обозначает | Допустимые значения\* |
| --- | --- | --- |
| crypt | Список методів шифрування, розділених комою, як перевагу. | `rijndael-cbc@lysator.liu.se` `aes256-cbc` `aes192-cbc` `aes128-cbc` `3des-cbc` `blowfish-cbc` `cast128-cbc` `arcfour`и`none**` |
| comp | Список методів стиснення, розділених комою, як перевагу. | `zlib`и`none` |
| mac | Список методів MAC, розділених комою, у порядку переваги. | `hmac-sha1` `hmac-sha1-96` `hmac-ripemd160` `hmac-ripemd160@openssh.com`и`none**` |

> **Зауваження** **Метод шифрування`none`і MAC**
> 
> В цілях безпеки `none` відключений у базовій бібліотеці [» libssh2](http://libssh2.org/), якщо ви не дозволили його самостійно на етапі збирання, використовуючи відповідні ключі ./configure. Дивіться документацію з базової бібліотеки для більш детальної інформації.

`callbacks`

`callbacks` може бути асоціативним масивом, що містить будь-який або всі нижчеперелічені параметри

**Параметри callback-функції**

| Индекс | Что обозначает | Прототип |
| --- | --- | --- |
| ignore | Ім'я функції, що викликається після отримання пакета **`SSH2_MSG_IGNORE`** | void ignore\_cb($message) |
| debug | Ім'я функції, що викликається після отримання пакета **`SSH2_MSG_DEBUG`** | void debug\_cb($message, $language, $always\_display) |
| macerror | Ім'я функції, що викликається, якщо пакет отримано, але MAC не вдався. Якщо callback-функція поверне **`true`**, розбіжність буде проігноровано, інакше з'єднання буде обірвано. | bool macerror\_cb($packet) |
| disconnect | Ім'я функції, що викликається після отримання пакета **`SSH2_MSG_DISCONNECT`** | void disconnect\_cb($reason, $message, $language) |

### Значення, що повертаються

Повертає ресурс у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример**ssh2\_connect()\*\*\*\*

Відкриємо з'єднання, примусово використовуючи такі налаштування: 3des-cbc під час відправлення пакетів, шифр aes будь-якої сили при отриманні пакетів, без стиснення в обох напрямках та обмін ключами Group1.

```php
<?php
/* Оповещаем пользователя, если сервер прервал соединение */
function my_ssh_disconnect($reason, $message, $language) {
  printf("Сервер отключился с кодом причины [%d] и сообщением: %s\n",
         $reason, $message);
}

$methods = array(
  'kex' => 'diffie-hellman-group1-sha1',
  'client_to_server' => array(
    'crypt' => '3des-cbc',
    'comp' => 'none'),
  'server_to_client' => array(
    'crypt' => 'aes256-cbc,aes192-cbc,aes128-cbc',
    'comp' => 'none'));

$callbacks = array('disconnect' => 'my_ssh_disconnect');

$connection = ssh2_connect('shell.example.com', 22, $methods, $callbacks);
if (!$connection) die('Не удалось установить соединение');
?>
```

### Дивіться також

-   [ssh2\_fingerprint()](function.ssh2-fingerprint.md) \- Отримання відбитка віддаленого сервера
-   [ssh2\_auth\_none()](function.ssh2-auth-none.md) - Аутентифікація як "none"
-   [ssh2\_auth\_password()](function.ssh2-auth-password.md) \- Аутентифікація через SSH із використанням звичайного пароля
-   [ssh2\_auth\_pubkey\_file()](function.ssh2-auth-pubkey-file.md) \- Аутентифікація з відкритим ключем
-   [ssh2\_disconnect()](function.ssh2-disconnect.md) \- Закрити з'єднання з віддаленим сервером SSH
