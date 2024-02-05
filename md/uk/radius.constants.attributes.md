---
navigation:
  - radius.constants.packets.md: типи пакетів RADIUS
  - radius.constants.vendor-specific.md: Атрибути RADIUS специфічні для різних виробників.
  - index.md: PHP Manual
  - radius.constants.md: Обумовлені константи
title: Типи атрибутів RADIUS
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Типи атрибутів RADIUS

Ці константи описують типи атрибутів RADIUS, які можна використовувати у функціях [radius\_put\_addr()](function.radius-put-addr.md) [radius\_put\_attr()](function.radius-put-attr.md) [radius\_put\_int()](function.radius-put-int.md) і [radius\_put\_string()](function.radius-put-string.md)

**`RADIUS_USER_NAME`**(int)

Атрибут User-Name. Повинен бути типу string і містити ім'я користувача, що автентифікується. Атрибут можна встановити функцією [radius\_put\_attr()](function.radius-put-attr.md)

**`RADIUS_USER_PASSWORD`**(int)

Атрибут User-Password. Має бути типу string і містити пароль користувача. Атрибут можна встановити функцією [radius\_put\_attr()](function.radius-put-attr.md). Це значення буде обфусковано при передачі згідно [» секції 5.2 RFC 2865](http://www.faqs.org/rfcs/rfc2865)

**`RADIUS_CHAP_PASSWORD`**(int)

Атрибут Chap-Password. Має бути типу string і містити ідентифікатор CHAP користувача, 16 байт, що містять MD5-хеш ідентифікатора CHAP, текстове представлення пароля та перевірочне значення CHAP з'єднаними в один рядок. Зверніть увагу, що перевірочне значення CHAP також має бути надіслано окремо в атрибуті [**`RADIUS_CHAP_CHALLENGE`**](radius.constants.attributes.md#constant.radius-chap-challenge)

**Приклад #1 Використання паролів CHAP**

```php
<?php
// Для начала создадим обработчик аутентификации и запрос.
$radh = radius_auth_open();
radius_add_server($radh, $server, $port, $secret, 3, 3);
radius_create_request($radh, RADIUS_ACCESS_REQUEST);

// Считая, что $password содержит пароль в незашифрованном виде, мы делаем:

// Создаём проверочное значение.
$challenge = mt_rand();

// Задаём идентификатор CHAP.
$ident = 1;

// Добавляем атрибут Chap-Password.
$cp = md5(pack('Ca*', $ident, $password.$challenge), true);
radius_put_attr($radh, RADIUS_CHAP_PASSWORD, pack('C', $ident).$cp);

// Добавляем атрибут Chap-Challenge.
radius_put_attr($radh, RADIUS_CHAP_CHALLENGE, $challenge);

/* Теперь можно добавлять прочие необходимые аттриубты
 * и вызывать radius_send_request(). */
?>
```

**`RADIUS_NAS_IP_ADDRESS`**(int)

Атрибут NAS IP-Address. Очікується, що значення буде IP адресою клієнта RADIUS у вигляді цілого числа. Атрибут встановлюється функцією [radius\_put\_addr()](function.radius-put-addr.md)

**`RADIUS_NAS_PORT`**(int)

Атрибут NAS-Port. Очікується, що значення буде фізичним портом клієнта RADIUS як цілого числа. Атрибут встановлюється функцією [radius\_put\_addr()](function.radius-put-addr.md)

**`RADIUS_SERVICE_TYPE`**(int)

Атрибут Service-Type. Значення атрибута позначає тип сервісу запитуваного клієнтом, має бути цілим числом. Атрибут встановлюється функцією [radius\_put\_addr()](function.radius-put-addr.md)

Допустимі такі значення:

-   **`RADIUS_LOGIN`**
-   **`RADIUS_FRAMED`**
-   **`RADIUS_CALLBACK_LOGIN`**
-   **`RADIUS_CALLBACK_FRAMED`**
-   **`RADIUS_OUTBOUND`**
-   **`RADIUS_ADMINISTRATIVE`**
-   **`RADIUS_NAS_PROMPT`**
-   **`RADIUS_AUTHENTICATE_ONLY`**
-   **`RADIUS_CALLBACK_NAS_PROMPT`**

**`RADIUS_FRAMED_PROTOCOL`**(int)

Атрибут Framed-Protocol. Атрибут повинен бути цілим числом, що означає протокол обгортку. Атрибут встановлюється функцією [radius\_put\_addr()](function.radius-put-addr.md). Допустимі значення:

-   **`RADIUS_PPP`**
-   **`RADIUS_SLIP`**
-   **`RADIUS_ARAP`**
-   **`RADIUS_GANDALF`**
-   **`RADIUS_XYLOGICS`**

**`RADIUS_FRAMED_IP_ADDRESS`**(int)

Атрибут Framed-IP-Address. Атрибут повинен містити адресу мережі користувача у вигляді цілого числа. Атрибут встановлюється функцією [radius\_put\_addr()](function.radius-put-addr.md) та витягується функцією [radius\_cvt\_addr()](function.radius-cvt-addr.md)

**`RADIUS_FRAMED_IP_NETMASK`**(int)

Атрибут Framed-IP-Netmask. Атрибут повинен містити маску мережі користувача у вигляді цілого числа. Атрибут встановлюється функцією [radius\_put\_addr()](function.radius-put-addr.md) та витягується функцією [radius\_cvt\_addr()](function.radius-cvt-addr.md)

**`RADIUS_FRAMED_ROUTING`**(int)

Атрибут Framed-Routing. Атрибут має бути цілим числом та містити метод маршрутизації. Атрибут встановлюється функцією [radius\_put\_addr()](function.radius-put-addr.md)

Допустимі значення:

-   : Без маршрутизації
-   : Посилання пакетів маршрутизації
-   : Чекати на пакети маршрутизації.
-   `3`: Посилати та чекати

**`RADIUS_FILTER_ID`**(int)

Атрибут Filter-ID. Атрибут повинен бути залежним від реалізації, людино-читаним рядком фільтрів. Атрибут встановлюється функцією [radius\_put\_addr()](function.radius-put-addr.md)

**`RADIUS_FRAMED_MTU`**(int)

Атрибут Framed-MTU. Ціле число, що означає значення MTU. Атрибут встановлюється функцією [radius\_put\_addr()](function.radius-put-addr.md)

**`RADIUS_FRAMED_COMPRESSION`**(int)

Атрибут Framed-Compression. Ціле число, що означає протокол стиснення. Атрибут встановлюється функцією [radius\_put\_addr()](function.radius-put-addr.md) Допустимі значення:

-   **`RADIUS_COMP_NONE`**: Без стиску
-   **`RADIUS_COMP_VJ`**: Стиснення заголовків VJ TCP/IP
-   **`RADIUS_COMP_IPXHDR`**: Стиснення заголовків IPX
-   **`RADIUS_COMP_STAC_LZS`**: Стиснення Stac-LZS (додано в PECL radius 1.3.0b2)

**`RADIUS_LOGIN_IP_HOST`**(int)

Атрибут Login-IP-Host. Ціле число, що представляє IP-адресу, з якою з'єднується користувач. Атрибут встановлюється функцією [radius\_put\_addr()](function.radius-put-addr.md)

**`RADIUS_LOGIN_SERVICE`**(int)

Атрибут Login-Service Значення атрибута означає послугу, з якою користувач з'єднується на сервері автентифікації. Це значення можна перетворити на ціле число PHP за допомогою функції [radius\_cvt\_int()](function.radius-cvt-int.md)

**`RADIUS_LOGIN_TCP_PORT`**(int)

Атрибут Login-TCP-Port. Атрибут означає порт, з яким користувач з'єднується на сервері автентифікації. Це значення можна перетворити на ціле число PHP за допомогою функції [radius\_cvt\_int()](function.radius-cvt-int.md)

**`RADIUS_REPLY_MESSAGE`**(int)

Атрибут Reply-Message. Значення атрибута містить текст, який можна показати користувачеві у відповідь на запит автентифікації.

**`RADIUS_CALLBACK_NUMBER`**(int)

Атрибути Callback-Number. Атрибут містить рядок, який можна використовувати як зворотний дзвінок.

**`RADIUS_CALLBACK_ID`**(int)

Атрибут Callback-Id. Рядок, що містить ім'я викликаного методу специфічного для конкретної реалізації.

**`RADIUS_FRAMED_ROUTE`**(int)

Атрибут Framed-Route. Рядок, що містить список маршрутів, що залежить від реалізації, сконфігурованих для користувача.

**`RADIUS_FRAMED_IPX_NETWORK`**(int)

Атрибут Framed-IPX-Network. Ціле число, що визначає мережу IPX, налаштовану для користувача або `0xFFFFFFFE`що закликає клієнта RADIUS вибрати мережу самостійно. Можна витягти за допомогою [radius\_cvt\_int()](function.radius-cvt-int.md)

**`RADIUS_STATE`**(int)

Атрибут State. Рядок, що залежить від реалізації, включений у відповідь Access-Challenge прийшов від сервера, яку необхідно включити в наступний запит Access-Request. Повинен встановлюватись функцією [radius\_put\_attr()](function.radius-put-attr.md)

**`RADIUS_CLASS`**(int)

Атрибут Class. Довільний рядок включений у повідомлення Access-Accept і який має бути надісланий серверу облікових даних у запиті Accounting-Request. Повинен встановлюватись функцією [radius\_put\_attr()](function.radius-put-attr.md)

**`RADIUS_VENDOR_SPECIFIC`**(int)

Атрибут Vendor-Specific. Загалом значення цього атрибуту повинні встановлюватися з використанням функцій [radius\_put\_vendor\_addr()](function.radius-put-vendor-addr.md) [radius\_put\_vendor\_attr()](function.radius-put-vendor-attr.md) [radius\_put\_vendor\_int()](function.radius-put-vendor-int.md) і [radius\_put\_vendor\_string()](function.radius-put-vendor-string.md), а чи не безпосередньо.

Ці константи необхідні інтерпретації специфічних, які від виробника атрибутів, які у відповідях сервера RADIUS; коли отримані такі атрибути, потрібно використовувати функцію [radius\_get\_vendor\_attr()](function.radius-get-vendor-attr.md) для вилучення ідентифікатора вендора, типу атрибута та його значення.

**`RADIUS_SESSION_TIMEOUT`**(int)

Час очікування сесії

**`RADIUS_IDLE_TIMEOUT`**(int)

Час очікування простою

**`RADIUS_TERMINATION_ACTION`**(int)

Припинення операції

**`RADIUS_CALLED_STATION_ID`**(int)

Ідентифікатор станції, що викликається

**`RADIUS_CALLING_STATION_ID`**(int)

Ідентифікатор зухвалої станції

**`RADIUS_NAS_IDENTIFIER`**(int)

NAS ID

**`RADIUS_PROXY_STATE`**(int)

Стан проксі

**`RADIUS_LOGIN_LAT_SERVICE`**(int)

Сервіс входу до системи LAT

**`RADIUS_LOGIN_LAT_NODE`**(int)

Вузол входу до системи LAT

**`RADIUS_LOGIN_LAT_GROUP`**(int)

Група входу до системи LAT

**`RADIUS_FRAMED_APPLETALK_LINK`**(int)

Framed Appletalk Link

**`RADIUS_FRAMED_APPLETALK_NETWORK`**(int)

Framed Appletalk Network

**`RADIUS_FRAMED_APPLETALK_ZONE`**(int)

Framed Appletalk Zone

**`RADIUS_CHAP_CHALLENGE`**(int)

Перевірочне значення

**`RADIUS_NAS_PORT_TYPE`**(int)

Тип порту NAS, одна з констант:

-   **`RADIUS_ASYNC`**
-   **`RADIUS_SYNC`**
-   **`RADIUS_ISDN_SYNC`**
-   **`RADIUS_ISDN_ASYNC_V120`**
-   **`RADIUS_ISDN_ASYNC_V110`**
-   **`RADIUS_VIRTUAL`**
-   **`RADIUS_PIAFS`**
-   **`RADIUS_HDLC_CLEAR_CHANNEL`**
-   **`RADIUS_X_25`**
-   **`RADIUS_X_75`**
-   **`RADIUS_G_3_FAX`**
-   **`RADIUS_SDSL`**
-   **`RADIUS_ADSL_CAP`**
-   **`RADIUS_ADSL_DMT`**
-   **`RADIUS_IDSL`**
-   **`RADIUS_ETHERNET`**
-   **`RADIUS_XDSL`**
-   **`RADIUS_CABLE`**
-   **`RADIUS_WIRELESS_OTHER`**
-   **`RADIUS_WIRELESS_IEEE_802_11`**

**`RADIUS_PORT_LIMIT`**(int)

Обмеження на порти

**`RADIUS_LOGIN_LAT_PORT`**(int)

Порт входу до системи LAT

**`RADIUS_CONNECT_INFO`**(int)

Інформація про з'єднання

**`RADIUS_ACCT_STATUS_TYPE`**(int)

Статус системи управління обліковими даними, одна з констант:

-   **`RADIUS_START`**
-   **`RADIUS_STOP`**
-   **`RADIUS_ACCOUNTING_ON`**
-   **`RADIUS_ACCOUNTING_OFF`**

**`RADIUS_ACCT_DELAY_TIME`**(int)

Час затримки системи керування обліковими даними

**`RADIUS_ACCT_INPUT_OCTETS`**(int)

Вхідні байти до системи управління обліковими даними

**`RADIUS_ACCT_OUTPUT_OCTETS`**(int)

Вихідні байти із системи управління обліковими даними

**`RADIUS_ACCT_SESSION_ID`**(int)

Ідентифікатор сесії системи управління обліковими даними

**`RADIUS_ACCT_AUTHENTIC`**(int)

Тип системи управління обліковими даними, одна з констант:

-   **`RADIUS_AUTH_RADIUS`**
-   **`RADIUS_AUTH_LOCAL`**
-   **`RADIUS_AUTH_REMOTE`**

**`RADIUS_ACCT_SESSION_TIME`**(int)

Час сесії у системі управління обліковими даними

**`RADIUS_ACCT_INPUT_PACKETS`**(int)

Вхідні пакети до системи управління обліковими даними

**`RADIUS_ACCT_OUTPUT_PACKETS`**(int)

Вихідні пакети із системи управління обліковими даними

**`RADIUS_ACCT_TERMINATE_CAUSE`**(int)

Аварійне завершення сеансу управління обліковими даними:

-   **`RADIUS_TERM_USER_REQUEST`**
-   **`RADIUS_TERM_LOST_CARRIER`**
-   **`RADIUS_TERM_LOST_SERVICE`**
-   **`RADIUS_TERM_IDLE_TIMEOUT`**
-   **`RADIUS_TERM_SESSION_TIMEOUT`**
-   **`RADIUS_TERM_ADMIN_RESET`**
-   **`RADIUS_TERM_ADMIN_REBOOT`**
-   **`RADIUS_TERM_PORT_ERROR`**
-   **`RADIUS_TERM_NAS_ERROR`**
-   **`RADIUS_TERM_NAS_REQUEST`**
-   **`RADIUS_TERM_NAS_REBOOT`**
-   **`RADIUS_TERM_PORT_UNNEEDED`**
-   **`RADIUS_TERM_PORT_PREEMPTED`**
-   **`RADIUS_TERM_PORT_SUSPENDED`**
-   **`RADIUS_TERM_SERVICE_UNAVAILABLE`**
-   **`RADIUS_TERM_CALLBACK`**
-   **`RADIUS_TERM_USER_ERROR`**
-   **`RADIUS_TERM_HOST_REQUEST`**

**`RADIUS_ACCT_MULTI_SESSION_ID`**(int)

Багатосесійний ідентифікатор системи управління обліковими даними

**`RADIUS_ACCT_LINK_COUNT`**(int)

Кількість з'єднань системи управління обліковими даними
