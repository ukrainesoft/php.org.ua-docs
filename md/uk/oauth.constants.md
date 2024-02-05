---
navigation:
  - oauth.resources.md: « Типи ресурсів
  - oauth.examples.md: Приклади »
  - index.md: PHP Manual
  - book.oauth.md: OAuth
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи визначені цим модулем і доступні або в збірках PHP з підтримкою цього модуля, або коли модуль динамічно завантажений під час виконання коду.

Більшість з цих констант торкаються проблем, зазначених у тому числі в офіційних [» повідомлення про проблеми](http://wiki.oauth.net/ProblemReporting) OAuth. Однак зауважте, що хоча ці імена констант і мають схожу схему імен, вони характерні тільки для PHP.

**`OAUTH_SIG_METHOD_RSASHA1`**(string)

Метод подписи OAuth*RSA-SHA1*

**`OAUTH_SIG_METHOD_HMACSHA1`**(string)

Метод подписи OAuth*HMAC-SHA1*

**`OAUTH_SIG_METHOD_HMACSHA256`**(string)

Метод подписи OAuth*HMAC-SHA256*

**`OAUTH_AUTH_TYPE_AUTHORIZATION`**(string)

Ця константа вказує на те, що OAuth параметри будуть поміщені в заголовок `Authorization`

**`OAUTH_AUTH_TYPE_NONE`**(string)

Ця константа означає NoAuth OAuth запит.

**`OAUTH_AUTH_TYPE_URI`**(string)

Ця константа вказує, що OAuth параметри буде розміщено в URI запиту. URI.

**`OAUTH_AUTH_TYPE_FORM`**(string)

Ця константа вказує на те, що OAuth параметри будуть поміщені в тіло HTTP POST запиту.

**`OAUTH_HTTP_METHOD_GET`**(string)

Константа вказує на використання *GET*метода для OAuth запроса.

**`OAUTH_HTTP_METHOD_POST`**(string)

Константа вказує на використання *POST*метода для OAuth запроса.

**`OAUTH_HTTP_METHOD_PUT`**(string)

Константа вказує на використання *PUT*метода для OAuth запроса.

**`OAUTH_HTTP_METHOD_HEAD`**(string)

Константа вказує на використання *HEAD*метода для OAuth запроса.

**`OAUTH_HTTP_METHOD_DELETE`**(string)

Константа вказує на використання *DELETE*метода для OAuth запроса.

**`OAUTH_REQENGINE_STREAMS`**(int)

Використовується методом [OAuth::setRequestEngine()](oauth.setrequestengine.md) Для вибору [потоків PHP](book.stream.md) як двигун, на противагу константі **`OAUTH_REQENGINE_CURL`**, що використовується для вибору [Curl](book.curl.md)

**`OAUTH_REQENGINE_CURL`**(int)

Використовується методом [OAuth::setRequestEngine()](oauth.setrequestengine.md) Для вибору [Curl](book.curl.md) як двигун, на противагу константі **`OAUTH_REQENGINE_STREAMS`**, що використовується для вибору [потоків PHP](book.stream.md)

**`OAUTH_OK`**(int)

Життя прекрасне.

**`OAUTH_BAD_NONCE`**(int)

Значение*oauth\_nonce* використовувалося у попередньому запиті, отже, не може бути використане зараз.

**`OAUTH_BAD_TIMESTAMP`**(int)

Значение*oauth\_timestamp* не було прийнято провайдером. У цьому випадку відповідь повинна також містити параметр *oauth\_acceptable\_timestamps*

**`OAUTH_CONSUMER_KEY_UNKNOWN`**(int)

*oauth\_consumer\_key* тимчасово недоступний провайдеру. Наприклад, якщо провайдер заблокував споживача.

**`OAUTH_CONSUMER_KEY_REFUSED`**(int)

Ключ споживача було відхилено.

**`OAUTH_INVALID_SIGNATURE`**(int)

Значение*oauth\_signature* недійсно, тому що не збігається з підписом, обчисленим провайдером.

**`OAUTH_TOKEN_USED`**(int)

*oauth\_token* було вжито. Він уже використовувався у попередньому запиті/запитах і більше не може бути використаний.

**`OAUTH_TOKEN_EXPIRED`**(int)

*oauth\_token*устарел.

**`OAUTH_TOKEN_REVOKED`**(int)

*oauth\_token* був відкликаний і надалі не буде ухвалено.

**`OAUTH_TOKEN_REJECTED`**(int)

Провайдер не прийняв *oauth\_token*. Причина невідома, але можливо полягає в тому, що токен ніколи не був виданий, чи вже був використаний, чи застарілий, чи був забутий провайдером.

**`OAUTH_VERIFIER_INVALID`**(int)

Некоректний *oauth\_verifier*

**`OAUTH_PARAMETER_ABSENT`**(int)

Необхідний параметр не було отримано. У цьому випадку відповідь повинна також містити параметр *oauth\_parameters\_absent*

**`OAUTH_SIGNATURE_METHOD_REJECTED`**(int)

*oauth\_signature\_method* не було прийнято провайдером.
