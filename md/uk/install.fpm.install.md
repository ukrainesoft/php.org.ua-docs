---
navigation:
  - install.fpm.md: Менеджер процесів FastCGI (FPM)
  - install.fpm.configuration.md: Налаштування "
  - index.md: PHP Manual
  - install.fpm.md: Менеджер процесів FastCGI (FPM)
title: Установка
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Установка

### Компіляція з вихідних джерел

Для того, щоб увімкнути FPM під час складання PHP, додайте рядок `--enable-fpm`

Існують також кілька інших опцій конфігурації FPM (усі опціональні):

-   `--with-fpm-user`\- Встановити користувача FPM (за замовчуванням - nobody).
    
-   `--with-fpm-group`\- встановити групу FPM (за замовчуванням – nobody).
    
-   `--with-fpm-systemd`\- Включити інтеграцію з systemd (за замовчуванням – no).
    
-   `--with-fpm-acl`\- Використовувати списки керування доступом (ACL) POSIX (за замовчуванням – no).
    
-   `--with-fpm-apparmor`\- Активувати інтеграцію з AppArmor (за замовчуванням – no).
    
-   `--with-fpm-selinux`\- Активувати інтеграцію з SELinux (за замовчуванням – no).
    

### список змін

| Версия | Опис |
| --- | --- |
| 8.2.0 | Добавлена опция`--with-fpm-selinux` |
| 8.0.0 | Добавлена опция`--with-fpm-apparmor` |
