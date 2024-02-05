---
navigation:
  - function.mail.md: « mail
  - intro.mailparse.md: Вступ "
  - index.md: PHP Manual
  - refs.remote.mail.md: Модулі для роботи з поштою
title: Mailparse
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Mailparse

-   [Вступ](intro.mailparse.md)
-   [Встановлення та налаштування](mailparse.setup.md)
    -   [Вимоги](mailparse.requirements.md)
    -   [Установка](mailparse.installation.md)
    -   [Налаштування під час виконання](mailparse.configuration.md)
    -   [Типи ресурсів](mailparse.resources.md)
-   [Обумовлені константи](mailparse.constants.md)
-   [Mailparse](ref.mailparse.md)
    -   [mailparse\_determine\_best\_xfer\_encoding](function.mailparse-determine-best-xfer-encoding.md) \- Визначити найкращий шлях декодування
    -   [mailparse\_msg\_create](function.mailparse-msg-create.md) \- Створює поштовий MIME-ресурс
    -   [mailparse\_msg\_extract\_part\_file](function.mailparse-msg-extract-part-file.md)— Вийняти/декодувати секцію із повідомленням із файлу
    -   [mailparse\_msg\_extract\_part](function.mailparse-msg-extract-part.md)— Вийняти/декодувати секцію із повідомленням
    -   [mailparse\_msg\_extract\_whole\_part\_file](function.mailparse-msg-extract-whole-part-file.md)— Витягти секцію повідомлення разом із заголовками без декодування
    -   [mailparse\_msg\_free](function.mailparse-msg-free.md) \- Вивільнити MIME-ресурс
    -   [mailparse\_msg\_get\_part\_data](function.mailparse-msg-get-part-data.md)— Повернути асоціативний масив із інформацією про повідомлення
    -   [mailparse\_msg\_get\_part](function.mailparse-msg-get-part.md)— Повертає покажчик на задану секцію у mime-повідомленні
    -   [mailparse\_msg\_get\_structure](function.mailparse-msg-get-structure.md)— Отримати масив імен mime-секцій у заданому повідомленні
    -   [mailparse\_msg\_parse\_file](function.mailparse-msg-parse-file.md) \- Розібрати файл
    -   [mailparse\_msg\_parse](function.mailparse-msg-parse.md) \- Інкрементальне розбирає дані у буфер
    -   [mailparse\_rfc822\_parse\_addresses](function.mailparse-rfc822-parse-addresses.md)— Розібрати адреси відповідно до RFC 822
    -   [mailparse\_stream\_encode](function.mailparse-stream-encode.md)— Кодує потік із файлу джерела та пише у файл одержувач.
    -   [mailparse\_uudecode\_all](function.mailparse-uudecode-all.md)— Сканує дані із зазначеного файлу та витягує всі вкладені файли, кодовані в uuencode
