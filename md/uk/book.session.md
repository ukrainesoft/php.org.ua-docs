Управління сесіями

-   [« Модулі для роботи з сесіями](refs.basic.session.html)
    
-   [Введение »](intro.session.html)
    
-   [PHP Manual](index.html)
    
-   [Модулі для роботи із сесіями](refs.basic.session.html)
    
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
    -   [Користувальницькі обробники сесії](session.customhandler.html)
-   [Отслеживание прогресса загрузки файлов с помощью сессий](session.upload-progress.html)
-   [Безпека сесій](session.security.html)
    -   [Базовые принципы управления сессиями](features.session.security.management.html)
    -   [INI-налаштування безпеки сесій](session.security.ini.html)
-   [Функції для роботи із сесіями](ref.session.html)
    -   [sessionabort](function.session-abort.html) — Скасує зміни у масиві сесії та завершує її
    -   [sessioncacheexpire](function.session-cache-expire.html) — Отримує та/або встановлює термін дії поточного кешу
    -   [sessioncachelimiter](function.session-cache-limiter.html) — Отримати та/або встановити поточний режим кешування
    -   [sessioncommit](function.session-commit.html) - Псевдонім sessionwriteclose
    -   [sessioncreateід](function.session-create-id.html) — Створює новий ідентифікатор сесії
    -   [sessiondecode](function.session-decode.html) — Декодує дані сесії із закодованого рядка сесії
    -   [sessiondestroy](function.session-destroy.html) — Знищує всі дані сесії
    -   [sessionencode](function.session-encode.html) — Кодує дані поточної сесії у форматі рядка сесії
    -   [sessionгк](function.session-gc.html) — Виконує складання сміття даних сесії
    -   [sessiongetcookieparams](function.session-get-cookie-params.html) — Повертає параметри cookie сесії
    -   [sessionід](function.session-id.html) — Отримує та/або встановлює ідентифікатор поточної сесії
    -   [sessionmodulename](function.session-module-name.html) — Повертає та/або встановлює модуль поточної сесії
    -   [sessionname](function.session-name.html) — Отримати або встановити ім'я поточної сесії
    -   [sessionregenerateід](function.session-regenerate-id.html) — Генерує та оновлює ідентифікатор поточної сесії
    -   [sessionregistershutdown](function.session-register-shutdown.html) - Функція завершення сесії
    -   [sessionreset](function.session-reset.html) — Реініціалізує сесію оригінальними значеннями
    -   [sessionsavepath](function.session-save-path.html) — Отримує та/або встановлює шлях збереження сесії
    -   [sessionsetcookieparams](function.session-set-cookie-params.html) — Встановлює параметри сесійної cookie
    -   [sessionsetsavehandler](function.session-set-save-handler.html) - Встановлює користувальницькі обробники зберігання сесії
    -   [sessionstart](function.session-start.html) — Стартує нову сесію або відновлює існуючу
    -   [sessionstatus](function.session-status.html) — Повертає стан поточної сесії
    -   [sessionunset](function.session-unset.html) — Видалити всі змінні сесії
    -   [sessionwriteclose](function.session-write-close.html) — Записує дані сесії та завершує її
-   [SessionHandler](class.sessionhandler.html) - Клас SessionHandler
    -   [SessionHandler::close](sessionhandler.close.html) - Закриває сесію
    -   [SessionHandler::createsid](sessionhandler.create-sid.html) — Повертає новий ідентифікатор сесії
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
    -   [SessionIdInterface::createsid](sessionidinterface.create-sid.html) — Створити ідентифікатор сесії
-   [SessionUpdateTimestampHandlerInterface](class.sessionupdatetimestamphandlerinterface.html) — Інтерфейс SessionUpdateTimestampHandlerInterface
    -   [SessionUpdateTimestampHandlerInterface::updateTimestamp](sessionupdatetimestamphandlerinterface.updatetimestamp.html) — Оновити позначку часу
    -   [SessionUpdateTimestampHandlerInterface::validateId](sessionupdatetimestamphandlerinterface.validateid.html) - Перевірити ідентифікатор