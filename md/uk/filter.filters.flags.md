---
navigation:
  - filter.filters.misc.md: « Інші фільтри
  - filter.constants.md: Обумовлені константи »
  - index.md: PHP Manual
  - filter.filters.md: Типи фільтрів
title: Прапори для фільтрів
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Прапори для фільтрів

**Список прапорів для фільтрів**

| Идентификатор | Совместимый фильтр | Опис |
| --- | --- | --- |
| **`FILTER_FLAG_STRIP_LOW`** | **`FILTER_SANITIZE_ENCODED`** **`FILTER_SANITIZE_SPECIAL_CHARS`** **`FILTER_SANITIZE_STRING`** **`FILTER_UNSAFE_RAW`** | Видаляє символи, які мають код < 32. |
| **`FILTER_FLAG_STRIP_HIGH`** | **`FILTER_SANITIZE_ENCODED`** **`FILTER_SANITIZE_SPECIAL_CHARS`** **`FILTER_SANITIZE_STRING`** **`FILTER_UNSAFE_RAW`** | Видаляє символи, які мають код > 127. |
| **`FILTER_FLAG_STRIP_BACKTICK`** | **`FILTER_SANITIZE_ENCODED`** **`FILTER_SANITIZE_SPECIAL_CHARS`** **`FILTER_SANITIZE_STRING`** **`FILTER_UNSAFE_RAW`** | Видаляє символи зворотної лапки (\` |
| **`FILTER_FLAG_ALLOW_FRACTION`** | **`FILTER_SANITIZE_NUMBER_FLOAT`** | Дозволяє точку ( ) як десятковий роздільник у числах. |
| **`FILTER_FLAG_ALLOW_THOUSAND`** | **`FILTER_SANITIZE_NUMBER_FLOAT`** **`FILTER_VALIDATE_FLOAT`** | Дозволяє кому (`,`) як роздільник тисяч у числах. |
| **`FILTER_FLAG_ALLOW_SCIENTIFIC`** | **`FILTER_SANITIZE_NUMBER_FLOAT`** | Дозволяє літери `e`и`E` для запису чисел у науковій нотації. |
| **`FILTER_FLAG_NO_ENCODE_QUOTES`** | **`FILTER_SANITIZE_STRING`** | При встановленні цього прапора одинарні (`'`) та подвійні (`"`) лапки кодуватись не будуть. |
| **`FILTER_FLAG_ENCODE_LOW`** | **`FILTER_SANITIZE_ENCODED`** **`FILTER_SANITIZE_STRING`** **`FILTER_UNSAFE_RAW`** | Кодує символи, які мають код < 32. |
| **`FILTER_FLAG_ENCODE_HIGH`** | **`FILTER_SANITIZE_ENCODED`** **`FILTER_SANITIZE_SPECIAL_CHARS`** **`FILTER_SANITIZE_STRING`** **`FILTER_UNSAFE_RAW`** | Кодує символи, які мають код > 127. |
| **`FILTER_FLAG_ENCODE_AMP`** | **`FILTER_SANITIZE_STRING`** **`FILTER_SANITIZE_RAW`** | Кодує амперсанди (`&` |
| **`FILTER_NULL_ON_FAILURE`** | будь-який [**`FILTER_VALIDATE_*`**](filter.filters.validate.md) | Повертає **`null`** для нерозпізнаних значень. |
| **`FILTER_FLAG_ALLOW_OCTAL`** | **`FILTER_VALIDATE_INT`** | Трактує вхідні дані, що починаються з нуля ( ), як вісімкові числа. Після нуля можна вказувати лише числа в діапазоні `0-7` |
| **`FILTER_FLAG_ALLOW_HEX`** | **`FILTER_VALIDATE_INT`** | Трактує вхідні дані, що починаються з літералу `0x`или`0X`як шістнадцяткові числа. Після літералу можна вказувати лише символи в діапазоні `a-fA-F0-9` |
| **`FILTER_FLAG_EMAIL_UNICODE`** | **`FILTER_VALIDATE_EMAIL`** | Дозволяє у локальній частині, до символу @, email-адреси Unicode-символи. |
| **`FILTER_FLAG_IPV4`** | **`FILTER_VALIDATE_IP`** | Дозволяє формат IPv4 для IP-адреси. |
| **`FILTER_FLAG_IPV6`** | **`FILTER_VALIDATE_IP`** | Дозволяє формат IPv6 для IP-адреси. |
| **`FILTER_FLAG_NO_PRIV_RANGE`** | **`FILTER_VALIDATE_IP`** |  |
| Забороняє успішну перевірку для наступних приватних IPv4-діапазонів: `10.0.0.0/8` `172.16.0.0/12`и`192.168.0.0/16` |  |  |

Забороняє успішну перевірку для IPv6-адрес, що починаються з `FD`или`FC`

**`FILTER_FLAG_NO_RES_RANGE`** **`FILTER_VALIDATE_IP`**

Забороняє успішну перевірку для наступних зарезервованих IPv4-діапазонів: `0.0.0.0/8` `169.254.0.0/16` `127.0.0.0/8`и`240.0.0.0/4`

Забороняє успішну перевірку для зарезервованих IPv6-діапазонів: `::1/128` `::/128` `::ffff:0:0/96`и`fe80::/10`

Це діапазони, які у стандарті [» RFC 6890](http://www.faqs.org/rfcs/rfc6890) відзначені як зарезервовані за протоколом (Reserved-By-Protocol).

**`FILTER_FLAG_GLOBAL_RANGE`** **`FILTER_VALIDATE_IP`**

Забороняє успішну перевірку для неглобальних IPv4- та IPv6-діапазонів з атрибутом `Global`, рівним `False`, как указано в стандарте[» RFC 6890](http://www.faqs.org/rfcs/rfc6890)

**`FILTER_FLAG_SCHEME_REQUIRED`** **`FILTER_VALIDATE_URL`** | Потрібно, щоб URL містив схему. | | **`FILTER_FLAG_HOST_REQUIRED`** **`FILTER_VALIDATE_URL`** | Потрібно, щоб URL містив хост. | | **`FILTER_FLAG_PATH_REQUIRED`** **`FILTER_VALIDATE_URL`** | Вимагає, щоб URL містив шлях. | | **`FILTER_FLAG_QUERY_REQUIRED`** **`FILTER_VALIDATE_URL`** | Вимагає, щоб URL-адреса містила рядок запиту. | | **`FILTER_REQUIRE_SCALAR`** | | Потребує, щоб значення було скаляром. | | **`FILTER_REQUIRE_ARRAY`** | | Потребує, щоб значення було масивом. Фільтр буде застосовано до кожного скалярного запису масиву. | | **`FILTER_FORCE_ARRAY`** | | Якщо значення скаляр, воно обробляється як масив з єдиним скалярним значенням. |

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Добавлена константа\*\*`FILTER_FLAG_GLOBAL_RANGE`\*\* як прапор для **`FILTER_VALIDATE_IP`** |
| 7.3.0 | Явна передача прапорів **`FILTER_FLAG_SCHEME_REQUIRED`** і **`FILTER_FLAG_HOST_REQUIRED`** оголошено застарілою. |
| 7.1.0 | Доданий прапор **`FILTER_FLAG_EMAIL_UNICODE`** |
