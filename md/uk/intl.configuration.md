---
navigation:
  - intl.installation.md: « Встановлення
  - intl.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - intl.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Intl**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [intl.default\_locale](intl.configuration.md#ini.intl.default-locale) |  | **`INI_ALL`** |  |
| [intl.error\_level](intl.configuration.md#ini.intl.error-level) |  | **`INI_ALL`** |  |
| [intl.use\_exceptions](intl.configuration.md#ini.intl.use-exceptions) |  | **`INI_ALL`** | Доступно з PECL 3.0.0a1 |

Коротке пояснення конфігураційних директив.

`intl.default_locale`string

Локаль за замовчуванням для використання у функціях у випадках, коли відповідні параметри будуть опущені, або задані як `NULL`. Це локаль ICU, а чи не системна. Вбудовані локалі ICU та їх дані можна переглянути за посиланням [» https://icu4c-demos.unicode.org/icu-bin/locexp](https://icu4c-demos.unicode.org/icu-bin/locexp)

За промовчанням значення порожнє, що веде до примусового використання локалі ICU за умовчанням. Одного разу задавши це значення, його вже не можна буде скинути на початкове. Не рекомендується використовувати локаль ICU за умовчанням, оскільки вона залежить від локалі оточення сервера.

`intl.error_level`int

Тип повідомлень про помилки, що генеруються при їх виникненні у функціях ICU. Задається як [рівень помилок PHP](errorfunc.constants.md), таких как\*\*`E_WARNING`\*\*. Можна встановити рівним якщо взагалі не хочете бачити повідомлення про помилки. Дана настройка не впливає на значення функцій, що повертаються, у разі помилок і результат виконання [intl\_get\_error\_code()](function.intl-get-error-code.md) та специфічних для класів методів, які повертають інформацію про помилки.

По умолчанию равно

`intl.use_exceptions`int

Если установлено как\*\*`true`\*\*, то замість помилок викидатимуться винятки класу [IntlException](class.intlexception.md). Можна використовувати на додаток до [intl.error\_level](intl.configuration.md#ini.intl.error-level)

по умолчанию равно\*\*`false`\*\*
