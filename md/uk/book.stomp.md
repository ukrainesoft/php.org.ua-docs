Stomp Client

-   [« ssh2\_tunnel](function.ssh2-tunnel.html)
    
-   [Введение »](intro.stomp.html)
    
-   [PHP Manual](index.html)
    
-   [Другие службы](refs.remote.other.html)
    
-   Stomp Client
    

# Stomp Client

-   [Введение](intro.stomp.html)
-   [Установка и настройка](stomp.setup.html)
    -   [Требования](stomp.requirements.html)
    -   [Установка](stomp.installation.html)
    -   [Настройка во время выполнения](stomp.configuration.html)
    -   [Типы ресурсов](stomp.resources.html)
-   [Примеры](stomp.examples.html)
-   [Функции Stomp](ref.stomp.html)
    -   [stomp\_connect\_error](function.stomp-connect-error.html) — Повертає рядок із описом останньої помилки підключення
    -   [stomp\_version](function.stomp-version.html) — Повертає поточну версію модуля Stomp
-   [Stomp](class.stomp.html) - Клас Stomp
    -   [Stomp::abort](stomp.abort.html) — Скасує виконання поточної транзакції
    -   [Stomp::ack](stomp.ack.html) — Підтверджує отримання повідомлення
    -   [Stomp::begin](stomp.begin.html) - Створює транзакцію
    -   [Stomp::commit](stomp.commit.html) — Виконує поточну транзакцію
    -   [Stomp::\_\_construct](stomp.construct.html) - Відкриває з'єднання
    -   [Stomp::\_\_destruct](stomp.destruct.html) - Закриває Stomp-з'єднання
    -   [Stomp::error](stomp.error.html) - Повертає останню помилку Stomp
    -   [Stomp::getReadTimeout](stomp.getreadtimeout.html) — Повертає час максимального очікування на операцію читання
    -   [Stomp::getSessionId](stomp.getsessionid.html) - Повертає ідентифікатор поточної сесії Stomp
    -   [Stomp::hasFrame](stomp.hasframe.html) — Перевіряє, чи можливе читання кадру
    -   [Stomp::readFrame](stomp.readframe.html) — Виконує операцію для читання наступного кадру
    -   [Stomp::send](stomp.send.html) — Надсилає повідомлення
    -   [Stomp::setReadTimeout](stomp.setreadtimeout.html) - Встановлює граничний час очікування операції читання
    -   [Stomp::subscribe](stomp.subscribe.html) — Реєструє передплату на вказану розсилку
    -   [Stomp::unsubscribe](stomp.unsubscribe.html) — Видаляє існуючу передплату
-   [StompFrame](class.stompframe.html) - Клас StompFrame
    -   [StompFrame::\_\_construct](stompframe.construct.html) - Конструктор
-   [StompException](class.stompexception.html) - Клас StompException
    -   [StompException::getDetails](stomp.getdetails.html) — Повертає відомості про виключення