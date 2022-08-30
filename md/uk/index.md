Посібник з PHP

-   [Авторские права »](copyright.md)
    
-   [PHP Manual](index.md)
    
-   Посібник з PHP
    

# Посібник з PHP

**від**  
Mehdi Achour

Friedhelm Betz

Antony Dovgal

Nuno Lopes

Hannes Magnusson

Georg Richter

Damien Seguy

Jakub Vrana

[І деякі інші](preface.html#contributors)

**Під редакцією**: Peter Cowburn

**від**  
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

[І деякі інші](preface.html#other.translators)

© 1997-2022 Група документування PHP

-   [Авторские права](copyright.md)
-   [Руководство по PHP](manual.md)
    -   [Предисловие](preface.md)
-   [Приступаючи до роботи](getting-started.html)
    -   [Введение](introduction.md)
    -   [Простий підручник](tutorial.md)
-   [Встановлення та налаштування](install.md)
    -   [Общие инструкции по установке](install.general.md)
    -   [Встановлення на Unix-системи](install.unix.md)
    -   [Установка на macOS](install.macosx.md)
    -   [Установка в системах Windows](install.windows.md)
    -   [Установка на платформах Cloud Computing](install.cloud.md)
    -   [Менеджер процесів FastCGI (FPM)](install.fpm.md)
    -   [Установка модулей PECL](install.pecl.md)
    -   [Проблеми?](install.problems.md)
    -   [Конфігурація часу виконання](configuration.md)
-   [Довідник мови](langref.md)
    -   [Основи синтаксису](language.basic-syntax.html)
    -   [Типи](language.types.md)
    -   [Змінні](language.variables.md)
    -   [Константи](language.constants.md)
    -   [Вирази](language.expressions.md)
    -   [Оператори](language.operators.md)
    -   [Управляющие конструкции](language.control-structures.html)
    -   [Функції](language.functions.md)
    -   [Класи та об'єкти](language.oop5.md)
    -   [Пространства имён](language.namespaces.md)
    -   [Перечисления](language.enumerations.md)
    -   [Ошибки](language.errors.md)
    -   [Исключения](language.exceptions.md)
    -   [Fibers](language.fibers.md)
    -   [Генератори](language.generators.md)
    -   [Атрибути](language.attributes.md)
    -   [Пояснення посилань](language.references.md)
    -   [Зумовлені змінні](reserved.variables.md)
    -   [Обумовлені винятки](reserved.exceptions.md)
    -   [Вбудовані інтерфейси та класи](reserved.interfaces.md)
    -   [Контекстні опції та параметри](context.md)
    -   [Підтримувані протоколи та обгортки](wrappers.md)
-   [Безпека](security.md)
    -   [Вступление](security.intro.md)
    -   [Общие рассуждения](security.general.md)
    -   [Если PHP установлен как CGI](security.cgi-bin.html)
    -   [Если PHP установлен как модуль Apache](security.apache.md)
    -   [Безпека сесій](security.sessions.md)
    -   [Безпека файлової системи](security.filesystem.md)
    -   [Безпека баз даних](security.database.md)
    -   [Повідомлення про помилки](security.errors.md)
    -   [Дані, введені користувачем](security.variables.md)
    -   [Приховування PHP](security.hiding.md)
    -   [Необходимость обновлений](security.current.md)
-   [Відмітні особливості](features.md)
    -   [HTTP-автентифікація в PHP](features.http-auth.html)
    -   [Cookies](features.cookies.md)
    -   [Сессии](features.sessions.md)
    -   [Работа с XForms](features.xforms.md)
    -   [Загрузка файлов на сервер](features.file-upload.html)
    -   [Робота з віддаленими файлами](features.remote-files.html)
    -   [Работа с соединениями](features.connection-handling.html)
    -   [Постійні з'єднання з базами даних](features.persistent-connections.html)
    -   [Використання PHP у командному рядку](features.commandline.md)
    -   [Сборка мусора](features.gc.md)
    -   [Динамічна трасування DTrace](features.dtrace.md)
-   [Справочник функций](funcref.md)
    -   [Изменение поведения PHP](refs.basic.php.md)
    -   [Обработка аудио форматов](refs.utilspec.audio.md)
    -   [Служби автентифікації](refs.remote.auth.md)
    -   [Модулі для роботи з командним рядком](refs.utilspec.cmdline.md)
    -   [Модулі для стиснення та архівації](refs.compression.md)
    -   [Криптографічні модулі](refs.crypto.md)
    -   [Модулі для роботи з базами даних](refs.database.md)
    -   [Модулі для роботи з датою та часом](refs.calendar.md)
    -   [Модулі для роботи з файловою системою](refs.fileprocess.file.md)
    -   [Підтримка мов та кодувань](refs.international.md)
    -   [Обработка и генерация изображений](refs.utilspec.image.md)
    -   [Модулі для роботи з поштою](refs.remote.mail.md)
    -   [Математичні модулі](refs.math.md)
    -   [Генерація нетекстових MIME-форматів](refs.utilspec.nontext.md)
    -   [Модули для управления процессами программ](refs.fileprocess.process.md)
    -   [Інші базові модулі](refs.basic.other.md)
    -   [Інші служби](refs.remote.other.md)
    -   [Модулі для роботи з пошуковими системами](refs.search.md)
    -   [Модулі для роботи із серверами](refs.utilspec.server.md)
    -   [Модулі для роботи із сесіями](refs.basic.session.md)
    -   [Обработка текста](refs.basic.text.md)
    -   [Модулі, що відносяться до змінних та типів](refs.basic.vartype.md)
    -   [Веб-сервіси](refs.webservice.md)
    -   [Модулі лише для Windows](refs.utilspec.windows.md)
    -   [Обработка XML](refs.xml.md)
    -   [Модулі для роботи з GUI](refs.ui.md)
-   [ЧАВО](faq.md) — ЧАВО: Часті питання та відповіді на них
    -   [Загальна інформація](faq.general.md)
    -   [Списки розсилки](faq.mailinglist.md)
    -   [Получение PHP](faq.obtaining.md)
    -   [Питання щодо баз даних](faq.databases.md) — Питання щодо Баз даних
    -   [Установка](faq.installation.md)
    -   [Проблеми збирання](faq.build.md)
    -   [Использование PHP](faq.using.md)
    -   [Хеширование паролей](faq.passwords.md) - Безпечне хешування паролів
    -   [PHP и HTML](faq.html.md)
    -   [PHP и COM](faq.com.md)
    -   [Різні питання](faq.misc.md)
-   [Appendices](appendices.md)
    -   [Історія PHP та суміжних проектів](history.md)
    -   [Миграция с PHP 8.0.x на PHP 8.1.x](migration81.md)
    -   [Миграция с PHP 7.4.x на PHP 8.0.x](migration80.md)
    -   [Миграция с PHP 7.3.x на PHP 7.4.x](migration74.md)
    -   [Миграция с PHP 7.2.x на PHP 7.3.x](migration73.md)
    -   [Миграция с PHP 7.1.x на PHP 7.2.x](migration72.md)
    -   [Миграция с PHP 7.0.x на PHP 7.1.x](migration71.md)
    -   [Миграция с PHP 5.6.x на PHP 7.0.x](migration70.md)
    -   [Миграция с PHP 5.5.x на PHP 5.6.x](migration56.md)
    -   [Отладка в PHP](debugger.md)
    -   [Опции конфигурации](configure.md)
    -   [Директиви php.ini](ini.md)
    -   [Список/класифікація модулів](extensions.md)
    -   [Список псевдонимов функций](aliases.md)
    -   [Список зарезервованих слів](reserved.md)
    -   [Список типов ресурсов](resource.md)
    -   [Список доступних фільтрів](filters.md)
    -   [Список підтримуваних транспортних протоколів](transports.md)
    -   [Таблица сравнения типов в PHP](types.comparisons.md)
    -   [Список меток (tokens) парсера](tokens.md)
    -   [Руководство по именованию](userlandnaming.md)
    -   [Про це керівництво](about.md)
    -   [Creative Commons Attribution 3.0](cc.license.md)
    -   [Алфавітний перелік](indexes.md)
    -   [Список изменений](doc.changelog.md)