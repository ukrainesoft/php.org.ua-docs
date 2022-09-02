---
navigation:
  - function.apache-lookup-uri.md: « apachelookupuri
  - function.apache-request-headers.md: apacherequestheaders »
  - index.md: PHP Manual
  - ref.apache.md: Функции Apache
title: apachenote
---
# apachenote

(PHP 4, PHP 5, PHP 7, PHP 8)

apachenote — Повертає та встановлює повідомлення до запиту Apache

### Опис

```methodsynopsis
apache_note(string $note_name, ?string $note_value = null): string|false
```

Ця функція є обгорткою для `table_get` і `table_set`. З її допомогою можна редагувати таблицю повідомлень (apache notes table), що створюється під час надсилання запиту. Таблиця сповіщень дозволяє модулям Apache обмінюватись даними.

Основне призначення **apachenote()** - передавати інформацію з одного модуля до іншого всередині одного запиту.

### Список параметрів

`note_name`

Назва повідомлення.

`note_value`

Значення сповіщення.

### Значення, що повертаються

Якщо `note_value` опущений або **`null`**, функція повертає поточне значення сповіщення `note_name`. Інакше вона встановлює значення повідомлення `note_name` в `note_value` та повертає попереднє значення `note_name`. Якщо значення повідомлення не може бути отримано, буде повернено **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | `note_value` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад передачі інформації між PHP та Perl**

```php
<?php

apache_note('name', 'Fredrik Ekengren');

// Вызов perl-скрипта
virtual("/perl/some_script.pl");

$result = apache_note("resultdata");
?>
```

Отримуємо об'єкт запиту Apache my $r = Apache->request()->main();

# Отримуємо передані дані

my $name = $r->notes('name');

# Деякі дії з даними

# Передача результату назад у PHP

$r->notes('resultdata', $result);

**Приклад #2 Приклад запису значень у access.log**

```php
<?php

apache_note('sessionID', session_id());

?>
```

"%{sessionID}n" може бути використаний у директиві LogFormat

### Дивіться також

-   [virtual()](function.virtual.md) - Виконує підзапит Apache
