---
navigation:
  - install.cloud.md: « Встановлення на платформах Cloud Computing
  - install.cloud.ec2.md: Amazon EC2 »
  - index.md: PHP Manual
  - install.cloud.md: Встановлення на платформах Cloud Computing
title: Azure App Services
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Azure App Services

PHP часто встановлюється на хмарний сервіс Azure App Services (також відомий як Microsoft Azure, Windows Azure та Azure Web Apps).

Azure App Services керує пулом Windows Web Servers для хостингу ваших веб-застосунків і представляє альтернативу створенню власного веб-сервера на власному Azure Compute VMs та інших платформах.

PHP за промовчанням доступний для вашого веб-сайту в Azure App Services. Просто оберіть на Azure Portal ваш сайт і виберіть потрібну версію PHP. Ви можете вибрати свіжішу версію, ніж за замовчуванням.

Таким чином, PHP та його модулі будуть працювати в Azure App Services так само, як і на будь-якому іншому сервері Windows. Більшість бази знань також портована, дивіться [Windows Troubleshooting Page](install.windows.troubleshooting.md) Тим не менш, інтерфейс керування для Azure App Services має відмінності:

-   Azure portal: создание, настройка и удаление сайтов . [» Azure Portal](https://portal.azure.com/)
    
-   Панель Kudu:\[ім'я вашого сайту\].azurewebsites.net. Тоді панель Kudu[» https://\[ім'я вашого сайту\].scm.azurewebsites.net/](https://your_web_site_name.scm.azurewebsites.net/). Панель Kudu дає вам доступ до деяких можливостей налагодження, керування файлами та модулями сайту. Модулі сайту - це механізм Azure для додавання програм, наприклад прев'ю збірок PHP, на ваш сайт.
    
-   Ви не зможете використовувати IIS Manager, Server Manager або RDP.
    

PHP SDK дозволяє програмно використовувати безліч Azure Services. Дивись [» Azure SDK для PHP](https://github.com/Azure/azure-sdk-for-php)

Для більш детальної інформації, дивись [» Azure PHP Developer Center](https://azure.microsoft.com/en-us/develop/php/)

### WinCache

WinCache за замовчуванням дозволено в Azure App Services і рекомендується його не відключати. Якщо ви встановили свою збірку PHP, ви повинні дозволити WinCache.

### Власні зборки PHP

Ви можете завантажити власну збірку PHP у D:\\Home (C:\\НЕ ДОСТУПЕН для записи). После чего, на Azure Portal, задайте SCRIPT\_PROCESSOR для .php дорівнює абсолютному шляху до php-cgi.exe з вашої збірки.
