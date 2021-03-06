- [«ini_restore](function.ini-restore.md)
- [memory_get_peak_usage »](function.memory-get-peak-usage.md)

- [PHP Manual](index.md)
- [Опції PHP/інформаційні функції](ref.info.md)
- Встановлює значення налаштування конфігурації

#ini_set

(PHP 4, PHP 5, PHP 7, PHP 8)

ini_set — Встановлює налаштування конфігурації

### Опис

**ini_set**(string `$option`, string\|int\|float\|bool\|null `$value`):
string\|false

Встановлює значення заданої конфігурації. Налаштування буде
зберігати встановлене значення поки що виконується скрипт. Після завершення
роботи скрипта значення налаштування повернеться до вихідного.

### Список параметрів

`option`
Не всі доступні установки можна змінювати функцією **ini_set()**. перелік
доступних параметрів наведено в [програмі](ini.list.md).

`value`
Нове значення налаштування.

### Значення, що повертаються

У разі успішного виконання повертає старе значення або **`false`**
у разі виникнення помилки.

### Список змін

| Версія | Опис                                                                                                                           |
| ------ | ------------------------------------------------------------------------------------------------------------------------------ |
| 8.1.0  | Параметр value тепер приймає будь-який скалярний тип (включаючи **null**). Раніше допускалися лише строкові (string) значення. |

### Приклади

**Приклад #1 Встановлення значення ini-налаштування**

` <?phpecho ini_get('display_errors');if (!ini_get('display_errors')) {   ini_set('display_errors', '1');}echo ini_get('display_errors');?> `

### Дивіться також

- [get_cfg_var()](function.get-cfg-var.md) - Витягує значення
налаштування конфігурації PHP
- [ini_get()](function.ini-get.md) - Отримує значення налаштування
конфігурації
- [ini_get_all()](function.ini-get-all.md) - Отримує всі налаштування
конфігурації
- [ini_restore()](function.ini-restore.md) - Відновлює
значення налаштування конфігурації
- [Як змінити конфігураційні установки](configuration.changes.md)
