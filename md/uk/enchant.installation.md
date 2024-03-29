---
navigation:
  - enchant.requirements.md: « Вимоги
  - enchant.configuration.md: Налаштування під час виконання »
  - index.md: PHP Manual
  - enchant.setup.md: Встановлення та налаштування
title: Установка
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Установка

Якщо встановлено [необхідні бібліотеки](enchant.requirements.md), то модуль можна встановити за допомогою опції **\--with-enchant\[=dir\]** при компіляції PHP.

Користувачі Windows повинні увімкнути php\_enchant.dll використовувати модуль.

> **Зауваження** **Додаткове налаштування у Windows**
> 
> Для роботи цього модуля системної змінної Windows PATH повинні бути доступні DLL-файли. Щоб дізнатися, як цього досягти, зверніться до розділу FAQ "[Як додати мою директорію з PHP до змінної Windows PATH](faq.installation.md#faq.installation.addtopath)". Хоча копіювання DLL-файлів з директорії PHP до системної папки Windows також вирішує проблему (бо системна директорія за умовчанням знаходиться в змінній PATH), це не рекомендується. . \*Цей модуль потребує наступних файлів у змінній PATH:\*libenchant.dll, glib-2.dll, gmodule-2.dll.
> 
> Крім того, необхідно скопіювати хоча б одного постачальника з lib\\enchant в\\usr\\local\\lib\\enchant-2 (це абсолютний шлях від кореня *поточного диска*). До версії PHP 8.0.0, тобто. при використанні Enchant v1, постачальники повинні були бути скопійовані C:\\enchant\_plugins, де цей шлях може бути налаштований шляхом створення значення реєстру `HKEY_CURRENT_USER\SOFTWARE\Enchant\Config\Module_Dir`, вказавши у ньому бажаний шлях.
