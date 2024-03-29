---
navigation:
  - features.http-auth.md: « HTTP-автентифікація в PHP
  - features.sessions.md: Сесії »
  - index.md: PHP Manual
  - features.md: Особливості
title: Cookies
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Cookies

PHP прозоро підтримує HTTP cookies. Cookies - це механізм зберігання даних браузером віддаленої машини для відстеження або ідентифікації відвідувачів, що повертаються. Ви можете встановити cookies за допомогою функцій [setcookie()](function.setcookie.md) або [setrawcookie()](function.setrawcookie.md)Cookies являются частью HTTP-заголовка, тому [setcookie()](function.setcookie.md) повинна викликатись до будь-якого виведення даних у браузер. Це те саме обмеження, яке має функція [header()](function.header.md). Ви можете використовувати [функції буферизації виводу](ref.outcontrol.md), щоб затримати виведення результатів роботи скрипта до того моменту, коли буде відомо, чи знадобиться встановлення cookies або інших заголовків.

Будь-які cookies, надіслані серверу браузером клієнта, будуть автоматично включені до суперглобального масиву [$\_COOKIE](reserved.variables.cookies.md), якщо директива [variables\_order](ini.core.md#ini.variables-order) містить літеру "C". Для призначення кількох значень однієї cookie просто додайте `[]` до її імені.

Додаткову інформацію, в тому числі й особливості реалізації браузерів, наведено в описі функцій [setcookie()](function.setcookie.md) і [setrawcookie()](function.setrawcookie.md)
