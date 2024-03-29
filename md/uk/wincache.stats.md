---
navigation:
  - wincache.configuration.md: « Налаштування під час виконання
  - wincache.sessionhandler.md: Обробник сесій WinCache »
  - index.md: PHP Manual
  - wincache.setup.md: Встановлення та налаштування
title: Скрипт статистики WinCache
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Скрипт статистики WinCache

Пакет WinCache містить PHP-скрипт, wincache.php, який можна використовувати для отримання статистики використання кеша.

Якщо модуль WinCache був встановлений за допомогою Microsoft Web Platform Installer, то скрипт розташовуватиметься на шляху %SystemDrive%\\Program Files\\IIS\\Windows Cache for PHP\\. На 64-розрядних версіях Windows Server, скрипт лежить на шляху %SystemDrive%\\Program Files (x86)\\IIS\\Windows Cache для PHP. Якщо модуль встановлювався самостійно, то wincache.php лежатиме в тому ж каталозі, в який ви розпаковували інсталяційний пакет.

Для використання wincache.php, скопіюйте його в кореневий каталог веб-сайту або будь-який його підкаталог. Щоб захистити скрипт, відкрийте його в текстовому редакторі та змініть значення констант *USERNAME*и*PASSWORD*. Якщо для автентифікації в IIS використовується інший механізм, дотримуйтесь інструкцій у коментарях:

**Приклад #1 Налаштування автентифікації для wincache.php**

```php
<?php
/**
 * ======================== CONFIGURATION SETTINGS ==============================
 * If you do not want to use authentication for this page, set USE_AUTHENTICATION to 0.
 * If you use authentication then replace the default password.
 */
define('USE_AUTHENTICATION', 1);
define('USERNAME', 'wincache');
define('PASSWORD', 'wincache');

/**
 * The Basic PHP authentication will work only when IIS is configured to support
 * Anonymous Authentication' and nothing else. If IIS is configured to support/use
 * any other kind of authentication like Basic/Negotiate/Digest etc, this will not work.
 * In that case use the array below to define the names of users in your
 * domain/network/workgroup which you want to grant access to.
 */
$user_allowed = array('DOMAIN\user1', 'DOMAIN\user2', 'DOMAIN\user3');

/**
 * If the array contains string 'all', then all the users authenticated by IIS
 * will have access to the page. Uncomment the below line and comment above line
 * to grant access to all users who gets authenticated by IIS.
 */
/* $user_allowed = array('all'); */

/** ===================== END OF CONFIGURATION SETTINGS ========================== */
?>
```

> **Зауваження**: Завжди захищайте скрипт wincache.php за допомогою вбудованого механізму або за допомогою механізму автентифікації веб-сервера. Залишаючи доступ до скрипту відкритим ви можете скомпрометувати вашу програму та веб-сервер.
