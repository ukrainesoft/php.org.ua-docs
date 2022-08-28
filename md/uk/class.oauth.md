Клас OAuth

-   [« oauth\_urlencode](function.oauth-urlencode.html)
    
-   [OAuth::\_\_construct »](oauth.construct.html)
    
-   [PHP Manual](index.html)
    
-   [OAuth](book.oauth.html)
    
-   Клас OAuth
    

# Клас OAuth

(PECL OAuth >= 0.99.1)

## Вступ

Модуль OAuth надає простий інтерфейс для взаємодії з провайдерами даних, які використовують специфікацію OAuth HTTP для захисту приватних ресурсів.

## Огляд класів

```classsynopsis


    
    
     
      class OAuth
     
     {
    

    /* Свойства */
    
     public
      $debug;

    public
      $sslChecks;

    public
      $debugInfo;


    /* Методы */
    
   public __construct(    string $consumer_key,    string $consumer_secret,    string $signature_method = OAUTH_SIG_METHOD_HMACSHA1,    int $auth_type = 0)

    public __destruct(): void
public disableDebug(): bool
public disableRedirects(): bool
public disableSSLChecks(): bool
public enableDebug(): bool
public enableRedirects(): bool
public enableSSLChecks(): bool
public fetch(    string $protected_resource_url,    array $extra_parameters = ?,    string $http_method = ?,    array $http_headers = ?): mixed
public generateSignature(string $http_method, string $url, mixed $extra_parameters = ?): string|false
public getAccessToken(    string $access_token_url,    string $auth_session_handle = ?,    string $verifier_token = ?,    string $http_method = ?): array
public getCAPath(): array
public getLastResponse(): string
public getLastResponseHeaders(): string|false
public getLastResponseInfo(): array
public getRequestHeader(string $http_method, string $url, mixed $extra_parameters = ?): string|false
public getRequestToken(string $request_token_url, string $callback_url = ?, string $http_method = ?): array
public setAuthType(int $auth_type): bool
public setCAPath(string $ca_path = ?, string $ca_info = ?): mixed
public setNonce(string $nonce): mixed
public setRequestEngine(int $reqengine): void
public setRSACertificate(string $cert): mixed
public setSSLChecks(int $sslcheck): bool
public setTimestamp(string $timestamp): mixed
public setToken(string $token, string $token_secret): bool
public setVersion(string $version): bool

   }
```

## Властивості

debug

sslChecks

debugInfo

## Зміст

-   [OAuth::\_\_construct](oauth.construct.html) — Створює новий об'єкт OAuth
-   [OAuth::\_\_destruct](oauth.destruct.html) - Деструктор
-   [OAuth::disableDebug](oauth.disabledebug.html) — Вимкнути докладну налагоджувальну інформацію
-   [OAuth::disableRedirects](oauth.disableredirects.html) — Вимкнути переадресацію
-   [OAuth::disableSSLChecks](oauth.disablesslchecks.html) — Вимкнути SSL перевірки
-   [OAuth::enableDebug](oauth.enabledebug.html) — Включити докладну налагоджувальну інформацію
-   [OAuth::enableRedirects](oauth.enableredirects.html) — Включити переадресацію
-   [OAuth::enableSSLChecks](oauth.enablesslchecks.html) — Увімкнути перевірки SSL
-   [OAuth::fetch](oauth.fetch.html) — Витягти захищений ресурс OAuth
-   [OAuth::generateSignature](oauth.generatesignature.html) - Згенерувати підпис
-   [OAuth::getAccessToken](oauth.getaccesstoken.html) — Отримати токен доступу
-   [OAuth::getCAPath](oauth.getcapath.html) — Отримати інформацію CA
-   [OAuth::getLastResponse](oauth.getlastresponse.html) — Отримати останню відповідь
-   [OAuth::getLastResponseHeaders](oauth.getlastresponseheaders.html) — Отримати заголовки останньої відповіді
-   [OAuth::getLastResponseInfo](oauth.getlastresponseinfo.html) — Отримати HTTP-інформацію про останню відповідь
-   [OAuth::getRequestHeader](oauth.getrequestheader.html) - Згенерувати підпис заголовка OAuth
-   [OAuth::getRequestToken](oauth.getrequesttoken.html) — Витягти токен запиту
-   [OAuth::setAuthType](oauth.setauthtype.html) - Встановити тип авторизації
-   [OAuth::setCAPath](oauth.setcapath.html) — Встановити CA для шляху та інформації
-   [OAuth::setNonce](oauth.setnonce.html) — Встановити nonce для подальших запитів
-   [OAuth::setRequestEngine](oauth.setrequestengine.html) — Використовується для setRequestEngine
-   [OAuth::setRSACertificate](oauth.setrsacertificate.html) — Встановити сертифікат RSA
-   [OAuth::setSSLChecks](oauth.setsslchecks.html) — Виконувати певні перевірки SSL для запиту
-   [OAuth::setTimestamp](oauth.settimestamp.html) — Встановити позначку часу
-   [OAuth::setToken](oauth.settoken.html) - Задати токен та його пароль
-   [OAuth::setVersion](oauth.setversion.html) — Встановити версію OAuth