---
navigation:
  - function.apache-lookup-uri.md: « apache\_lookup\_uri
  - function.apache-request-headers.md: apache\_request\_headers »
  - index.md: PHP Manual
  - ref.apache.md: Функції Apache
title: apache\_note
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# apache\_note

(PHP 4, PHP 5, PHP 7, PHP 8)

apache\_note — Повертає та встановлює повідомлення до запиту Apache

### Опис

```methodsynopsis
apache_note(string $note_name, ?string $note_value = null): string|false
```

Ця функція є обгорткою для `table_get`и`table_set`. З її допомогою можна редагувати таблицю повідомлень (apache notes table), що створюється під час надсилання запиту. Таблиця сповіщень дозволяє модулям Apache обмінюватись даними.

Основное назначение**apache\_note()** - передавати інформацію з одного модуля до іншого всередині одного запиту.

### Список параметрів

`note_name`

Назва повідомлення.

`note_value`

Значення сповіщення.

### Значення, що повертаються

Якщо `note_value`опущен или\*\*`null`\*\*, функция возвращает текущее значение уведомления`note_name`. Інакше вона встановлює значення повідомлення `note_name`в`note_value` та повертає попереднє значення `note_name`. Якщо значення повідомлення не може бути отримано, буде повернено **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `note_value` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад передачі інформації між PHP та Perl**

```php
<?php

apache_note('name', 'Fredrik Ekengren');

// Вызов perl-скрипта
virtual("/perl/some_script.pl");

$result = apache_note("resultdata");
?>
```

\# Отримуємо об'єкт запиту Apache my $r = Apache->request()->main();

# Отримуємо передані дані

my $name = $r->notes('name');

# Деякі дії з даними

# Передача результату назад у PHP

$r->notes('resultdata', $result);

**Приклад #2 Приклад запису значень у access.log**

```php
<?php

apache_note('sessionID', session_id());

?>
```

\# "%{sessionID}n" може бути використаний у директиві LogFormat

### Дивіться також

-   [virtual()](function.virtual.md) \- Виконує підзапит Apache
