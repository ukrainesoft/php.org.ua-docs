Клієнтська бібліотека роботи з URL

-   [« Другие службы](refs.remote.other.html)
    
-   [Введение »](intro.curl.html)
    
-   [PHP Manual](index.html)
    
-   [Другие службы](refs.remote.other.html)
    
-   Клієнтська бібліотека роботи з URL
    

# Клієнтська бібліотека роботи з URL

-   [Введение](intro.curl.html)
-   [Установка и настройка](curl.setup.html)
    -   [Требования](curl.requirements.html)
    -   [Установка](curl.installation.html)
    -   [Настройка во время выполнения](curl.configuration.html)
    -   [Типы ресурсов](curl.resources.html)
-   [Предопределённые константы](curl.constants.html)
-   [Примеры](curl.examples.html)
    -   [Простой пример использования curl](curl.examples-basic.html)
-   [Функции cURL](ref.curl.html)
    -   [curl\_close](function.curl-close.html) - Завершує сеанс cURL
    -   [curl\_copy\_handle](function.curl-copy-handle.html) — Копіює дескриптор cURL разом із усіма його налаштуваннями
    -   [curl\_errno](function.curl-errno.html) — Повертає код останньої помилки
    -   [curl\_error](function.curl-error.html) — Повертає рядок із описом останньої помилки поточного сеансу
    -   [curl\_escape](function.curl-escape.html) — Кодує рядок як URL
    -   [curl\_exec](function.curl-exec.html) — Виконує запит cURL
    -   [curl\_file\_create](function.curl-file-create.html) — Створює об'єкт CURLFile
    -   [curl\_getinfo](function.curl-getinfo.html) — Повертає інформацію про певну операцію
    -   [curl\_init](function.curl-init.html) - Ініціалізує сеанс cURL
    -   [curl\_multi\_add\_handle](function.curl-multi-add-handle.html) — Додає звичайний cURL-дескриптор до набору cURL-дескрипторів
    -   [curl\_multi\_close](function.curl-multi-close.html) — Закриває набір cURL-дескрипторів
    -   [curl\_multi\_errno](function.curl-multi-errno.html) — Повертає код останньої помилки множинного curl
    -   [curl\_multi\_exec](function.curl-multi-exec.html) — Запускає підключення поточного дескриптора cURL
    -   [curl\_multi\_getcontent](function.curl-multi-getcontent.html) — Повертає результат операції, якщо було встановлено опцію CURLOPTRETURNTRANSFER
    -   [curl\_multi\_info\_read](function.curl-multi-info-read.html) — Повертає інформацію про поточні операції
    -   [curl\_multi\_init](function.curl-multi-init.html) — Створює набір cURL-дескрипторів
    -   [curl\_multi\_remove\_handle](function.curl-multi-remove-handle.html) — Видаляє cURL дескриптор із набору cURL дескрипторів
    -   [curl\_multi\_select](function.curl-multi-select.html) — Чекає на активність на будь-якому curlmulti з'єднанні
    -   [curl\_multi\_setopt](function.curl-multi-setopt.html) — Встановити налаштування для множинного дескриптора cURL
    -   [curl\_multi\_strerror](function.curl-multi-strerror.html) — Повертає рядок, що описує помилку
    -   [curl\_pause](function.curl-pause.html) — Припинити та відновити з'єднання
    -   [curl\_reset](function.curl-reset.html) — Скинути налаштування обробника сесії libcurl
    -   [curl\_setopt\_array](function.curl-setopt-array.html) — Встановлює кілька параметрів сеансу cURL
    -   [curl\_setopt](function.curl-setopt.html) — Встановлює параметр сеансу CURL
    -   [curl\_share\_close](function.curl-share-close.html) — Закрити оброблюваний обробник cURL
    -   [curl\_share\_errno](function.curl-share-errno.html) — Повертає код останньої помилки оброблюваного обробника curl
    -   [curl\_share\_init](function.curl-share-init.html) — Ініціалізація оброблюваного обробника cURL
    -   [curl\_share\_setopt](function.curl-share-setopt.html) — Встановити опції роздільного обробника cURL
    -   [curl\_share\_strerror](function.curl-share-strerror.html) — Повертає опис для заданого коду помилки
    -   [curl\_strerror](function.curl-strerror.html) — Отримати текстовий опис для коду помилки
    -   [curl\_unescape](function.curl-unescape.html) — Декодує закодований URL-рядок
    -   [curl\_version](function.curl-version.html) — Повертає версію cURL
-   [CurlHandle](class.curlhandle.html) - Клас CurlHandle
-   [CurlMultiHandle](class.curlmultihandle.html) - Клас CurlMultiHandle
-   [CurlShareHandle](class.curlsharehandle.html) - Клас CurlShareHandle
-   [CURLFile](class.curlfile.html) - Клас CURLFile
    -   [CURLFile::\_\_construct](curlfile.construct.html) — Створює об'єкт CURLFile
    -   [CURLFile::getFilename](curlfile.getfilename.html) — Повертає ім'я файлу на сервері
    -   [CURLFile::getMimeType](curlfile.getmimetype.html) - Повертає MIME-тип файлу
    -   [CURLFile::getPostFilename](curlfile.getpostfilename.html) — Повертає ім'я файлу, що надсилається POST-запитом
    -   [CURLFile::setMimeType](curlfile.setmimetype.html) - Встановлює MIME-тип
    -   [CURLFile::setPostFilename](curlfile.setpostfilename.html) — Встановлює ім'я файлу для надсилання методом POST
-   [CURLStringFile](class.curlstringfile.html) - Клас CURLStringFile
    -   [CURLStringFile::\_\_construct](curlstringfile.construct.html) — Створює об'єкт CURLStringFile