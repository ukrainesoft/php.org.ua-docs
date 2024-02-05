---
navigation:
  - function.ssh2-tunnel.md: « ssh2\_tunnel
  - intro.stomp.md: Вступ "
  - index.md: PHP Manual
  - refs.remote.other.md: Інші служби
title: Stomp Client
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Stomp Client

-   [Вступ](intro.stomp.md)
-   [Встановлення та налаштування](stomp.setup.md)
    -   [Вимоги](stomp.requirements.md)
    -   [Установка](stomp.installation.md)
    -   [Налаштування під час виконання](stomp.configuration.md)
    -   [Типи ресурсів](stomp.resources.md)
-   [Приклади](stomp.examples.md)
-   [Опції Stomp](ref.stomp.md)
    -   [stomp\_connect\_error](function.stomp-connect-error.md)— Повертає рядок із описом останньої помилки підключення
    -   [stomp\_version](function.stomp-version.md)— Повертає поточну версію модуля Stomp
-   [Stomp](class.stomp.md) \- Клас Stomp
    -   [Stomp::abort](stomp.abort.md)— Скасує виконання поточної транзакції
    -   [Stomp::ack](stomp.ack.md)— Підтверджує отримання повідомлення
    -   [Stomp::begin](stomp.begin.md) \- Створює транзакцію
    -   [Stomp::commit](stomp.commit.md) \- Виконує поточну транзакцію
    -   [Stomp::\_\_construct](stomp.construct.md) \- Відкриває з'єднання
    -   [Stomp::\_\_destruct](stomp.destruct.md) \- Закриває Stomp-з'єднання
    -   [Stomp::error](stomp.error.md) \- Повертає останню помилку Stomp
    -   [Stomp::getReadTimeout](stomp.getreadtimeout.md)— Повертає час максимального очікування на операцію читання
    -   [Stomp::getSessionId](stomp.getsessionid.md) \- Повертає ідентифікатор поточної сесії Stomp
    -   [Stomp::hasFrame](stomp.hasframe.md)— Перевіряє, чи можливе читання кадру
    -   [Stomp::readFrame](stomp.readframe.md)— Виконує операцію для читання наступного кадру
    -   [Stomp::send](stomp.send.md)— Надсилає повідомлення
    -   [Stomp::setReadTimeout](stomp.setreadtimeout.md)— Встановлює граничний час очікування на операцію читання
    -   [Stomp::subscribe](stomp.subscribe.md)— Реєструє передплату на вказану розсилку
    -   [Stomp::unsubscribe](stomp.unsubscribe.md)— Видаляє існуючу передплату
-   [StompFrame](class.stompframe.md) \- Клас StompFrame
    -   [StompFrame::\_\_construct](stompframe.construct.md) \- Конструктор
-   [StompException](class.stompexception.md) \- Клас StompException
    -   [StompException::getDetails](stomp.getdetails.md)— Повертає відомості про виключення
