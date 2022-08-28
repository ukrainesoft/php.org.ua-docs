SOAP

-   [« OAuthException](class.oauthexception.html)
    
-   [Введение »](intro.soap.html)
    
-   [PHP Manual](index.html)
    
-   [Веб-сервисы](refs.webservice.html)
    
-   SOAP
    

# SOAP

-   [Введение](intro.soap.html)
-   [Установка и настройка](soap.setup.html)
    -   [Требования](soap.requirements.html)
    -   [Установка](soap.installation.html)
    -   [Настройка во время выполнения](soap.configuration.html)
    -   [Типы ресурсов](soap.resources.html)
-   [Предопределённые константы](soap.constants.html)
-   [Функции SOAP](ref.soap.html)
    -   [is\_soap\_fault](function.is-soap-fault.html) — Перевіряє, чи виникла помилка під час виклику SOAP
    -   [use\_soap\_error\_handler](function.use-soap-error-handler.html) — Встановити, чи слід використовувати обробник помилок SOAP
-   [SoapClient](class.soapclient.html) - Клас SoapClient
    -   [SoapClient::\_\_call](soapclient.call.html) - Викликає SOAP-функцію (застарілий метод)
    -   [SoapClient::\_\_construct](soapclient.construct.html) - Конструктор класу SoapClient
    -   [SoapClient::\_\_doRequest](soapclient.dorequest.html) - Виконує SOAP-запит
    -   [SoapClient::\_\_getCookies](soapclient.getcookies.html) — Отримати список cookies
    -   [SoapClient::\_\_getFunctions](soapclient.getfunctions.html) — Повертає список доступних SOAP-функцій
    -   [SoapClient::\_\_getLastRequest](soapclient.getlastrequest.html) - Повертає останній SOAP-запит
    -   [SoapClient::\_\_getLastRequestHeaders](soapclient.getlastrequestheaders.html) — Повертає SOAP-заголовки останнього запиту
    -   [SoapClient::\_\_getLastResponse](soapclient.getlastresponse.html) — Повертає останню SOAP-відповідь
    -   [SoapClient::\_\_getLastResponseHeaders](soapclient.getlastresponseheaders.html) — Повертає SOAP-заголовки останньої відповіді
    -   [SoapClient::\_\_getTypes](soapclient.gettypes.html) — Повертає список типів SOAP
    -   [SoapClient::\_\_setCookie](soapclient.setcookie.html) — Встановлює cookie для запитів SOAP
    -   [SoapClient::\_\_setLocation](soapclient.setlocation.html) — Встановлює адресу веб-служби, що використовується.
    -   [SoapClient::\_\_setSoapHeaders](soapclient.setsoapheaders.html) — Встановлює заголовки SOAP для наступних дзвінків
    -   [SoapClient::\_\_soapCall](soapclient.soapcall.html) - Викликає SOAP-функцію
-   [SoapServer](class.soapserver.html) - Клас SoapServer
    -   [SoapServer::addFunction](soapserver.addfunction.html) — Додає одну або кілька функцій для обробки запитів SOAP
    -   [SoapServer::addSoapHeader](soapserver.addsoapheader.html) — Додати заголовок SOAP у відповідь
    -   [SoapServer::\_\_construct](soapserver.construct.html) - Конструктор SoapServer
    -   [SoapServer::fault](soapserver.fault.html) — Вимушує SoapServer повернути помилку
    -   [SoapServer::getFunctions](soapserver.getfunctions.html) — Повернути список функцій
    -   [SoapServer::handle](soapserver.handle.html) - Обробка SOAP-запиту
    -   [SoapServer::setClass](soapserver.setclass.html) - Встановлює клас, який обробляє SOAP-запити
    -   [SoapServer::setObject](soapserver.setobject.html) — Встановлює об'єкт, який використовуватиметься для обробки SOAP-запитів
    -   [SoapServer::setPersistence](soapserver.setpersistence.html) — Встановлює режим збереження SoapServer
-   [SoapFault](class.soapfault.html) - Клас SoapFault
    -   [SoapFault::\_\_construct](soapfault.construct.html) - Конструктор SoapFault
    -   [SoapFault::\_\_toString](soapfault.tostring.html) — Отримати текстове уявлення SoapFault
-   [SoapHeader](class.soapheader.html) - Клас SoapHeader
    -   [SoapHeader::\_\_construct](soapheader.construct.html) - Конструктор SoapHeader
-   [SoapParam](class.soapparam.html) - Клас SoapParam
    -   [SoapParam::\_\_construct](soapparam.construct.html) - Конструктор SoapParam
-   [SoapVar](class.soapvar.html) - Клас SoapVar
    -   [SoapVar::\_\_construct](soapvar.construct.html) - Конструктор SoapVar