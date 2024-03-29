---
navigation:
  - oci8.connection.md: « Робота зі з'єднаннями OCI8 та Connection Pooling
  - oci8.taf.md: >-
      Підтримка прозорого для програм відновлення після відмови (Transparent
      Application Failover або TAF) для OCI8 »
  - index.md: PHP Manual
  - book.oci8.md: OCI8
title: Підтримка OCI8 Fast Application Notification (FAN)
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Підтримка OCI8 Fast Application Notification (FAN)

Підтримка FAN забезпечує швидке перепідключення у разі збоїв, що забезпечує високу доступність бази даних Oracle. Ця функціональність дозволяє PHP OCI8 скрипту отримувати оповіщення у випадку, якщо база даних або сервер, на якому вона запущена, стають недоступними. Без FAN, OCI8 може підвиснути, поки не буде перевищено час очікування підключення та повернено помилку, що може тривати кілька хвилин. Дозвіл FAN у OCI8 дозволяє програмам визначати такі помилки та перепідключатися до доступного екземпляра бази даних без очікування відповіді від недоступної бази.

Підтримка FAN доступна, якщо клієнтські бібліотеки Oracle, з якими зібрано PHP, і база даних Oracle мають версію 10gR2 або пізнішу.

FAN дає переваги користувачам кластерної технології Oracle (RAC), оскільки підключення до доступної бази даних може бути здійснено миттєво. Користувачі Oracle Data Guard з брокером можуть спостерігати події FAN, створені при переході резервної бази в режим основної. Окремі встановлені екземпляри бази даних надсилатимуть події FAN під час свого перезапуску.

Для активних з'єднань, коли сервер або екземпляр бази стають недоступними, повернеться помилка з'єднання для поточної запущеної функції модуля OCI8. При подальшому перепідключенні PHP-скрипту буде встановлено з'єднання з діючим екземпляром бази даних. Також модуль OCI8 прозоро зачищає всі з'єднання, що очікують, порушені падінням сервера або бази даних, так що нові з'єднання будуть нормально встановлюватися без огляду на будь-які проблеми з сервісом.

Якщо [oci8.events](oci8.configuration.md#ini.oci8.events)установлено как`On`, то передбачається, що [oci8.ping\_interval](oci8.configuration.md#ini.oci8.ping-interval) встановлено в -1, оскільки включення подій FAN надає проактивне управління очікуваними з'єднаннями.

Для включення підтримки FAN у PHP OCI8, зберіть PHP OCI8 з бібліотеками Oracle 10gR2 або пізнішими та виконайте такі кроки:

-   Під обліковим записом привілейованого адміністратора баз даних, за допомогою програм типу SQL\*Plus дозвольте сервісу бази відправляти оповіщення FAN, наприклад:
    
    ```
    SQL> execute dbms_service.modify_service(
                       SERVICE_NAME        => 'sales',
                       AQ_HA_NOTIFICATIONS => TRUE);
    ```
    
-   Додати до php.ini
    
    ```
    oci8.events = On
    ```
    
-   Якщо програма не обробляє помилки з'єднання OCI8, модифікуйте її таким чином, щоб обробляло та виробляло, наприклад, перепідключення та перезапуск запитів.
    
-   Запустіть програму, з'єднуючись з базою даних Oracle версії 10gR2 або вище.
