Варіант 2: використання cgi.forceredirect

-   [« Вариант 1: обслуживаются только общедоступные файлы](security.cgi-bin.default.html)
    
-   [Вариант 3: использование опций doc\_root или user\_dir »](security.cgi-bin.doc-root.html)
    
-   [PHP Manual](index.html)
    
-   [Если PHP установлен как CGI](security.cgi-bin.html)
    
-   Варіант 2: використання cgi.forceredirect
    

## Варіант 2: використання `cgi.force_redirect`

Конфігураційна директива [cgi.force\_redirect](ini.core.html#ini.cgi.force-redirect) запобігає спробам безпосереднього виклику PHP за адресою виду [http://my.host/cgi-bin/php/secretdir/script.php](http://my.host/cgi-bin/php/secretdir/script.php). Замість цього PHP оброблятиме запит лише в тому випадку, якщо він був перенаправлений веб-сервером.

Зазвичай перенаправлення в конфігурації Apache налаштовується за допомогою таких опцій:

Action php-script /cgi-bin/php AddHandler php-script .php

Ця опція перевірена лише з веб-сервером Apache, її робота ґрунтується на установці у разі перенаправлення нестандартної змінної REDIRECTSTATUS, що знаходиться в CGI-оточенні. У випадку, якщо ваш веб-сервер не надає можливості однозначно ідентифікувати, чи є цей запит перенаправленим, ви не можете використовувати опцію, що описується в цьому розділі, і повинні скористатися будь-яким іншим методом роботи з CGI-додатками.