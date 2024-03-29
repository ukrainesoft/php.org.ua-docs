---
navigation:
  - function.oci-set-db-operation.md: « oci\_set\_db\_operation
  - function.oci-set-module-name.md: oci\_set\_module\_name »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_set\_edition
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_set\_edition

(PHP 5 >= 5.3.2, PHP 7, PHP 8, PECL OCI8 >= 1.4.0)

oci\_set\_edition - Задає випуск (edition) бази даних

### Опис

```methodsynopsis
oci_set_edition(string $edition): bool
```

Задає серію об'єктів для використання на нижчестоящих з'єднаннях.

Подібні "випуски" Oracle дозволяють запускати програми, що використовують однакові схеми та імена об'єктів у конкурентному режимі. Це може бути корисним при модернізації працюючих систем без їх відключення.

Викликайте **oci\_set\_edition()** до виклику [oci\_connect()](function.oci-connect.md) [oci\_pconnect()](function.oci-pconnect.md) або [oci\_new\_connect()](function.oci-new-connect.md)

Якщо заданий випуск неприпустимий у базі даних, з'єднання не встановлюватиметься, навіть якщо функція **oci\_set\_edition()** успішно виконається.

При використанні постійних з'єднань, якщо з'єднання з цим значенням серії вже існує, воно буде використано повторно. В інших випадках буде створюватись нове з'єднання.

### Список параметрів

`edition`

Ім'я "випуску" бази даних Oracle, раніше створене SQL командою "`CREATE EDITION`".

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Два скрипти можуть використовувати різні версії myfunc() одночасно**

```php
<?php

// Файл 1

echo "Версия приложения 1\n";

oci_set_edition('ORA$BASE');
$c = oci_connect('hr', 'welcome', 'localhost/XE');

$s = oci_parse($c, "begin :r := myfunc(); end;");
oci_bind_by_name($s, ":r", $r, 20);
oci_execute($s);
echo "Результат: $r\n";

?>
```

```php
<?php

// Файл 2

echo "Версия приложения 2\n";

oci_set_edition('E1');
$c = oci_connect('hr', 'welcome', 'localhost/XE');

$s = oci_parse($c, "begin :r := myfunc(); end;");
oci_bind_by_name($s, ":r", $r, 20);
oci_execute($s);
echo "Результат: $r\n";

?>
```

### Примітки

> **Зауваження** **Вимога до версії Oracle**
> 
> Ця функція доступна, починаючи з Oracle 11*g*R2.

**Застереження**

# Постійні з'єднання

Щоб уникнути несумісності та випадкових помилок, не використовуйте команду "ALTER SESSION SET EDITION" для зміни "серії" на постійних з'єднаннях.

**Застереження**

# DRCP об'єднання з'єднань у пул

Щоб уникнути несумісності та випадкових помилок при використанні серій та [DRCP](oci8.connection.md) в Oracle 11.2.0.1 дотримуйтесь однозначної відповідності між [oci8.connection\_class](oci8.configuration.md#ini.oci8.connection-class) та ім'ям "випуску", яким користуються додатки. Кожен сервер, що входить до складу пулу із заданим класом з'єднань, повинен використовуватися лише з одним "випуском". Це обмеження усунуто у версії Oracle 11.2.0.2.
