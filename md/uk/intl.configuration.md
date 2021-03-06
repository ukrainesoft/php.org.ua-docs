- [« Встановлення](intl.installation.md)
- [Типи ресурсів»](intl.resources.md)

- [PHP Manual](index.md)
- [Встановлення та налаштування](intl.setup.md)
- Налаштування під час виконання

## Налаштування під час виконання

Поведінка цих функцій залежить від установок `php.ini`.

| Ім'я За замовчуванням                                                | Місце зміни | Список змін |
| -------------------------------------------------------------------- | ----------- | ----------- |
| [intl.default_locale](intl.configuration.md#ini.intl.default-locale) |             | PHP_INI_ALL |
| [intl.error_level](intl.configuration.md#ini.intl.error-level)       | 0           | PHP_INI_ALL |
| [intl.use_exceptions](intl.configuration.md#ini.intl.use-exceptions) | 0           | PHP_INI_ALL | Доступно з PECL 3.0.0a1

**Опції налаштування Intl**

Коротке пояснення конфігураційних директив.

`intl.default_locale` string
Локаль за замовчуванням для використання у функціях у разі якщо
відповідні параметри будуть опущені або задані як `NULL`. Це
локаль ICU, а чи не системна. Вбудовані локалі ICU та їх дані можна
подивитися за посиланням
[»http://demo.icu-project.org/icu-bin/locexp](http://demo.icu-project.org/icu-bin/locexp).

За промовчанням значення порожнє, що веде до примусового використання
локалі ICU за замовчуванням. Одного разу поставивши це значення його вже не можна
скинутиме на початкове. Не рекомендується використовувати локаль ICU по
замовчуванням, оскільки вона залежить від локалі оточення сервера.

`intl.error_level` int
Рівень повідомлень про помилки, що генеруються при їх виникненні
функціях ICU. Визначається як рівень помилок PHP, таких як
**`E_WARNING`**. Можна встановити рівним `0`, якщо взагалі не хочете
бачити повідомлення про помилки. Ця установка не впливає на повертані
значення функцій у разі помилок та результат виконання
[intl_get_error_code()](function.intl-get-error-code.md) та специфічних
для класів методів, що повертають інформацію про помилки. Якщо обрано
рівень `E_ERROR`, то виконання скрипта буде перериватись у випадку
виникнення помилки.

За замовчуванням одно `0`.

`intl.use_exceptions` int
Якщо встановлено як **`true`**, то замість помилок викидатимуться
виняток класу [IntlException](class.intlexception.md). Можна, можливо
використовувати на додаток до
[intl.error_level](intl.configuration.md#ini.intl.error-level).

за умовчанням дорівнює **`false`**.
