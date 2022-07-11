- [« OAuth::getRequestHeader](oauth.getrequestheader.md)
- [OAuth::setAuthType »](oauth.setauthtype.md)

- [PHP Manual](index.md)
- [OAuth](class.oauth.md)
- Витягти токен запиту

# OAuth::getRequestToken

(PECL OAuth = 0.99.1)

OAuth::getRequestToken — Витягти токен запиту

### Опис

public **OAuth::getRequestToken**(string `$request_token_url`, string
`$callback_url` = ?, string `$http_method` = ?): array

Отримати токен запиту, його пароль та додаткові параметри відповіді
постачальника послуг.

### Список параметрів

`request_token_url`
URL до API токена запиту.

callback_url
URL callback-функції OAuth. Якщо `callback_url` заданий порожнім значенням,
то він встановиться як "oob" рішення OAuth 2009.1.

`http_method`
HTTP-метод, наприклад `GET` або `POST`.

### Значення, що повертаються

Повертає масив обробленого запиту OAuth або **false**.

### Список змін

| Версія            | Опис                                                                    |
|-------------------|-------------------------------------------------------------------------|
| PECL oauth 1.0.0  | Раніше у разі виникнення помилки повертався **null** замість **false**. |
| PECL oauth 0.99.9 | Доданий параметр callback_url                                           |

### Приклади

**Приклад #1 Приклад використання **OAuth::getRequestToken()****

` <?phptry {|   $oauth = new OAuth(OAUTH_CONSUMER_KEY,OAUTH_CONSUMER_SECRET); $request_token_info==$oauth->getRequestToken("https://example.com/oauth/request_token"); if(!empty($request_token_info)) {        print_r($request_token_info); } else {        print "Не удалося отримати токен доступу, відповідь був: " . $oauth->getLastResponse(); }} catch(OAuthException $E) {   echo "Відповідь: ". $E->lastResponse . "
";}?> `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[oauth_token] => some_token
[oauth_token_secret] => some_token_secret
)

### Дивіться також

- [OAuth::getLastResponse()](oauth.getlastresponse.md) - Отримати
остання відповідь
- [OAuth::getLastResponseInfo()](oauth.getlastresponseinfo.md) -
Отримати HTTP-інформацію про останню відповідь
