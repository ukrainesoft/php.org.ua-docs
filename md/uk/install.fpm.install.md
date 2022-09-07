---
navigation:
  - install.fpm.md: Менеджер процесів FastCGI (FPM)
  - install.fpm.configuration.md: Настройка »
  - index.md: PHP Manual
  - install.fpm.md: Менеджер процесів FastCGI (FPM)
title: Встановлення
---
## Встановлення

### Компіляція з вихідних джерел

Для того, щоб увімкнути FPM під час складання PHP, додайте рядок `--enable-fpm`

Існують також кілька інших опцій конфігурації FPM (усі опціональні):

-   `--with-fpm-user` - Встановити користувача FPM (за замовчуванням - nobody).
    
-   `--with-fpm-group` - встановити групу FPM (за замовчуванням – nobody).
    
-   `--with-fpm-systemd` - Включити інтеграцію з systemd (за замовчуванням – no).
    
-   `--with-fpm-acl` - Використовувати списки керування доступом (ACL) POSIX (за замовчуванням – no).
    
-   `--with-fpm-apparmor` - Активувати інтеграцію з AppArmor (за замовчуванням – no).
    

### список змін

| Версия | Описание |
| --- | --- |
|  | Додана опція `--with-fpm-apparmor` |
