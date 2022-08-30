OAuth

-   [« Веб-сервисы](refs.webservice.html)
    
-   [Введение »](intro.oauth.html)
    
-   [PHP Manual](index.html)
    
-   [Веб-сервисы](refs.webservice.html)
    
-   OAuth
    

# OAuth

-   [Введение](intro.oauth.html)
-   [Установка и настройка](oauth.setup.html)
    -   [Требования](oauth.requirements.html)
    -   [Установка](oauth.installation.html)
    -   [Настройка во время выполнения](oauth.configuration.html)
    -   [Типы ресурсов](oauth.resources.html)
-   [Предопределённые константы](oauth.constants.html)
-   [Примеры](oauth.examples.html)
    -   [FireEagle](oauth.examples.fireeagle.html)
-   [Функции OAuth](ref.oauth.html)
    -   [oauthgetsbs](function.oauth-get-sbs.html) - Створити базовий рядок підпису (Signature Base String)
    -   [oauthurlencode](function.oauth-urlencode.html) — Кодує URI відповідно до RFC 3986
-   [OAuth](class.oauth.html) - Клас OAuth
    -   [OAuth::construct](oauth.construct.html) — Створює новий об'єкт OAuth
    -   [OAuth::destruct](oauth.destruct.html) - Деструктор
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
-   [OAuthProvider](class.oauthprovider.html) - Клас OAuthProvider
    -   [OAuthProvider::addRequiredParameter](oauthprovider.addrequiredparameter.html) — Додати необхідні параметри
    -   [OAuthProvider::callconsumerHandler](oauthprovider.callconsumerhandler.html) — Викликати callback-функцію consumerNonceHandler
    -   [OAuthProvider::callTimestampNonceHandler](oauthprovider.calltimestampnoncehandler.html) — Викликати callback-функцію timestampNonceHandler
    -   [OAuthProvider::calltokenHandler](oauthprovider.calltokenhandler.html) — Викликати callback-функцію tokenNonceHandler
    -   [OAuthProvider::checkOAuthRequest](oauthprovider.checkoauthrequest.html) - Перевірка запиту oauth
    -   [OAuthProvider::construct](oauthprovider.construct.html) - Конструктор класу OAuthProvider
    -   [OAuthProvider::consumerHandler](oauthprovider.consumerhandler.html) — Встановити обробник consumerHandler
    -   [OAuthProvider::generateToken](oauthprovider.generatetoken.html) - Генерація випадкового токена
    -   [OAuthProvider::is2LeggedEndpoint](oauthprovider.is2leggedendpoint.html) - is2LeggedEndpoint
    -   [OAuthProvider::isRequestTokenEndpoint](oauthprovider.isrequesttokenendpoint.html) — Установка isRequestTokenEndpoint
    -   [OAuthProvider::removeRequiredParameter](oauthprovider.removerequiredparameter.html) — Видалити потрібний параметр
    -   [OAuthProvider::reportProblem](oauthprovider.reportproblem.html) — Повідомити про проблему
    -   [OAuthProvider::setParam](oauthprovider.setparam.html) — Встановити параметр
    -   [OAuthProvider::setRequestTokenPath](oauthprovider.setrequesttokenpath.html) - Встановити шлях запиту токена
    -   [OAuthProvider::timestampNonceHandler](oauthprovider.timestampnoncehandler.html) — Встановити обробник timestampNonceHandler
    -   [OAuthProvider::tokenHandler](oauthprovider.tokenhandler.html) — Встановити обробник tokenHandler
-   [OAuthException](class.oauthexception.html) - Клас OAuthException