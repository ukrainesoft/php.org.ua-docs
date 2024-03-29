---
navigation:
  - function.tcpwrap-check.md: « tcpwrap\_check
  - intro.varnish.md: Вступ "
  - index.md: PHP Manual
  - refs.remote.other.md: Інші служби
title: Varnish
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Varnish

-   [Вступ](intro.varnish.md)
-   [Встановлення та налаштування](varnish.setup.md)
    -   [Вимоги](varnish.requirements.md)
    -   [Установка](varnish.installation.md)
    -   [Налаштування під час виконання](varnish.configuration.md)
    -   [Типи ресурсів](varnish.resources.md)
-   [Обумовлені константи](varnish.constants.md)
-   [Приклади](varnish.examples.md)
    -   [Просте використання VarnishAdmin](varnish.example.admin.md)
    -   [Просте використання VarnishStat](varnish.example.stat.md)
    -   [Просте використання VarnishLog](varnish.example.log.md)
-   [VarnishAdmin](class.varnishadmin.md) \- Клас VarnishAdmin
    -   [VarnishAdmin::auth](varnishadmin.auth.md)— Аутентифікація на екземплярі varnish
    -   [VarnishAdmin::ban](varnishadmin.ban.md)— Заборонити URL-адресу за допомогою виразу VCL
    -   [VarnishAdmin::banUrl](varnishadmin.banurl.md)— Заборонити URL-адресу, використовуючи вираз VCL
    -   [VarnishAdmin::clearPanic](varnishadmin.clearpanic.md)— Очистити критичні повідомлення екземпляра varnish
    -   [VarnishAdmin::connect](varnishadmin.connect.md)— Підключення до інтерфейсу адміністрування екземпляра varnish
    -   [VarnishAdmin::\_\_construct](varnishadmin.construct.md)— VarnishAdmin constructor
    -   [VarnishAdmin::disconnect](varnishadmin.disconnect.md)— Відключення від інтерфейсу адміністрування екземпляра varnish
    -   [VarnishAdmin::getPanic](varnishadmin.getpanic.md)— Отримати останнє критичне повідомлення на екземплярі varnish
    -   [VarnishAdmin::getParams](varnishadmin.getparams.md)— Отримати параметри конфігурації поточного екземпляра varnish
    -   [VarnishAdmin::isRunning](varnishadmin.isrunning.md)— Перевірити, чи виконується зараз підпорядкований процес varnish
    -   [VarnishAdmin::setCompat](varnishadmin.setcompat.md)— Встановити параметр конфігурації класу compat
    -   [VarnishAdmin::setHost](varnishadmin.sethost.md)— Встановити параметр конфігурації host класу
    -   [VarnishAdmin::setIdent](varnishadmin.setident.md)— Встановити параметр конфігурації ident класу
    -   [VarnishAdmin::setParam](varnishadmin.setparam.md)— Встановити параметр конфігурації на поточному екземплярі varnish
    -   [VarnishAdmin::setPort](varnishadmin.setport.md)— Встановити параметр конфігурації класу port
    -   [VarnishAdmin::setSecret](varnishadmin.setsecret.md)— Встановити параметр конфігурації secret класу
    -   [VarnishAdmin::setTimeout](varnishadmin.settimeout.md)— Встановити параметр конфігурації timeout класу
    -   [VarnishAdmin::start](varnishadmin.start.md)— Запустити робочий процес varnish
    -   [VarnishAdmin::stop](varnishadmin.stop.md)— Зупинити робочий процес varnish
-   [VarnishStat](class.varnishstat.md) \- Клас VarnishStat
    -   [VarnishStat::\_\_construct](varnishstat.construct.md) \- Конструктор VarnishStat
    -   [VarnishStat::getSnapshot](varnishstat.getsnapshot.md)— Отримати фотографію статистики поточного екземпляра varnish
-   [VarnishLog](class.varnishlog.md) \- Клас VarnishLog
    -   [VarnishLog::\_\_construct](varnishlog.construct.md) \- Конструктор Varnishlog
    -   [VarnishLog::getLine](varnishlog.getline.md)— Отримати наступний рядок журналу
    -   [VarnishLog::getTagName](varnishlog.gettagname.md)— Отримати строкове подання тега журналу за його індексом
