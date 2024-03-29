---
navigation:
  - filter.filters.md: « Типи фільтрів
  - filter.filters.sanitize.md: 'Фільтри, що очищають »'
  - index.md: PHP Manual
  - filter.filters.md: Типи фільтрів
title: Фільтри валідації даних
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Фільтри валідації даних

**Список фільтрів валідації даних**

| Идентификатор | Имя | Параметры | Флаги | Опис |
| --- | --- | --- | --- | --- |
| **`FILTER_VALIDATE_BOOLEAN`** **`FILTER_VALIDATE_BOOL`** | "boolean" | `default` | **`FILTER_NULL_ON_FAILURE`** |  |
| Повертає **`true`** для значень "1", "true", "on" та "yes". Інакше повертає **`false`** |  |  |  |  |

Если установлен флаг\*\*`FILTER_NULL_ON_FAILURE`**, то**`false`\*\* повертається тільки для значень "0", "false", "off", "no" і "", а значення **`null`** буде повернутий для нелогічних значень.

Перед порівнянням строкові значення обрізаються функцією [trim()](function.trim.md)

**`FILTER_VALIDATE_DOMAIN`** | "validate\_domain" | `default` **`FILTER_FLAG_HOSTNAME`** **`FILTER_NULL_ON_FAILURE`**

Перевіряє, чи допустимі довжини міток доменного імені.

Перевіряє доменні імена на відповідність стандартам RFC 1034, RFC 1035, RFC 952, RFC 1123, RFC 2732, RFC 2181 та RFC 1123. Необов'язковий прапор **`FILTER_FLAG_HOSTNAME`** окремо перевіряє імена хостів (стандарти дозволяють іменам починатися з буквено-цифрового символу та містити лише буквено-цифрові символи або дефіси).

**`FILTER_VALIDATE_EMAIL`** | "validate\_email" | `default` **`FILTER_FLAG_EMAIL_UNICODE`** **`FILTER_NULL_ON_FAILURE`**

Перевіряє, чи є дійсна адреса електронної пошти.

Загалом перевіряє `addr-spec`\-синтаксис адреса на соответствие стандарту с[» RFC 822](http://www.faqs.org/rfcs/rfc822), за винятком того, що не підтримуються коментарі, плескання пробілів і доменні імена без точок.

**`FILTER_VALIDATE_FLOAT`** | "float" | `default` `decimal` `min_range` `max_range` **`FILTER_FLAG_ALLOW_THOUSAND`** **`FILTER_NULL_ON_FAILURE`**

Перевіряє значення на відповідність коректному числу з плаваючою точкою, і, якщо потрібно, входить у певний діапазон, у разі успішної перевірки перетворює число з плаваючою точкою.

Перед порівнянням строкові значення обрізаються функцією [trim()](function.trim.md)

**`FILTER_VALIDATE_INT`** | "int" | `default` `min_range` `max_range` **`FILTER_FLAG_ALLOW_OCTAL`** **`FILTER_FLAG_ALLOW_HEX`** **`FILTER_NULL_ON_FAILURE`**

Перевіряє значення на відповідність коректному цілого числа, і, якщо потрібно, входить у певний діапазон, у разі успішної перевірки перетворює на ціле число.

Перед порівнянням строкові значення обрізаються функцією [trim()](function.trim.md)

**`FILTER_VALIDATE_IP`** | "validate\_ip" | `default` **`FILTER_FLAG_IPV4`** **`FILTER_FLAG_IPV6`** **`FILTER_FLAG_NO_PRIV_RANGE`** **`FILTER_FLAG_NO_RES_RANGE`** **`FILTER_FLAG_GLOBAL_RANGE`** **`FILTER_NULL_ON_FAILURE`** | Перевіряє значення на відповідність коректній IP-адресі, і, якщо потрібно, то тільки для протоколів IPv4 або IPv6, а також те, чи адреса не входить в приватні або зарезервовані діапазони. | | **`FILTER_VALIDATE_MAC`** | "validate\_mac\_address" | `default` **`FILTER_NULL_ON_FAILURE`** | Перевіряє значення на відповідність коректній MAC-адресі. | | **`FILTER_VALIDATE_REGEXP`** | "validate\_regexp" | `default` `regexp` **`FILTER_NULL_ON_FAILURE`** | Перевіряє значення на відповідність регулярному виразу `regexp` [Perl-сумісному](book.pcre.md) регулярного вираження. | | **`FILTER_VALIDATE_URL`** | "validate\_url" | `default` **`FILTER_FLAG_SCHEME_REQUIRED`** **`FILTER_FLAG_HOST_REQUIRED`** **`FILTER_FLAG_PATH_REQUIRED`** **`FILTER_FLAG_QUERY_REQUIRED`** **`FILTER_NULL_ON_FAILURE`**| Проверяет значение на соответствие корректному URL-адресу (по правилам стандарта[» http://www.faqs.org/rfcs/rfc2396](http://www.faqs.org/rfcs/rfc2396)), якщо потрібно, з необхідними прапорами. Обережно, URL-адреса без протоколу `http://` визнається допустимим, тому іноді потрібна додаткова перевірка, яка визначить, чи використовує URL-адресу необхідний протокол, наприклад `ssh://`или`mailto:`. Функція визнає допустимими URL-адреси, які складаються лише із символів ASCII; Міжнародні доменні імена не пройдуть перевірку. |

> **Зауваження** :
> 
> Вместо значения, которое не прошло проверку, функция подставит значение по умолчанию, если в массиве параметров определена опция`default`

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Флаги\*\*`FILTER_FLAG_SCHEME_REQUIRED`** і **`FILTER_FLAG_HOST_REQUIRED`**для фільтра**`FILTER_VALIDATE_URL`\*\* були вилучені. Прапори `scheme`и`host` були та залишаються обов'язковими. |
| 8.0.0 | Добавлена константа\*\*`FILTER_VALIDATE_BOOL`\*\* як псевдонім **`FILTER_VALIDATE_BOOLEAN`**. . Краще віддати перевагу **`FILTER_VALIDATE_BOOL`** |
| 7.4.0 | Додані опції `min_range`и`max_range`для фільтра\*\*`FILTER_VALIDATE_FLOAT`\*\* |
| 7.0.0 | Доданий прапор **`FILTER_FLAG_HOSTNAME`** та фільтр **`FILTER_VALIDATE_DOMAIN`** |
