---
navigation:
  - function.error-get-last.md: « error\_get\_last
  - function.error-reporting.md: error\_reporting »
  - index.md: PHP Manual
  - ref.errorfunc.md: Функції обробки помилок
title: error\_log
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# error\_log

(PHP 4, PHP 5, PHP 7, PHP 8)

error\_log — Надсилає повідомлення про помилку заданому обробнику помилок

### Опис

```methodsynopsis
error_log(    string $message,    int $message_type = 0,    ?string $destination = null,    ?string $additional_headers = null): bool
```

Надсилає повідомлення про помилку в лог веб-сервера або в файл користувача.

### Список параметрів

`message`

Повідомлення про помилку, яка має бути логована.

`message_type`

Визначає, куди відправляти помилку. Можливі такі значення:

<table class="doctable table"><caption><strong>Типи журналів <span class="function"><strong>error_log()</strong></span></strong></caption><tbody class="tbody"><tr><td>0</td><td>Повідомлення <code class="parameter">message</code> відправляється в системний реєстратор PHP, використовуючи механізм логування операційної системи, або файл, залежно від значення директиви <a href="errorfunc.configuration.md#ini.error-log" class="link">error_log</a> у конфігураційному файлі. Це значення за промовчанням.</td></tr><tr><td>1</td><td>Повідомлення <code class="parameter">message</code> надсилається електронною поштою на адресу, встановлену у параметрі <code class="parameter">destination</code>. Це єдиний тип повідомлення, де використовується четвертий параметр <code class="parameter">additional_headers</code>.</td></tr><tr><td>2</td><td>Більше не використовується.&lt; /td&gt;</td></tr><tr><td>3</td><td><code class="parameter">message</code> застосовується до зазначеного в <code class="parameter">destination</code> файлу. Перенесення рядка автоматично не додається до кінця <code class="parameter">message</code>.</td></tr><tr><td>4</td><td>Повідомлення <code class="parameter ">message</code> відправляється безпосередньо в обробник логера SAPI.</td></tr></tbody></table>

`destination`

Назначение. Устанавливается в зависимости от параметра`message_type`

`additional_headers`

Додаткові заголовки. Використовується, коли значення параметра `message_type` . Цей тип повідомлення використовує ту саму внутрішню функцію, що й [mail()](function.mail.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки. Если`message_type` дорівнює нулю, функція завжди повертає \*\*`true`\*\*незалежно від того, чи може помилка логуватися чи ні.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`destination`и`additional_headers` тепер допускають значення null. |

### Приклади

**Приклад #1 Приклади використання **error\_log()****

```php
<?php
// Отправляет уведомление посредством серверного лога, если мы не можем
// подключиться к базе данных.
if (!Ora_Logon($username, $password)) {
    error_log("База данных Oracle недоступна!", 0);
}

// Уведомить администратора по электронной почте, если невозможно выделить ресурсы для FOO
if (!($foo = allocate_new_foo())) {
    error_log("Большая проблема, мы выпали из FOO!", 1,
               "operator@example.com");
}

// другой способ вызвать error_log():
error_log("Вы ошиблись!", 3, "/var/tmp/my-errors.log");
?>
```

### Примітки

**Увага**

**error\_log()** не є бінарно-безпечною функцією . `message` обрізається за null-символом.

**Підказка**

`message` ні містити null-символ. Врахуйте, що `message` може передаватися у файл, поштою, syslog і т.д. Використовуйте відповідну перетворювальну або екрануючу функцію, [base64\_encode()](function.base64-encode.md) [rawurlencode()](function.rawurlencode.md) або [addslashes()](function.addslashes.md) перед викликом **error\_log()**
