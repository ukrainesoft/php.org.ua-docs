- [« Установка](pcre.installation.md)
- [Типи ресурсів»](pcre.resources.md)

- [PHP Manual](index.md)
- [Встановлення та налаштування](pcre.setup.md)
- Налаштування під час виконання

## Налаштування під час виконання

Поведінка цих функцій залежить від установок `php.ini`.

| Ім'я За замовчуванням                                                  | Місце зміни | Список змін |
| ---------------------------------------------------------------------- | ----------- | ----------- |
| [pcre.backtrack_limit](pcre.configuration.md#ini.pcre.backtrack-limit) | "1000000"   | PHP_INI_ALL |
| [pcre.recursion_limit](pcre.configuration.md#ini.pcre.recursion-limit) | "100000"    | PHP_INI_ALL |
| [pcre.jit](pcre.configuration.md#ini.pcre.jit)                         | "1"         | PHP_INI_ALL |

**Опції конфігурації PCRE**

Для детального опису констант PHP_INI\_\*, зверніться до розділу [Де
можуть бути встановлені параметри конфігурації](configuration.changes.modes.md).

Коротке пояснення конфігураційних директив.

`pcre.backtrack_limit` int
Ліміт зворотних посилань PCRE. Для PHP \< 5.3.7 значення за замовчуванням
100 000.

`pcre.recursion_limit` int
Ліміт на рекурсію. Не забувайте про те, що якщо ви встановите достатньо
високе значення, то PCRE може перевищити розмір стека (встановлений
операційною системою) і врешті-решт викликає падіння PHP.

`pcre.jit` bool
Чи використовуватиметься JIT-компіляція PCRE.
