- [«error_get_last](function.error-get-last.md)
- [error_reporting »](function.error-reporting.md)

- [PHP Manual](index.md)
- [Функції обробки помилок](ref.errorfunc.md)
- Надсилає повідомлення про помилку заданому обробникові помилок

#error_log

(PHP 4, PHP 5, PHP 7, PHP 8)

error_log — Надсилає повідомлення про помилку заданому обробникові помилок

### Опис

**error_log**(
string `$message`,
int `$message_type` = 0,
?string `$destination` = **`null`**,
?string `$additional_headers` = **`null`**
): bool

Надсилає повідомлення про помилку в лог веб-сервера або в
файл.

### Список параметрів

`message`
Повідомлення про помилку, яка має бути логована.

`message_type`
Визначає куди надсилати помилку. Можливі такі значення:

|   |                                                                                                                                                                                                                                                                             |
|---|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 | Повідомлення message відправляється в системний реєстратор PHP, використовуючи механізм логування операційної системи або файл, залежно від значення директиви [error_log](errorfunc.configuration.md#ini.error-log) у конфігураційному файлі. Це значення за промовчанням. |
| 1 | Повідомлення message надсилається електронною поштою на адресу, встановлену в параметрі destination. Це єдиний тип повідомлення, де використовується четвертий параметр additional_headers.                                                                                 |
| 2 | Більше не використовується.                                                                                                                                                                                                                                                 |
| 3 | message застосовується до вказаного в destination файлу. Перенесення рядка автоматично не додається до кінця message.                                                                                                                                                       |
| 4 | Повідомлення message відправляється безпосередньо в обробник логера SAPI.                                                                                                                                                                                                   |

**Типи журналів **error_log()****

`destination`
Призначення. Встановлюється залежно від параметра `message_type`.

`additional_headers`
Додаткові заголовки. Використовується, коли значення параметра
`message_type` - `1`. Цей тип повідомлення використовує ту ж внутрішню
функцію, як і [mail()](function.mail.md).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки. Якщо `message_type` дорівнює нулю, функція
завжди повертає **`true`**, незалежно від того, чи може помилка
логуватися чи ні.

### Список змін

| Версія | Опис                                                                       |
|--------|----------------------------------------------------------------------------|
| 8.0.0  | Параметр destination та additional_headers тепер допускають значення null. |

### Приклади

**Приклад #1 Приклади використання **error_log()****

`<?php// Відправляє повідомлення через серверного лога, якщо ми не можемо підключитися до бази даних.if (! Ora_Logon ($ username, $ $)) // Уведомить администратора по электронной почте, если невозможно выделить ресурсы для FOOif (!($foo = allocate_new_foo())) {    error_log("Большая проблема, мы выпали из FOO!", 1,               "operator@example.com"); }// інший способ викликати error_log():error_log("Ви помилися!", 3, "/var/tmp/my-errors.log");?> `

### Примітки

**Увага**

**error_log()** не є бінарно-безпечною функцією. `message`
обрізається за null-символом.

**Підказка**

`message` не повинен утримувати null-символ. Врахуйте, що `message` може
передаватися у файл, поштою, syslog тощо. Використовуйте відповідну
перетворюючу або екрануючу функцію,
[base64_encode()](function.base64-encode.md),
[rawurlencode()](function.rawurlencode.md) або
[addslashes()](function.addslashes.md) перед викликом **error_log()**.
