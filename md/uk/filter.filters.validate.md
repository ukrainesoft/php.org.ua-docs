Фільтри валідації даних

-   [« Типы фильтров](filter.filters.html)
    
-   [Очищающие фильтры »](filter.filters.sanitize.html)
    
-   [PHP Manual](index.html)
    
-   [Типы фильтров](filter.filters.html)
    
-   Фільтри валідації даних
    

## Фільтри валідації даних

**Список фільтрів валідації даних**

| Идентификатор                                                                           | Имя       | Параметры | Флаги                        | Описание |
|-----------------------------------------------------------------------------------------|-----------|-----------|------------------------------|----------|
| **`FILTER_VALIDATE_BOOLEAN`** **`FILTER_VALIDATE_BOOL`**                                | "boolean" | `default` | **`FILTER_NULL_ON_FAILURE`** |          |
| Повертає **`true`** для значень "1", "true", "on" та "yes". Інакше повертає **`false`** |           |           |                              |          |

Якщо встановлено прапор **`FILTER_NULL_ON_FAILURE`**, то **`false`** повертається тільки для значень "0", "false", "off", "no" та "", а **`null`** буде повернутий всім значень не логічного типу.

Перед порівнянням строкові значення обрізаються за допомогою функції [trim()](function.trim.html)

**`FILTER_VALIDATE_DOMAIN`** | "validatedomain" | `default` **`FILTER_FLAG_HOSTNAME`** **`FILTER_NULL_ON_FAILURE`**

Перевіряє, чи довжини міток імен домену коректні.

Перевіряє доменні імена на відповідність RFC 1034, RFC 1035, RFC 952, RFC 1123, RFC 2732, RFC 2181 та RFC 1123. Опціональний прапор **`FILTER_FLAG_HOSTNAME`** додає можливість спеціально перевіряти імена хостів (вони повинні починатися з літер, або цифр і містити лише літери, цифри та тире).

**`FILTER_VALIDATE_EMAIL`** | "validateemail" | `default` **`FILTER_FLAG_EMAIL_UNICODE`** **`FILTER_NULL_ON_FAILURE`**

Перевіряє, що значення є коректним електронною поштою.

Загалом відбувається перевірка `addr-spec`синтаксису адреси відповідно до [» RFC 822](http://www.faqs.org/rfcs/rfc822), за винятком того, що не підтримуються коментарі, плескання пробілів і доменні імена без крапок.

**`FILTER_VALIDATE_FLOAT`** | "float" | `default` `decimal` `min_range` `max_range` **`FILTER_FLAG_ALLOW_THOUSAND`** **`FILTER_NULL_ON_FAILURE`**

Перевіряє, що значення є коректним числом з плаваючою точкою, і, при необхідності, входить у певний діапазон, у разі успішної перевірки перетворює число з плаваючою точкою.

Перед порівнянням строкові значення обрізаються за допомогою функції [trim()](function.trim.html)

**`FILTER_VALIDATE_INT`** | "int" | `default` `min_range` `max_range` **`FILTER_FLAG_ALLOW_OCTAL`** **`FILTER_FLAG_ALLOW_HEX`** **`FILTER_NULL_ON_FAILURE`**

Перевіряє, що значення є коректним цілим числом, і, при необхідності, входить у певний діапазон, у разі успішної перевірки перетворює на ціле число.

Перед порівнянням строкові значення обрізаються за допомогою функції [trim()](function.trim.html)

**`FILTER_VALIDATE_IP`** | "validateip" | `default` **`FILTER_FLAG_IPV4`** **`FILTER_FLAG_IPV6`** **`FILTER_FLAG_NO_PRIV_RANGE`** **`FILTER_FLAG_NO_RES_RANGE`** **`FILTER_NULL_ON_FAILURE`** | Перевіряє, що значення є коректною IP-адресою, при необхідності лише для протоколів IPv4 або IPv6, а також відсутність входження до приватних або зарезервованих діапазонів. | | **`FILTER_VALIDATE_MAC`** | "validatemacaddress" | `default` **`FILTER_NULL_ON_FAILURE`** | Перевіряє, що значення - це коректна MAC-адреса. | | **`FILTER_VALIDATE_REGEXP`** | "validateregexp" | `default` `regexp` **`FILTER_NULL_ON_FAILURE`** | Перевіряє значення на відповідність `regexp` [Perl-совместимому](book.pcre.html) регулярного вираження. | | **`FILTER_VALIDATE_URL`** | "validateurl" | `default` **`FILTER_FLAG_SCHEME_REQUIRED`** **`FILTER_FLAG_HOST_REQUIRED`** **`FILTER_FLAG_PATH_REQUIRED`** **`FILTER_FLAG_QUERY_REQUIRED`** **`FILTER_NULL_ON_FAILURE`** | Перевіряє значення як URL (відповідно до [» http://www.faqs.org/rfcs/rfc2396](http://www.faqs.org/rfcs/rfc2396)), опціонально з необхідними компонентами. Пам'ятайте, що URL не містить ім'я протоколу `http://` є коректним, так що може знадобитися додаткова перевірка того, що URL-адреса використовує необхідний протокол, наприклад `ssh://` або `mailto:`. Зверніть увагу, що ця функція вважає коректними тільки URL-адреси, що складаються з символів ASCII; Міжнародні доменні імена не пройдуть перевірку. |

> **Зауваження**
> 
> Якщо заданий `default`, то значення `default` буде підставлено, якщо перевірка провалилася.

### список змін

| Версия | Описание                                                                                                                                                                       |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Константа **`FILTER_SANITIZE_STRING`** і **`FILTER_SANITIZE_STRIPPED`** оголошено застарілими.                                                                                 |
|        | Прапор **`FILTER_FLAG_SCHEME_REQUIRED`** **`FILTER_FLAG_HOST_REQUIRED`** і **`FILTER_VALIDATE_URL`** були вилучені. Прапори `scheme` і `host` є (і були) завжди обов'язковими. |
|        | Додано константу **`FILTER_VALIDATE_BOOL`** як псевдонім **`FILTER_VALIDATE_BOOLEAN`**. Переважно використовувати **`FILTER_VALIDATE_BOOL`**                                   |
|        | Додані опції `min_range` і `max_range` для **`FILTER_VALIDATE_FLOAT`**                                                                                                         |
|        | Додано константу **`FILTER_FLAG_HOSTNAME`** і **`FILTER_VALIDATE_DOMAIN`**                                                                                                     |