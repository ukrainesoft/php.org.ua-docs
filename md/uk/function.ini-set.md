Встановлює налаштування конфігурації

-   [« inirestore](function.ini-restore.html)
    
-   [memorygetpeakusage »](function.memory-get-peak-usage.html)
    
-   [PHP Manual](index.md)
    
-   [Опції PHP/інформаційні функції](ref.info.md)
    
-   Встановлює налаштування конфігурації
    

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
echo ini_get('display_errors');

if (!ini_get('display_errors')) {
    ini_set('display_errors', '1');
}

echo ini_get('display_errors');
?>
```

### Дивіться також

-   [getcfgvar()](function.get-cfg-var.html) - Витягує значення налаштування конфігурації PHP
-   [iniget()](function.ini-get.html) - Отримує значення налаштування конфігурації
-   [inigetall()](function.ini-get-all.html) - Отримує всі налаштування конфігурації
-   [inirestore()](function.ini-restore.html) - Відновлює налаштування конфігурації.
-   [Як змінити налаштування конфігурації](configuration.changes.md)