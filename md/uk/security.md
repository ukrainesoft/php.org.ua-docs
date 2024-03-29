---
navigation:
  - wrappers.expect.md: '« expect://'
  - security.intro.md: Вступ »
  - index.md: PHP Manual
title: Безпека
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Безпека

-   [Вступ](security.intro.md)
-   [Загальні міркування](security.general.md)
-   [Якщо PHP встановлено як CGI](security.cgi-bin.md)
    -   [Можливі атаки](security.cgi-bin.attacks.md)
    -   [Варіант 1: обслуговуються лише загальнодоступні файли](security.cgi-bin.default.md)
    -   [Варіант 2: використання cgi.force\_redirect](security.cgi-bin.force-redirect.md)
    -   [Варіант 3: використання опцій doc\_root або user\_dir](security.cgi-bin.doc-root.md)
    -   [Варіант 4: PHP поза деревом веб-документів](security.cgi-bin.shell.md)
-   [Якщо PHP встановлено як модуль Apache](security.apache.md)
-   [Безпека сесій](security.sessions.md)
-   [Безпека файлової системи](security.filesystem.md)
    -   [Проблеми безпеки, пов'язані з нульовим байтом](security.filesystem.nullbytes.md)
-   [Безпека баз даних](security.database.md)
    -   [Проектування бази даних](security.database.design.md)
    -   [З'єднання з базою даних](security.database.connection.md)
    -   [Шифрування сховища бази даних](security.database.storage.md)
    -   [SQL-ін'єкції](security.database.sql-injection.md)
-   [Повідомлення про помилки](security.errors.md)
-   [Дані, введені користувачем](security.variables.md)
-   [Приховування PHP](security.hiding.md)
-   [Необхідність оновлень](security.current.md)
