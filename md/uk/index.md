Посібник з PHP

-   [Авторские права »](copyright.html)
    
-   [PHP Manual](index.html)
    
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

-   [Авторские права](copyright.html)
-   [Руководство по PHP](manual.html)
    -   [Предисловие](preface.html)
-   [Приступаючи до роботи](getting-started.html)
    -   [Введение](introduction.html)
    -   [Простий підручник](tutorial.html)
-   [Установка и настройка](install.html)
    -   [Общие инструкции по установке](install.general.html)
    -   [Установка на Unix-системы](install.unix.html)
    -   [Установка на macOS](install.macosx.html)
    -   [Установка в системах Windows](install.windows.html)
    -   [Установка на платформах Cloud Computing](install.cloud.html)
    -   [Менеджер процесів FastCGI (FPM)](install.fpm.html)
    -   [Установка модулей PECL](install.pecl.html)
    -   [Проблемы?](install.problems.html)
    -   [Конфигурация времени выполнения](configuration.html)
-   [Справочник языка](langref.html)
    -   [Основы синтаксиса](language.basic-syntax.html)
    -   [Типы](language.types.html)
    -   [Переменные](language.variables.html)
    -   [Константы](language.constants.html)
    -   [Выражения](language.expressions.html)
    -   [Оператори](language.operators.html)
    -   [Управляющие конструкции](language.control-structures.html)
    -   [Функції](language.functions.html)
    -   [Классы и объекты](language.oop5.html)
    -   [Пространства имён](language.namespaces.html)
    -   [Перечисления](language.enumerations.html)
    -   [Ошибки](language.errors.html)
    -   [Исключения](language.exceptions.html)
    -   [Fibers](language.fibers.html)
    -   [Генераторы](language.generators.html)
    -   [Атрибуты](language.attributes.html)
    -   [Объяснение ссылок](language.references.html)
    -   [Предопределённые переменные](reserved.variables.html)
    -   [Предопределённые исключения](reserved.exceptions.html)
    -   [Вбудовані інтерфейси та класи](reserved.interfaces.html)
    -   [Контекстные опции и параметры](context.html)
    -   [Підтримувані протоколи та обгортки](wrappers.html)
-   [Безпека](security.html)
    -   [Вступление](security.intro.html)
    -   [Общие рассуждения](security.general.html)
    -   [Если PHP установлен как CGI](security.cgi-bin.html)
    -   [Если PHP установлен как модуль Apache](security.apache.html)
    -   [Безпека сесій](security.sessions.html)
    -   [Безпека файлової системи](security.filesystem.html)
    -   [Безпека баз даних](security.database.html)
    -   [Повідомлення про помилки](security.errors.html)
    -   [Дані, введені користувачем](security.variables.html)
    -   [Приховування PHP](security.hiding.html)
    -   [Необходимость обновлений](security.current.html)
