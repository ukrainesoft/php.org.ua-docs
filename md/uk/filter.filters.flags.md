---
navigation:
  - filter.filters.misc.md: « Інші фільтри
  - filter.constants.md: Обумовлені константи »
  - index.md: PHP Manual
  - filter.filters.md: Типи фільтрів
title: 'Прапори, що використовуються у фільтрах'
---
## Прапори, що використовуються у фільтрах

**Список прапорів, що використовуються у фільтрах**

| Идентификатор | Используется совместно с фильтром | Описание |
| --- | --- | --- |
| **`FILTER_FLAG_STRIP_LOW`** | **`FILTER_SANITIZE_ENCODED`** **`FILTER_SANITIZE_SPECIAL_CHARS`** **`FILTER_SANITIZE_STRING`** **`FILTER_UNSAFE_RAW`** | Видаляє символи, код яких <32. |
| **`FILTER_FLAG_STRIP_HIGH`** | **`FILTER_SANITIZE_ENCODED`** **`FILTER_SANITIZE_SPECIAL_CHARS`** **`FILTER_SANITIZE_STRING`** **`FILTER_UNSAFE_RAW`** | Видаляє символи, код яких >127. |
| **`FILTER_FLAG_STRIP_BACKTICK`** | **`FILTER_SANITIZE_ENCODED`** **`FILTER_SANITIZE_SPECIAL_CHARS`** **`FILTER_SANITIZE_STRING`** **`FILTER_UNSAFE_RAW`** | Видаляє символи зворотної лапки ( |
| **`FILTER_FLAG_ALLOW_FRACTION`** | **`FILTER_SANITIZE_NUMBER_FLOAT`** | Дозволяє наявність точки (`.`) як десятковий роздільник у числах. |
| **`FILTER_FLAG_ALLOW_THOUSAND`** | **`FILTER_SANITIZE_NUMBER_FLOAT`** **`FILTER_VALIDATE_FLOAT`** | Дозволяє наявність коми (`,`) як роздільник тисяч у числах. |
| **`FILTER_FLAG_ALLOW_SCIENTIFIC`** | **`FILTER_SANITIZE_NUMBER_FLOAT`** | Дозволяє наявність `e` і `E` для наукових нотацій чисел. |
| **`FILTER_FLAG_NO_ENCODE_QUOTES`** | **`FILTER_SANITIZE_STRING`** | При встановленні цього прапора одинарні (`'`) та подвійні (`"`) лапки кодуватись не будуть. |
| **`FILTER_FLAG_ENCODE_LOW`** | **`FILTER_SANITIZE_ENCODED`** **`FILTER_SANITIZE_STRING`** **`FILTER_SANITIZE_RAW`** | Кодує всі символи <32. |
| **`FILTER_FLAG_ENCODE_HIGH`** | **`FILTER_SANITIZE_ENCODED`** **`FILTER_SANITIZE_SPECIAL_CHARS`** **`FILTER_SANITIZE_STRING`** **`FILTER_SANITIZE_RAW`** | Кодує всі символи, код яких >127. |
| **`FILTER_FLAG_ENCODE_AMP`** | **`FILTER_SANITIZE_STRING`** **`FILTER_SANITIZE_RAW`** | Кодує амперсанд (`&` |
| **`FILTER_NULL_ON_FAILURE`** | будь-який [**`FILTER_VALIDATE_*`**](filter.filters.validate.md) | Повертає **`null`** для невідомих значень. |
| **`FILTER_FLAG_ALLOW_OCTAL`** | **`FILTER_VALIDATE_INT`** | Трактує введення, що починається з нуля (`0`) як вісімкове число. Для цього наступні числа мають бути в діапазоні `0-7` |
| **`FILTER_FLAG_ALLOW_HEX`** | **`FILTER_VALIDATE_INT`** | Трактує введення, що починається з `0x` або `0X` як шістнадцяткове число. Для цього наступні символи мають бути в діапазоні `a-fA-F0-9` |
| **`FILTER_FLAG_EMAIL_UNICODE`** | **`FILTER_VALIDATE_EMAIL`** | Дозволити символи Unicode у локальній частині email-адреси. |
| **`FILTER_FLAG_IPV4`** | **`FILTER_VALIDATE_IP`** | Дозволяє формат IPv4 для IP-адреси. |
| **`FILTER_FLAG_IPV6`** | **`FILTER_VALIDATE_IP`** | Дозволяє формат IPv6 для IP-адреси. |
| **`FILTER_FLAG_NO_PRIV_RANGE`** | **`FILTER_VALIDATE_IP`** |  |
| Забороняє успішне проходження перевірки для наступних приватних IPv4-діапазонів: `10.0.0.0/8` `172.16.0.0/12` і `192.168.0.0/16` |  |  |

Забороняє успішне проходження перевірки для IPv6-адрес, що починаються з `FD` або `FC`

**`FILTER_FLAG_NO_RES_RANGE`** **`FILTER_VALIDATE_IP`**

Забороняє успішне проходження перевірки для наступних зарезервованих IPv4-діапазонів: `0.0.0.0/8` `169.254.0.0/16` `127.0.0.0/8` і `240.0.0.0/4`

Забороняє перевірку для зарезервованих діапазонів IPv6: `::1/128` `::/128` `::ffff:0:0/96` і `fe80::/10`

Це діапазони, які позначені як зарезервовані за протоколом [» RFC 6890](http://www.faqs.org/rfcs/rfc6890)

**`FILTER_FLAG_SCHEME_REQUIRED`** **`FILTER_VALIDATE_URL`** | Потрібно, щоб URL містив частину зі схемою. | | **`FILTER_FLAG_HOST_REQUIRED`** **`FILTER_VALIDATE_URL`** | Вимагає, щоб URL містив частину з хостом. | | **`FILTER_FLAG_PATH_REQUIRED`** **`FILTER_VALIDATE_URL`** | Вимагає, щоб URL містив частину шляхом. | | **`FILTER_FLAG_QUERY_REQUIRED`** **`FILTER_VALIDATE_URL`** | Вимагає, щоб URL-адреса містила частину з рядком запиту. | | **`FILTER_REQUIRE_SCALAR`** | | Потребує, щоб значення було скалярним. | | **`FILTER_REQUIRE_ARRAY`** | | Потребує, щоб значення було масивом. | | **`FILTER_FORCE_ARRAY`** | | Якщо значення скалярне, воно буде розглядатися як масив з єдиним елементом з цим значенням. |

### список змін

| Версия | Описание |
| --- | --- |
|  | Явне використання **`FILTER_FLAG_SCHEME_REQUIRED`** і **`FILTER_FLAG_HOST_REQUIRED`** оголошено застарілим. |
|  | Додано константу **`FILTER_FLAG_EMAIL_UNICODE`** |
