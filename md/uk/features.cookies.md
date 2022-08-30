Cookies

-   [« HTTP-автентифікація в PHP](features.http-auth.html)
    
-   [Сессии »](features.sessions.html)
    
-   [PHP Manual](index.html)
    
-   [Відмітні особливості](features.html)
    
-   Cookies
    

# Cookies

PHP прозоро підтримує HTTP cookies. Cookies - це механізм зберігання даних браузером віддаленої машини для відстеження або ідентифікації відвідувачів, що повертаються. Ви можете встановити cookies за допомогою функцій [setcookie()](function.setcookie.html) або [setrawcookie()](function.setrawcookie.html). Cookies є частиною HTTPзаголовка, тому [setcookie()](function.setcookie.html) повинна викликатись до будь-якого виведення даних у браузер. Це те саме обмеження, яке має функція [header()](function.header.html). Ви можете використовувати [функции буферизации вывода](ref.outcontrol.html), щоб затримати виведення результатів роботи скрипта до того моменту, коли буде відомо, чи знадобиться встановлення cookies або інших заголовків.

Будь-які cookies, надіслані серверу браузером клієнта, будуть автоматично включені до суперглобального масиву [COOKIE](reserved.variables.cookies.html), якщо директива [variablesorder](ini.core.html#ini.variables-order) містить літеру "C". Для призначення кількох значень однієї cookie просто додайте `[]` до її імені.

Додаткову інформацію, в тому числі й особливості реалізації браузерів, наведено в описі функцій [setcookie()](function.setcookie.html) і [setrawcookie()](function.setrawcookie.html)