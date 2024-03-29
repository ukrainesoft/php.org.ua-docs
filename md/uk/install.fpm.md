---
navigation:
  - install.cloud.ec2.md: « Amazon EC2
  - install.fpm.install.md: Встановлення »
  - index.md: PHP Manual
  - install.md: Встановлення та налаштування
title: Менеджер процесів FastCGI (FPM)
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Менеджер процесів FastCGI (FPM)

## Зміст

-   [Установка](install.fpm.install.md)
-   [Налаштування](install.fpm.configuration.md)

FPM (FastCGI Process Manager, менеджер процесів FastCGI) є альтернативною реалізацією PHP FastCGI з кількома додатковими можливостями, що зазвичай використовуються для високонавантажених сайтів.

Ці можливості включають:

-   Просунуте управління процесами з коректною (graceful) процедурою зупинки та запуску;
    
-   Пули, що дають можливість запуску воркерів з різними uid/gid/chroot/оточенням, прослуховуючи різні порти та використовуючи різні php.ini (заміщення safe\_mode);
    
-   Настроювання ведення журналу потоків виведення (stdout) і помилок (stderr);
    
-   Аварійний перезапуск у разі раптового руйнування opcode-кешу;
    
-   Підтримка прискореного завантаження (accelerated upload);
    
-   "slowlog" - логування скриптів, що незвичайно повільно виконуються (не тільки їх імена, але також і їх трасування. Це досягається за допомогою ptrace та інших подібних утиліт для читання даних виконання віддалених процесів);
    
-   [fastcgi\_finish\_request()](function.fastcgi-finish-request.md) \- спеціальна функція для завершення запиту та скидання всіх буферів даних, причому процес може продовжувати виконання будь-яких тривалих дій (конвертування відео, обробка статистики тощо);
    
-   Динамічне/на вимогу/статичне породження дочірніх процесів;
    
-   Базова та розширена інформація про стан (аналогічно Apache mod\_status) з підтримкою різних форматів, таких як json, xml та openmetrics;
    
-   Конфігураційний файл, що базується на php.ini.
