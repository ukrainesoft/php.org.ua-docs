Управління сесіями

-   [« Модули для работы с сессиями](refs.basic.session.html)
    
-   [Введение »](intro.session.html)
    
-   [PHP Manual](index.html)
    
-   [Модули для работы с сессиями](refs.basic.session.html)
    
-   Управління сесіями
    

# Управління сесіями

-   [Введение](intro.session.html)
-   [Установка и настройка](session.setup.html)
    -   [Требования](session.requirements.html)
    -   [Установка](session.installation.html)
    -   [Настройка во время выполнения](session.configuration.html)
    -   [Типы ресурсов](session.resources.html)
-   [Предопределённые константы](session.constants.html)
-   [Примеры](session.examples.html)
    -   [Основы использования](session.examples.basic.html)
    -   [Передача идентификатора сессии](session.idpassing.html)
    -   [Пользовательские обработчики сессии](session.customhandler.html)
-   [Отслеживание прогресса загрузки файлов с помощью сессий](session.upload-progress.html)
-   [Безопасность сессий](session.security.html)
    -   [Базовые принципы управления сессиями](features.session.security.management.html)
    -   [INI-настройки безопасности сессий](session.security.ini.html)
-   [Функции для работы с сессиями](ref.session.html)
    -   [session\_abort](function.session-abort.html) — Скасує зміни у масиві сесії та завершує її
    -   [session\_cache\_expire](function.session-cache-expire.html) — Отримує та/або встановлює термін дії поточного кешу
    -   [session\_cache\_limiter](function.session-cache-limiter.html) — Отримати та/або встановити поточний режим кешування
    -   [session\_commit](function.session-commit.html) - Псевдонім sessionwriteclose
    -   [session\_create\_id](function.session-create-id.html) — Створює новий ідентифікатор сесії
    -   [session\_decode](function.session-decode.html) — Декодує дані сесії із закодованого рядка сесії
    -   [session\_destroy](function.session-destroy.html) — Знищує всі дані сесії
    -   [session\_encode](function.session-encode.html) — Кодує дані поточної сесії у форматі рядка сесії
    -   [session\_gc](function.session-gc.html) — Виконує складання сміття даних сесії
    -   [session\_get\_cookie\_params](function.session-get-cookie-params.html) — Повертає параметри cookie сесії
    -   [session\_id](function.session-id.html) — Отримує та/або встановлює ідентифікатор поточної сесії
    -   [session\_module\_name](function.session-module-name.html) — Повертає та/або встановлює модуль поточної сесії
    -   [session\_name](function.session-name.html) — Отримати або встановити ім'я поточної сесії
    -   [session\_regenerate\_id](function.session-regenerate-id.html) — Генерує та оновлює ідентифікатор поточної сесії
    -   [session\_register\_shutdown](function.session-register-shutdown.html) - Функція завершення сесії
    -   [session\_reset](function.session-reset.html) — Реініціалізує сесію оригінальними значеннями
    -   [session\_save\_path](function.session-save-path.html) — Отримує та/або встановлює шлях збереження сесії
    -   [session\_set\_cookie\_params](function.session-set-cookie-params.html) — Встановлює параметри сесійної cookie
    -   [session\_set\_save\_handler](function.session-set-save-handler.html) - Встановлює користувальницькі обробники зберігання сесії
    -   [session\_start](function.session-start.html) — Стартує нову сесію або відновлює існуючу
    -   [session\_status](function.session-status.html) — Повертає стан поточної сесії
    -   [session\_unset](function.session-unset.html) — Видалити всі змінні сесії
    -   [session\_write\_close](function.session-write-close.html) — Записує дані сесії та завершує її
-   [SessionHandler](class.sessionhandler.html) - Клас SessionHandler
    -   [SessionHandler::close](sessionhandler.close.html) - Закриває сесію
    -   [SessionHandler::create\_sid](sessionhandler.create-sid.html) — Повертає новий ідентифікатор сесії
    -   [SessionHandler::destroy](sessionhandler.destroy.html) - Знищує сесію
    -   [SessionHandler::gc](sessionhandler.gc.html) - Очищає старі сесії
    -   [SessionHandler::open](sessionhandler.open.html) - Ініціалізує сесію
    -   [SessionHandler::read](sessionhandler.read.html) — Зчитує дані сесії
    -   [SessionHandler::write](sessionhandler.write.html) — Записує дані сесії
-   [SessionHandlerInterface](class.sessionhandlerinterface.html) - Клас SessionHandlerInterface
    -   [SessionHandlerInterface::close](sessionhandlerinterface.close.html) - Закриває сесію
    -   [SessionHandlerInterface::destroy](sessionhandlerinterface.destroy.html) - Знищує сесію
    -   [SessionHandlerInterface::gc](sessionhandlerinterface.gc.html) - Очищає старі сесії
    -   [SessionHandlerInterface::open](sessionhandlerinterface.open.html) - Ініціалізує сесію
    -   [SessionHandlerInterface::read](sessionhandlerinterface.read.html) — Читає дані сесії
    -   [SessionHandlerInterface::write](sessionhandlerinterface.write.html) — Записати дані сесії
-   [SessionIdInterface](class.sessionidinterface.html) - Інтерфейс SessionIdInterface
    -   [SessionIdInterface::create\_sid](sessionidinterface.create-sid.html) — Створити ідентифікатор сесії
-   [SessionUpdateTimestampHandlerInterface](class.sessionupdatetimestamphandlerinterface.html) — Інтерфейс SessionUpdateTimestampHandlerInterface
    -   [SessionUpdateTimestampHandlerInterface::updateTimestamp](sessionupdatetimestamphandlerinterface.updatetimestamp.html) — Оновити позначку часу
    -   [SessionUpdateTimestampHandlerInterface::validateId](sessionupdatetimestamphandlerinterface.validateid.html) - Перевірити ідентифікатор