---
navigation:
  - function.ini-restore.md: « ini\_restore
  - function.memory-get-peak-usage.md: memory\_get\_peak\_usage »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: ini\_set
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ini\_set

(PHP 4, PHP 5, PHP 7, PHP 8)

ini\_set — Встановлює налаштування конфігурації

### Опис

```methodsynopsis
ini_set(string $option, string|int|float|bool|null $value): string|false
```

Встановлює значення налаштування конфігурації. Налаштування буде зберігати встановлене значення, поки виконується скрипт. Після завершення роботи скрипта значення налаштування повернеться до вихідного.

### Список параметрів

`option`

Не всі доступні установки можна змінювати функцією **ini\_set()**. Список доступних налаштувань наведено в [додатку](ini.list.md)

`value`

Нове значення налаштування.

### Значення, що повертаються

У разі успішного виконання повертає старе значення або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`value` тепер приймає будь-який скалярний тип (включаючи **`null`**). Раніше допускалися лише строкові (string) значення. |

### Приклади

**Приклад #1 Встановлення значення ini-налаштування**

```php
<?php
echo ini_get('display_errors');

if (!ini_get('display_errors')) {
    ini_set('display_errors', '1');
}

echo ini_get('display_errors');
?>
```

### Дивіться також

-   [get\_cfg\_var()](function.get-cfg-var.md) \- Витягує значення налаштування конфігурації PHP
-   [ini\_get()](function.ini-get.md) \- Отримує значення налаштування конфігурації
-   [ini\_get\_all()](function.ini-get-all.md) \- Отримує всі налаштування конфігурації
-   [ini\_restore()](function.ini-restore.md) \- Відновлює налаштування конфігурації.
-   [Як змінити налаштування конфігурації](configuration.changes.md)
