Varnish

-   [« tcpwrap\_check](function.tcpwrap-check.html)
    
-   [Введение »](intro.varnish.html)
    
-   [PHP Manual](index.html)
    
-   [Другие службы](refs.remote.other.html)
    
-   Varnish
    

# Varnish

-   [Введение](intro.varnish.html)
-   [Установка и настройка](varnish.setup.html)
    -   [Требования](varnish.requirements.html)
    -   [Установка](varnish.installation.html)
    -   [Настройка во время выполнения](varnish.configuration.html)
    -   [Типы ресурсов](varnish.resources.html)
-   [Предопределённые константы](varnish.constants.html)
-   [Примеры](varnish.examples.html)
    -   [Простое использование VarnishAdmin](varnish.example.admin.html)
    -   [Простое использование VarnishStat](varnish.example.stat.html)
    -   [Простое использование VarnishLog](varnish.example.log.html)
-   [VarnishAdmin](class.varnishadmin.html) - Клас VarnishAdmin
    -   [VarnishAdmin::auth](varnishadmin.auth.html) — Аутентифікація на екземплярі varnish
    -   [VarnishAdmin::ban](varnishadmin.ban.html) — Заборонити URL-адресу за допомогою виразу VCL
    -   [VarnishAdmin::banUrl](varnishadmin.banurl.html) — Заборонити URL-адресу, використовуючи вираз VCL
    -   [VarnishAdmin::clearPanic](varnishadmin.clearpanic.html) — Очистити критичні повідомлення екземпляра varnish
    -   [VarnishAdmin::connect](varnishadmin.connect.html) — Підключення до інтерфейсу адміністрування екземпляра varnish
    -   [VarnishAdmin::\_\_construct](varnishadmin.construct.html) — VarnishAdmin constructor
    -   [VarnishAdmin::disconnect](varnishadmin.disconnect.html) — Відключення від інтерфейсу адміністрування екземпляра varnish
    -   [VarnishAdmin::getPanic](varnishadmin.getpanic.html) — Отримати останнє критичне повідомлення на екземплярі varnish
    -   [VarnishAdmin::getParams](varnishadmin.getparams.html) — Отримати параметри конфігурації поточного екземпляра varnish
    -   [VarnishAdmin::isRunning](varnishadmin.isrunning.html) — Перевірити, чи виконується зараз підпорядкований процес varnish
    -   [VarnishAdmin::setCompat](varnishadmin.setcompat.html) — Встановити параметр конфігурації класу compat
    -   [VarnishAdmin::setHost](varnishadmin.sethost.html) — Встановити параметр конфігурації host класу
    -   [VarnishAdmin::setIdent](varnishadmin.setident.html) — Встановити параметр конфігурації ident класу
    -   [VarnishAdmin::setParam](varnishadmin.setparam.html) — Встановити параметр конфігурації на поточному екземплярі varnish
    -   [VarnishAdmin::setPort](varnishadmin.setport.html) — Встановити параметр конфігурації класу port
    -   [VarnishAdmin::setSecret](varnishadmin.setsecret.html) — Встановити параметр конфігурації secret класу
    -   [VarnishAdmin::setTimeout](varnishadmin.settimeout.html) — Встановити параметр конфігурації timeout класу
    -   [VarnishAdmin::start](varnishadmin.start.html) — Запустити робочий процес varnish
    -   [VarnishAdmin::stop](varnishadmin.stop.html) — Зупинити робочий процес varnish
-   [VarnishStat](class.varnishstat.html) - Клас VarnishStat
    -   [VarnishStat::\_\_construct](varnishstat.construct.html) - Конструктор VarnishStat
    -   [VarnishStat::getSnapshot](varnishstat.getsnapshot.html) — Отримати фотографію статистики поточного екземпляра varnish
-   [VarnishLog](class.varnishlog.html) - Клас VarnishLog
    -   [VarnishLog::\_\_construct](varnishlog.construct.html) - Конструктор Varnishlog
    -   [VarnishLog::getLine](varnishlog.getline.html) — Отримати наступний рядок журналу
    -   [VarnishLog::getTagName](varnishlog.gettagname.html) — Отримати строкове представлення тега журналу за його індексом