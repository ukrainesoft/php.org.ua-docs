---
navigation:
  - sockets.examples.md: « Приклади
  - ref.sockets.md: Опції сокету »
  - index.md: PHP Manual
  - book.sockets.md: Сокети
title: Помилки сокетів
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Помилки сокетів

Модуль socket був написаний для забезпечення зручного інтерфейсу до BSD сокетів. Були вжиті необхідні заходи для того, щоб ці функції працювали однаково добре в реалізації як Win32, так і Unix. Майже всі функції, за певних умов, можуть завершитися з помилкою та викликають помилку рівня **`E_WARNING`**. Іноді розробники перешкоджають цьому. Наприклад, функція [socket\_read()](function.socket-read.md) може раптово викликати помилку рівня \*\*`E_WARNING`\*\*тому, що з'єднання несподівано обірвалося. Звичайна практика придушувати попередження за допомогою оператора `@` та перехоплювати код помилки у додатку за допомогою функції [socket\_last\_error()](function.socket-last-error.md). Ви можете викликати функцію [socket\_strerror()](function.socket-strerror.md) з кодом помилки для отримання рядка, що описує помилку. Дивіться опис цих функцій для більш детальної інформації.

> **Зауваження** :
> 
> Сообщения\*\*`E_WARNING`**, що викликаються модулем socket, будуть англійською мовою, а отримане повідомлення про помилку з'являтиметься залежно від налаштувань поточної локалі (**`LC_MESSAGES`\*\*):
> 
> ```
> Warning - socket_bind() unable to bind address [98]: Die Adresse wird bereits verwendet
> ```
