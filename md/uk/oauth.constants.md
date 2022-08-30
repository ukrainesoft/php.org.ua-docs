Обумовлені константи

-   [« Типи ресурсів](oauth.resources.md)
    
-   [Приклади »](oauth.examples.md)
    
-   [PHP Manual](index.md)
    
-   [OAuth](book.oauth.md)
    
-   Обумовлені константи
    

# Обумовлені константи

Наведені нижче константи визначені даним модулем і можуть бути доступні тільки в тому випадку, якщо PHP був зібраний за допомогою цього модуля або в тому випадку, якщо даний модуль був динамічно завантажений під час виконання.

Більшість з цих констант торкаються проблем, зазначених у тому числі в офіційних [» сообщениях о проблемах](http://wiki.oauth.net/ProblemReporting) OAuth. Однак зауважте, що хоча ці імена констант і мають схожу схему імен, вони характерні тільки для PHP.

**`OAUTH_SIG_METHOD_RSASHA1`** (string)

Метод підпису OAuth *RSA-SHA1*

**`OAUTH_SIG_METHOD_HMACSHA1`** (string)

Метод підпису OAuth *HMAC-SHA1*

**`OAUTH_SIG_METHOD_HMACSHA256`** (string)

Метод підпису OAuth *HMAC-SHA256*

**`OAUTH_AUTH_TYPE_AUTHORIZATION`** (string)

Ця константа вказує, що OAuth параметри буде поміщено в заголовок `Authorization`

**`OAUTH_AUTH_TYPE_NONE`** (string)

Ця константа означає NoAuth OAuth запит.

**`OAUTH_AUTH_TYPE_URI`** (string)

Ця константа вказує, що OAuth параметри буде розміщено в URI запиту. URI.

**`OAUTH_AUTH_TYPE_FORM`** (string)

Ця константа вказує на те, що OAuth параметри будуть поміщені в тіло HTTP POST запиту.

**`OAUTH_HTTP_METHOD_GET`** (string)

Константа вказує на використання *GET* метод для OAuth запиту.

**`OAUTH_HTTP_METHOD_POST`** (string)

Константа вказує на використання *POST* метод для OAuth запиту.

**`OAUTH_HTTP_METHOD_PUT`** (string)

Константа вказує на використання *PUT* метод для OAuth запиту.

**`OAUTH_HTTP_METHOD_HEAD`** (string)

Константа вказує на використання *HEAD* метод для OAuth запиту.

**`OAUTH_HTTP_METHOD_DELETE`** (string)

Константа вказує на використання *DELETE* метод для OAuth запиту.

**`OAUTH_REQENGINE_STREAMS`** (int)

Використовується методом [OAuth::setRequestEngine()](oauth.setrequestengine.md) Для вибору [потоків PHP](book.stream.md) як двигун, на противагу константі **`OAUTH_REQENGINE_CURL`**, що використовується для вибору [Curl](book.curl.md)

**`OAUTH_REQENGINE_CURL`** (int)

Використовується методом [OAuth::setRequestEngine()](oauth.setrequestengine.md) Для вибору [Curl](book.curl.md) як двигун, на противагу константі **`OAUTH_REQENGINE_STREAMS`**, що використовується для вибору [потоків PHP](book.stream.md)

**`OAUTH_OK`** (int)

Життя прекрасне.

**`OAUTH_BAD_NONCE`** (int)

Значення *oauthnonce* використовувалося у попередньому запиті, отже, не може бути використане зараз.

**`OAUTH_BAD_TIMESTAMP`** (int)

Значення *oauthtimestamp* не було прийнято провайдером. У цьому випадку відповідь повинна також містити параметр *oauthaceptabletimestamps*

**`OAUTH_CONSUMER_KEY_UNKNOWN`** (int)

*oauthconsumerkey* тимчасово недоступний провайдеру. Наприклад, якщо провайдер заблокував споживача.

**`OAUTH_CONSUMER_KEY_REFUSED`** (int)

Ключ споживача було відхилено.

**`OAUTH_INVALID_SIGNATURE`** (int)

Значення *oauthsignature* недійсно, оскільки не збігається з підписом, обчисленим провайдером.

**`OAUTH_TOKEN_USED`** (int)

*oauthtoken* було вжито. Він уже використовувався у попередньому запиті/запитах і більше не може бути використаний.

**`OAUTH_TOKEN_EXPIRED`** (int)

*oauthtoken* застарів.

**`OAUTH_TOKEN_REVOKED`** (int)

*oauthtoken* був відкликаний і надалі не буде ухвалено.

**`OAUTH_TOKEN_REJECTED`** (int)

Провайдер не прийняв *oauthtoken*. Причина невідома, але можливо полягає в тому, що токен ніколи не був виданий, чи вже був використаний, чи застарілий, чи був забутий провайдером.

**`OAUTH_VERIFIER_INVALID`** (int)

Некоректний *oauthverifier*

**`OAUTH_PARAMETER_ABSENT`** (int)

Необхідний параметр не було отримано. У цьому випадку відповідь повинна також містити параметр *oauthparametersabsent*

**`OAUTH_SIGNATURE_METHOD_REJECTED`** (int)

*oauthsignatureметод* не було прийнято провайдером.