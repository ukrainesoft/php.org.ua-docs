---
navigation:
  - copyright.md: Авторські права "
  - index.md: PHP Manual
title: Посібник з PHP
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Посібник з PHP

**от** :  
Mehdi Achour

Friedhelm Betz

Antony Dovgal

Nuno Lopes

Hannes Magnusson

Georg Richter

Damien Seguy

Jakub Vrana

[І деякі інші](preface.md#contributors)

2024-02-04

**Під редакцією**: Peter Cowburn

**от** :  
Олексій Шеїн

Андрій Безруков

Максим Чабан

Олександр Москальов

Борис Клименко

Дмитро Вінярчук

Борис Флейтліх

Олексій Єгоров

Юрій Бабіков

Михайло Баранов

Андрій Громов

Олексій Пильцин

Сергій Пантелєєв

Сергій Зорін

Євген Четверіков

[І деякі інші](preface.md#other.translators)

© 1997-2024 Група документування PHP

-   [Авторські права](copyright.md)
-   [Посібник з PHP](manual.md)
    -   [Передмова](preface.md)
-   [Приступаючи до роботи](getting-started.md)
    -   [Вступ](introduction.md)
    -   [Простий підручник](tutorial.md)
-   [Встановлення та налаштування](install.md)
    -   [Загальні інструкції щодо встановлення](install.general.md)
    -   [Встановлення на Unix-системи](install.unix.md)
    -   [Встановлення на macOS](install.macosx.md)
    -   [Встановлення у системах Windows](install.windows.md)
    -   [Встановлення на платформах Cloud Computing](install.cloud.md)
    -   [Менеджер процесів FastCGI (FPM)](install.fpm.md)
    -   [Встановлення модулів PECL](install.pecl.md)
    -   [Проблеми?](install.problems.md)
    -   [Конфігурація часу виконання](configuration.md)
-   [Довідник мови](langref.md)
    -   [Основи синтаксису](language.basic-syntax.md)
    -   [Типи](language.types.md)
    -   [Змінні](language.variables.md)
    -   [Константи](language.constants.md)
    -   [Вирази](language.expressions.md)
    -   [Оператори](language.operators.md)
    -   [Керуючі конструкції](language.control-structures.md)
    -   [Функції](language.functions.md)
    -   [Класи та об'єкти](language.oop5.md)
    -   [Простори імен](language.namespaces.md)
    -   [Перерахування](language.enumerations.md)
    -   [Помилки](language.errors.md)
    -   [Винятки](language.exceptions.md)
    -   [Fibers](language.fibers.md)
    -   [Генератори](language.generators.md)
    -   [Атрибути](language.attributes.md)
    -   [Пояснення посилань](language.references.md)
    -   [Зумовлені змінні](reserved.variables.md)
    -   [Обумовлені винятки](reserved.exceptions.md)
    -   [Вбудовані інтерфейси та класи](reserved.interfaces.md)
    -   [Зумовлені атрибути](reserved.attributes.md)
    -   [Контекстні опції та параметри](context.md)
    -   [Підтримувані протоколи та обгортки](wrappers.md)
-   [Безпека](security.md)
    -   [Вступ](security.intro.md)
    -   [Загальні міркування](security.general.md)
    -   [Якщо PHP встановлено як CGI](security.cgi-bin.md)
    -   [Якщо PHP встановлено як модуль Apache](security.apache.md)
    -   [Безпека сесій](security.sessions.md)
    -   [Безпека файлової системи](security.filesystem.md)
    -   [Безпека баз даних](security.database.md)
    -   [Повідомлення про помилки](security.errors.md)
    -   [Дані, введені користувачем](security.variables.md)
    -   [Приховування PHP](security.hiding.md)
    -   [Необхідність оновлень](security.current.md)
-   [Особливості](features.md)
    -   [HTTP-автентифікація в PHP](features.http-auth.md)
    -   [Cookies](features.cookies.md)
    -   [Сесії](features.sessions.md)
    -   [Робота з XForms](features.xforms.md)
    -   [Завантаження файлів на сервер](features.file-upload.md)
    -   [Робота з віддаленими файлами](features.remote-files.md)
    -   [Робота зі з'єднаннями](features.connection-handling.md)
    -   [Постійні з'єднання з базами даних](features.persistent-connections.md)
    -   [Робота з PHP з командного рядка](features.commandline.md)
    -   [Складання сміття](features.gc.md)
    -   [Динамічна трасування DTrace](features.dtrace.md)
-   [Довідник функцій](funcref.md)
    -   [Зміна поведінки PHP](refs.basic.php.md)
    -   [Обробка аудіоформатів](refs.utilspec.audio.md)
    -   [Служби автентифікації](refs.remote.auth.md)
    -   [Модулі для роботи з командним рядком](refs.utilspec.cmdline.md)
    -   [Модулі для стиснення та архівації](refs.compression.md)
    -   [Криптографічні модулі](refs.crypto.md)
    -   [Модулі для роботи з базами даних](refs.database.md)
    -   [Модулі для роботи з датою та часом](refs.calendar.md)
    -   [Модулі для роботи з файловою системою](refs.fileprocess.file.md)
    -   [Підтримка мов та кодувань](refs.international.md)
    -   [Обробка та генерація зображень](refs.utilspec.image.md)
    -   [Модулі для роботи з поштою](refs.remote.mail.md)
    -   [Математичні модулі](refs.math.md)
    -   [Генерація нетекстових MIME-форматів](refs.utilspec.nontext.md)
    -   [Модулі для керування процесами програм](refs.fileprocess.process.md)
    -   [Інші базові модулі](refs.basic.other.md)
    -   [Інші служби](refs.remote.other.md)
    -   [Модулі для роботи з пошуковими системами](refs.search.md)
    -   [Модулі для роботи із серверами](refs.utilspec.server.md)
    -   [Модулі для роботи із сесіями](refs.basic.session.md)
    -   [Обробка тексту](refs.basic.text.md)
    -   [Модулі, що відносяться до змінних та типів](refs.basic.vartype.md)
    -   [Веб-сервіси](refs.webservice.md)
    -   [Модулі лише для Windows](refs.utilspec.windows.md)
    -   [Обробка XML](refs.xml.md)
    -   [Модулі для роботи з GUI](refs.ui.md)
-   [ЧАВО](faq.md)— ЧАВО: Часті питання та відповіді на них
    -   [Загальна інформація](faq.general.md)
    -   [Списки розсилки](faq.mailinglist.md)
    -   [Отримання PHP](faq.obtaining.md)
    -   [Питання щодо баз даних](faq.databases.md)— Питання щодо Баз даних
    -   [Установка](faq.installation.md)
    -   [Проблеми збирання](faq.build.md)
    -   [Використання PHP](faq.using.md)
    -   [Хешування паролів](faq.passwords.md) \- Безпечне хешування паролів
    -   [PHP та HTML](faq.md.md)
    -   [PHP та COM](faq.com.md)
    -   [Різні питання](faq.misc.md)
-   [Програми](appendices.md)
    -   [Історія PHP та суміжних проектів](history.md)
    -   [Міграція з PHP 8.2.x на PHP 8.3.x](migration83.md)
    -   [Міграція з PHP 8.1.x на PHP 8.2.x](migration82.md)
    -   [Міграція з PHP 8.0.x на PHP 8.1.x](migration81.md)
    -   [Міграція з PHP 7.4.x на PHP 8.0.x](migration80.md)
    -   [Міграція з PHP 7.3.x на PHP 7.4.x](migration74.md)
    -   [Міграція з PHP 7.2.x на PHP 7.3.x](migration73.md)
    -   [Міграція з PHP 7.1.x на PHP 7.2.x](migration72.md)
    -   [Міграція з PHP 7.0.x на PHP 7.1.x](migration71.md)
    -   [Міграція з PHP 5.6.x на PHP 7.0.x](migration70.md)
    -   [Міграція з PHP 5.5.x на PHP 5.6.x](migration56.md)
    -   [Налагодження в PHP](debugger.md)
    -   [Опції конфігурації](configure.md)
    -   [Директиви php.ini](ini.md)
    -   [Список/класифікація модулів](extensions.md)
    -   [Список псевдонімів функцій](aliases.md)
    -   [Список зарезервованих слів](reserved.md)
    -   [Список типів ресурсів](resource.md)
    -   [Список доступних фільтрів](filters.md)
    -   [Список підтримуваних транспортних протоколів](transports.md)
    -   [Таблиці порівняння типів PHP](types.comparisons.md)
    -   [Список тегів (tokens) парсера](tokens.md)
    -   [Посібник з іменування](userlandnaming.md)
    -   [Про це керівництво](about.md)
    -   [Creative Commons Attribution 3.0](cc.license.md)
    -   [Алфавітний перелік](indexes.md)
    -   [список змін](doc.changelog.md)