-   [Відмітні особливості](features.html)
    -   [HTTP-автентифікація в PHP](features.http-auth.html)
    -   [Cookies](features.cookies.html)
    -   [Сессии](features.sessions.html)
    -   [Работа с XForms](features.xforms.html)
    -   [Загрузка файлов на сервер](features.file-upload.html)
    -   [Робота з віддаленими файлами](features.remote-files.html)
    -   [Работа с соединениями](features.connection-handling.html)
    -   [Постійні з'єднання з базами даних](features.persistent-connections.html)
    -   [Використання PHP у командному рядку](features.commandline.html)
    -   [Сборка мусора](features.gc.html)
    -   [Динамічна трасування DTrace](features.dtrace.html)
-   [Справочник функций](funcref.html)
    -   [Изменение поведения PHP](refs.basic.php.html)
    -   [Обработка аудио форматов](refs.utilspec.audio.html)
    -   [Служби автентифікації](refs.remote.auth.html)
    -   [Модулі для роботи з командним рядком](refs.utilspec.cmdline.html)
    -   [Модулі для стиснення та архівації](refs.compression.html)
    -   [Криптографічні модулі](refs.crypto.html)
    -   [Модулі для роботи з базами даних](refs.database.html)
    -   [Модулі для роботи з датою та часом](refs.calendar.html)
    -   [Модулі для роботи з файловою системою](refs.fileprocess.file.html)
    -   [Підтримка мов та кодувань](refs.international.html)
    -   [Обработка и генерация изображений](refs.utilspec.image.html)
    -   [Модулі для роботи з поштою](refs.remote.mail.html)
    -   [Математичні модулі](refs.math.html)
    -   [Генерація нетекстових MIME-форматів](refs.utilspec.nontext.html)
    -   [Модули для управления процессами программ](refs.fileprocess.process.html)
    -   [Інші базові модулі](refs.basic.other.html)
    -   [Другие службы](refs.remote.other.html)
    -   [Модулі для роботи з пошуковими системами](refs.search.html)
    -   [Модулі для роботи із серверами](refs.utilspec.server.html)
    -   [Модулі для роботи із сесіями](refs.basic.session.html)
    -   [Обработка текста](refs.basic.text.html)
    -   [Модули, относящиеся к переменным и типам](refs.basic.vartype.html)
    -   [Веб-сервисы](refs.webservice.html)
    -   [Модулі лише для Windows](refs.utilspec.windows.html)
    -   [Обработка XML](refs.xml.html)
    -   [Модулі для роботи з GUI](refs.ui.html)
-   [ЧАВО](faq.html) — ЧАВО: Часті питання та відповіді на них
    -   [Загальна інформація](faq.general.html)
    -   [Списки рассылки](faq.mailinglist.html)
    -   [Получение PHP](faq.obtaining.html)
    -   [Питання щодо баз даних](faq.databases.html) — Питання щодо Баз даних
    -   [Установка](faq.installation.html)
    -   [Проблемы сборки](faq.build.html)
    -   [Использование PHP](faq.using.html)
    -   [Хеширование паролей](faq.passwords.html) - Безпечне хешування паролів
    -   [PHP и HTML](faq.html.html)
    -   [PHP и COM](faq.com.html)
    -   [Різні питання](faq.misc.html)
-   [Appendices](appendices.html)
    -   [Історія PHP та суміжних проектів](history.html)
    -   [Миграция с PHP 8.0.x на PHP 8.1.x](migration81.html)
    -   [Миграция с PHP 7.4.x на PHP 8.0.x](migration80.html)
    -   [Миграция с PHP 7.3.x на PHP 7.4.x](migration74.html)
    -   [Миграция с PHP 7.2.x на PHP 7.3.x](migration73.html)
    -   [Миграция с PHP 7.1.x на PHP 7.2.x](migration72.html)
    -   [Миграция с PHP 7.0.x на PHP 7.1.x](migration71.html)
    -   [Миграция с PHP 5.6.x на PHP 7.0.x](migration70.html)
    -   [Миграция с PHP 5.5.x на PHP 5.6.x](migration56.html)
    -   [Отладка в PHP](debugger.html)
    -   [Опции конфигурации](configure.html)
    -   [Директивы php.ini](ini.html)
    -   [Список/класифікація модулів](extensions.html)
    -   [Список псевдонимов функций](aliases.html)
    -   [Список зарезервованих слів](reserved.html)
    -   [Список типов ресурсов](resource.html)
    -   [Список доступних фільтрів](filters.html)
    -   [Список підтримуваних транспортних протоколів](transports.html)
    -   [Таблица сравнения типов в PHP](types.comparisons.html)
    -   [Список меток (tokens) парсера](tokens.html)
    -   [Руководство по именованию](userlandnaming.html)
    -   [Про це керівництво](about.html)
    -   [Creative Commons Attribution 3.0](cc.license.html)
    -   [Алфавитный список](indexes.html)
    -   [Список изменений](doc.changelog.html)