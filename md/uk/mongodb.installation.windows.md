---
navigation:
  - mongodb.installation.homebrew.md: « Установка драйвера PHP MongoDB на macOS помощью Homebrew
  - mongodb.installation.manual.md: Сборка драйвера PHP MongoDB из исходного кода »
  - index.md: PHP Manual
  - mongodb.installation.md: Установка
title: Встановлення драйвера PHP MongoDB під Windows
---
## Встановлення драйвера PHP MongoDB під Windows

Скомпільовані модулі для кожної версії доступні на сайті [» PECL](https://pecl.php.net/package/mongodb) для всіх комбінацій версій, потокобезпеки та бібліотек VC. Розархівуйте завантажений модуль та скопіюйте phpmongo.dll - директорію з модулями PHP (за замовчуванням "ext").

Додайте наступний рядок до файлу php.ini для кожного оточення, в якому ви збираєтеся використовувати драйвер:

extension=phpmongo.dll

> **Зауваження** **Додаткові залежності DLL для користувачів Windows**
> 
> Для роботи цього модуля системної змінної Windows PATH повинні бути доступні DLLфайли. Щоб дізнатися, як цього досягти, зверніться до розділу FAQ "[Як додати мою директорію з PHP до змінної Windows PATH](faq.installation.md#faq.installation.addtopath)". Хоча копіювання DLL-файлів з директорії PHP до системної папки Windows також вирішує проблему (бо системна директорія за умовчанням знаходиться в змінній PATH), це не рекомендується . *Цей модуль потребує наступних файлів у змінній PATH:* libsasl.dll
