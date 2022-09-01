---
navigation:
  - wrappers.expect.md: '« expect://'
  - security.intro.md: Вступление »
  - index.md: PHP Manual
title: Безпека
---
# Безпека

-   [Вступление](security.intro.md)
-   [Общие рассуждения](security.general.md)
-   [Если PHP установлен как CGI](security.cgi-bin.md)
    -   [Можливі атаки](security.cgi-bin.attacks.md)
    -   [Варіант 1: обслуговуються лише загальнодоступні файли](security.cgi-bin.default.md)
    -   [Вариант 2: использование cgi.forceredirect](security.cgi-bin.force-redirect.md)
    -   [Вариант 3: использование опций docroot или userdir](security.cgi-bin.doc-root.md)
    -   [Варіант 4: PHP поза деревом веб-документів](security.cgi-bin.shell.md)
-   [Если PHP установлен как модуль Apache](security.apache.md)
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
-   [Необходимость обновлений](security.current.md)
