---
navigation:
  - function.oauth-urlencode.md: « oauthurlencode
  - oauth.construct.md: 'OAuth::construct »'
  - index.md: PHP Manual
  - book.oauth.md: OAuth
title: Клас OAuth
---
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

-   [OAuth::construct](oauth.construct.md) — Створює новий об'єкт OAuth
-   [OAuth::destruct](oauth.destruct.md) - Деструктор
-   [OAuth::disableDebug](oauth.disabledebug.md) — Вимкнути докладну налагоджувальну інформацію
-   [OAuth::disableRedirects](oauth.disableredirects.md) — Вимкнути переадресацію
-   [OAuth::disableSSLChecks](oauth.disablesslchecks.md) — Вимкнути SSL перевірки
-   [OAuth::enableDebug](oauth.enabledebug.md) — Включити докладну налагоджувальну інформацію
-   [OAuth::enableRedirects](oauth.enableredirects.md) — Включити переадресацію
-   [OAuth::enableSSLChecks](oauth.enablesslchecks.md) — Увімкнути перевірки SSL
-   [OAuth::fetch](oauth.fetch.md) — Витягти захищений ресурс OAuth
-   [OAuth::generateSignature](oauth.generatesignature.md) - Згенерувати підпис
-   [OAuth::getAccessToken](oauth.getaccesstoken.md) — Отримати токен доступу
-   [OAuth::getCAPath](oauth.getcapath.md) — Отримати інформацію CA
-   [OAuth::getLastResponse](oauth.getlastresponse.md) — Отримати останню відповідь
-   [OAuth::getLastResponseHeaders](oauth.getlastresponseheaders.md) — Отримати заголовки останньої відповіді
-   [OAuth::getLastResponseInfo](oauth.getlastresponseinfo.md) — Отримати HTTP-інформацію про останню відповідь
-   [OAuth::getRequestHeader](oauth.getrequestheader.md) - Згенерувати підпис заголовка OAuth
-   [OAuth::getRequestToken](oauth.getrequesttoken.md) — Витягти токен запиту
-   [OAuth::setAuthType](oauth.setauthtype.md) - Встановити тип авторизації
-   [OAuth::setCAPath](oauth.setcapath.md) — Встановити CA для шляху та інформації
-   [OAuth::setNonce](oauth.setnonce.md) — Встановити nonce для подальших запитів
-   [OAuth::setRequestEngine](oauth.setrequestengine.md) — Використовується для setRequestEngine
-   [OAuth::setRSACertificate](oauth.setrsacertificate.md) — Встановити сертифікат RSA
-   [OAuth::setSSLChecks](oauth.setsslchecks.md) — Виконувати певні перевірки SSL для запиту
-   [OAuth::setTimestamp](oauth.settimestamp.md) — Встановити позначку часу
-   [OAuth::setToken](oauth.settoken.md) - Задати токен та його пароль
-   [OAuth::setVersion](oauth.setversion.md) — Встановити версію OAuth
