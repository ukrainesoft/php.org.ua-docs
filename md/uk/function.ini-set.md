---
navigation:
  - function.ini-restore.md: « inirestore
  - function.memory-get-peak-usage.md: memorygetpeakusage »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: iniset
---
# iniset

(PHP 4, PHP 5, PHP 7, PHP 8)

iniset — Встановлює налаштування конфігурації

### Опис

```methodsynopsis
ini_set(string $option, string|int|float|bool|null $value): string|false
```

Встановлює значення налаштування конфігурації. Налаштування буде зберігати встановлене значення, поки виконується скрипт. Після завершення роботи скрипта значення налаштування повернеться до вихідного.

### Список параметрів

`option`

Не всі доступні установки можна змінювати функцією **iniset()**. Список доступних налаштувань наведено в [приложении](ini.list.md)

`value`

Нове значення налаштування.

### Значення, що повертаються

У разі успішного виконання повертає старе значення або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `value` тепер приймає будь-який скалярний тип (включаючи **`null`**). Раніше допускалися лише строкові (string) значення. |

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

-   [getcfgvar()](function.get-cfg-var.md) - Витягує значення налаштування конфігурації PHP
-   [iniget()](function.ini-get.md) - Отримує значення налаштування конфігурації
-   [inigetall()](function.ini-get-all.md) - Отримує всі налаштування конфігурації
-   [inirestore()](function.ini-restore.md) - Відновлює налаштування конфігурації.
-   [Як змінити налаштування конфігурації](configuration.changes.md)
