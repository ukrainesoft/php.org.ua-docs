---
navigation:
  - soapvar.construct.md: '« SoapVar::construct'
  - intro.yar.md: Введение »
  - index.md: PHP Manual
  - refs.webservice.md: Веб-сервіси
title: Ще один RPC-фреймворк
---
# Ще один RPC-фреймворк

-   [Введение](intro.yar.md)
-   [Встановлення та налаштування](yar.setup.md)
    -   [Вимоги](yar.requirements.md)
    -   [Установка](yar.installation.md)
    -   [Налаштування під час виконання](yar.configuration.md)
    -   [Типи ресурсів](yar.resources.md)
-   [Обумовлені константи](yar.constants.md)
-   [Приклади](yar.examples.md)
-   [YarServer](class.yar-server.md) - Клас YarServer
    -   [YarServer::construct](yar-server.construct.md) - Конструктор YarServer
    -   [YarServer::handle](yar-server.handle.md) — Запустити сервер RPC
-   [YarClient](class.yar-client.md) - Клас YarClient
    -   [YarClient::call](yar-client.call.md) - Виклик сервісу
    -   [YarClient::construct](yar-client.construct.md) - Конструктор YarClient
    -   [YarClient::setOpt](yar-client.setopt.md) — Задати контекст дзвінка
-   [YarConcurrentClient](class.yar-concurrent-client.md) - Клас YarConcurrentClient
    -   [YarConcurrentClient::call](yar-concurrent-client.call.md) — Зареєструвати конкурентний виклик
    -   [YarConcurrentClient::loop](yar-concurrent-client.loop.md) — Запуск усіх зареєстрованих викликів
    -   [YarConcurrentClient::reset](yar-concurrent-client.reset.md) — Очистити всі зареєстровані дзвінки
-   [YarServerException](class.yar-server-exception.md) - Клас YarServerException
    -   [YarServerException::getType](yar-server-exception.gettype.md) — Отримати тип виключення
-   [YarClientException](class.yar-client-exception.md) - Клас YarClientException
    -   [YarClientException::getType](yar-client-exception.gettype.md) — Отримати тип виключення
