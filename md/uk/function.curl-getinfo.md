---
navigation:
  - function.curl-exec.md: « curl\_exec
  - function.curl-init.md: curl\_init »
  - index.md: PHP Manual
  - ref.curl.md: Опції cURL
title: curl\_getinfo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# curl\_getinfo

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

curl\_getinfo — Отримує інформацію про конкретну передачу

### Опис

```methodsynopsis
curl_getinfo(CurlHandle $handle, ?int $option = null): mixed
```

Отримує інформацію про останню передачу.

### Список параметрів

`handle`

Дескриптор cURL, отриманий з [curl\_init()](function.curl-init.md)

`option`

Константа зі списку:

| Опция | Опис |
| --- | --- |
| **`CURLINFO_CAINFO`** | Шлях до вбудованого сертифіката центру засвідчення за промовчанням |
| **`CURLINFO_CAPATH`** | Рядок шляху до вбудованого сертифіката засвідчувального центру за промовчанням |
| **`CURLINFO_EFFECTIVE_URL`** | Остання ефективна URL |
| **`CURLINFO_HTTP_CODE`** | Останній код відповіді. Починаючи з cURL 7.10.8, це застарілий псевдонім опції. **`CURLINFO_RESPONSE_CODE`** |
| **`CURLINFO_FILETIME`** | Час отримання документа по годиннику віддаленого сервера, якщо параметр **`CURLOPT_FILETIME`** включений для дескриптора cURL; якщо повертається значення -1, час отримання документа невідомо |
| **`CURLINFO_TOTAL_TIME`** | Загальний час транзакції за секунди для останньої передачі |
| **`CURLINFO_NAMELOOKUP_TIME`** | Час у секундах, витрачений на дозвіл імені |
| **`CURLINFO_CONNECT_TIME`** | Час у секундах, витрачений на встановлення з'єднання |
| **`CURLINFO_PRETRANSFER_TIME`** | Час у секундах від запуску до моменту початку передачі файлу |
| **`CURLINFO_STARTTRANSFER_TIME`** | Час у секундах від запуску передачі до отримання першого байта |
| **`CURLINFO_REDIRECT_COUNT`** | Число перенаправлень, якщо параметр **`CURLOPT_FOLLOWLOCATION`** включений для дескриптора cURL |
| **`CURLINFO_REDIRECT_TIME`** | Загальний час у секундах, який був потрібний для всіх кроків перенаправлення до запуску останньої транзакції, якщо параметр **`CURLOPT_FOLLOWLOCATION`** включений для дескриптора cURL |
| **`CURLINFO_REDIRECT_URL`** | Якщо параметр дескриптора **`CURLOPT_FOLLOWLOCATION`** відключено: URL-адресу перенаправлення, знайдену в останній транзакції, яку наступного разу потрібно запросити вручну. Якщо параметр **`CURLOPT_FOLLOWLOCATION`** увімкнено: порожнє значення. Тоді URL-адреса перенаправлення доступна в опції **`CURLINFO_EFFECTIVE_URL`** |
| **`CURLINFO_PRIMARY_IP`** | IP-адреса останнього з'єднання |
| **`CURLINFO_PRIMARY_PORT`** | Порт призначення останнього з'єднання |
| **`CURLINFO_LOCAL_IP`** | Локальна (вихідна) IP-адреса останнього з'єднання |
| **`CURLINFO_LOCAL_PORT`** | Локальний (вихідний) порт останнього з'єднання |
| **`CURLINFO_SIZE_UPLOAD`** | Загальна кількість переданих байтів |
| **`CURLINFO_SIZE_DOWNLOAD`** | Загальна кількість отриманих байтів |
| **`CURLINFO_SPEED_DOWNLOAD`** | Середня швидкість отримання даних |
| **`CURLINFO_SPEED_UPLOAD`** | Середня швидкість передачі даних |
| **`CURLINFO_HEADER_SIZE`** | Сумарний розмір отриманих заголовків |
| **`CURLINFO_HEADER_OUT`** | Надісланий рядок запиту. Щоб цей параметр працював, потрібно додати опцію **`CURLINFO_HEADER_OUT`** у дескриптор через виклик функції [curl\_setopt()](function.curl-setopt.md) |
| **`CURLINFO_REFERER`** | Заголовок реферера |
| **`CURLINFO_REQUEST_SIZE`** | Сумарний розмір відправлених запитів, працює поки що тільки для HTTP-запитів |
| **`CURLINFO_RETRY_AFTER`** | Інформація із заголовка `Retry-After:` або нуль, якщо допустимого заголовка не було |
| **`CURLINFO_SSL_VERIFYRESULT`** | Результат перевірки сертифікації SSL, запитаний з параметром **`CURLOPT_SSL_VERIFYPEER`** |
| **`CURLINFO_CONTENT_LENGTH_DOWNLOAD`** | Розмір отриманих даних, прочитаний із заголовка `Content-Length:` |
| **`CURLINFO_CONTENT_LENGTH_UPLOAD`** | Розмір переданих даних |
| **`CURLINFO_CONTENT_TYPE`** | Значення заголовка `Content-Type:` запитаного документа. Значення NULL вказує, що сервер не надіслав допустимий заголовок `Content-Type:` |
| **`CURLINFO_PRIVATE`** | Закриті дані, пов'язані з поточним дескриптором cURL, які раніше були встановлені функцією [curl\_setopt()](function.curl-setopt.md)с параметром\*\*`CURLOPT_PRIVATE`\*\* |
| **`CURLINFO_PROXY_ERROR`** | Детальний код помилки проксі-сервера (SOCKS), коли остання передача повернула помилку **`CURLE_PROXY`**. . Значення, що повертається, дорівнюватиме значенню константи з сімейства **`CURLPX_*`**. . Код помилки дорівнюватиме значенню константи \*\*`CURLPX_OK`\*\*якщо код відповіді не був доступний |
| **`CURLINFO_RESPONSE_CODE`** | Останній код відповіді |
| **`CURLINFO_HTTP_CONNECTCODE`** | Код відповіді на запит CONNECT |
| **`CURLINFO_HTTPAUTH_AVAIL`** | Бітова маска доступного методу або методів аутентифікації на основі даних попередньої відповіді |
| **`CURLINFO_PROXYAUTH_AVAIL`** | Бітова маска доступного методу або методів аутентифікації проксі-сервера на основі даних попередньої відповіді |
| **`CURLINFO_OS_ERRNO`** | Значення змінної Errno у разі збою з'єднання. Номер помилки залежить від ОС та особливостей системи |
| **`CURLINFO_NUM_CONNECTS`** | Кількість з'єднань, які curl довелося створити, що успішно виконати попередню передачу |
| **`CURLINFO_SSL_ENGINES`** | Список підтримуваних криптодвижків бібліотеки OpenSSL |
| **`CURLINFO_COOKIELIST`** | Відомі куки |
| **`CURLINFO_FTP_ENTRY_PATH`** | Шлях входу на FTP-сервер |
| **`CURLINFO_APPCONNECT_TIME`** | Час у секундах від запуску до встановлення SSL- або SSH-підключення або рукостискання з віддаленим хостом |
| **`CURLINFO_CERTINFO`** | Ланцюжок сертифікатів TLS |
| **`CURLINFO_CONDITION_UNMET`** | Інформація про невиконані за відведений час умови |
| **`CURLINFO_RTSP_CLIENT_CSEQ`** | Наступний CSeq-заголовок RTSP-клієнта |
| **`CURLINFO_RTSP_CSEQ_RECV`** | Останній отриманий заголовок CSeq |
| **`CURLINFO_RTSP_SERVER_CSEQ`** | Наступний CSeq-заголовок RTSP-сервера |
| **`CURLINFO_RTSP_SESSION_ID`** | Ідентифікатор RTSP-сесії |
| **`CURLINFO_CONTENT_LENGTH_DOWNLOAD_T`** | Розмір даних. Це значення зчитується з поля `Content-Length:`. . Значення дорівнює -1, якщо розмір невідомий |
| **`CURLINFO_CONTENT_LENGTH_UPLOAD_T`** | Розмір надісланих даних. Значення дорівнює -1, якщо розмір невідомий |
| **`CURLINFO_HTTP_VERSION`** | Версія HTTP-протоколу останнього з'єднання. Значення, що повертається, дорівнюватиме значенню константи з сімейства **`CURL_HTTP_VERSION_*`** або 0, якщо версію неможливо визначити |
| **`CURLINFO_PROTOCOL`** | Протокол останнього з'єднання HTTP. Значення, що повертається, дорівнюватиме значенню константи з сімейства **`CURLPROTO_*`** |
| **`CURLINFO_PROXY_SSL_VERIFYRESULT`** | Результат запитаної перевірки сертифіката (з параметром **`CURLOPT_PROXY_SSL_VERIFYPEER`**). Працює тільки для серверів HTTPS-проксі |
| **`CURLINFO_SCHEME`** | Схема URL останнього з'єднання |
| **`CURLINFO_SIZE_DOWNLOAD_T`** | Загальна кількість байтів, отриманих. Число буде вказано лише для останньої передачі та скидатиметься при кожній новій передачі |
| **`CURLINFO_SIZE_UPLOAD_T`** | Загальна кількість байтів, які були передані |
| **`CURLINFO_SPEED_DOWNLOAD_T`** | Середня швидкість отримання даних у байтах за секунду, яку curl виміряв в кінці передачі |
| **`CURLINFO_SPEED_UPLOAD_T`** | Середня швидкість передачі даних у байтах за секунду, яку curl виміряв в кінці передачі |
| **`CURLINFO_APPCONNECT_TIME_T`** | Час у мікросекундах, що минув від запуску до завершення SSL або SSH підключення або рукостискання з віддаленим хостом |
| **`CURLINFO_CONNECT_TIME_T`** | Загальний час у мікросекундах, що минув від запуску до завершення підключення до віддаленого хоста або проксі-сервера |
| **`CURLINFO_FILETIME_T`** | Час отримання документа у вигляді мітки часу Unix по годинниках віддаленого сервера, альтернатива опції **`CURLINFO_FILETIME`**, щоб дозволити системам з 32-бітними long-змінними витягувати дати за межами діапазону 32-бітних міток часу |
| **`CURLINFO_NAMELOOKUP_TIME_T`** | Час у мікросекундах від запуску до дозволу імені |
| **`CURLINFO_PRETRANSFER_TIME_T`** | Час у мікросекундах від запуску до моменту початку передачі файлу |
| **`CURLINFO_REDIRECT_TIME_T`** | Загальний час у мікросекундах, який знадобився для всіх кроків перенаправлення, включаючи пошук імені, підключення, попередню основну передачу до запуску остаточної транзакції |
| **`CURLINFO_STARTTRANSFER_TIME_T`** | Час у мікросекундах від запуску передачі до отримання першого байта |
| **`CURLINFO_TOTAL_TIME_T`** | Загальний час попередньої передачі в мікросекундах, включаючи роздільну здатність імені, TCP-з'єднання і т.д. |

### Значення, що повертаються

Якщо параметр `option` заданий, повертається його значення. В інших випадках повертається асоціативний масив з такими елементами (які відповідають значенням параметра `option`) или\*\*`false`\*\*в случае ошибки:

-   «url»
-   «content\_type»
-   «http\_code»
-   «header\_size»
-   «request\_size»
-   «filetime»
-   «ssl\_verify\_result»
-   «redirect\_count»
-   «total\_time»
-   «namelookup\_time»
-   «connect\_time»
-   «pretransfer\_time»
-   «size\_upload»
-   «size\_download»
-   «speed\_download»
-   «speed\_upload»
-   «download\_content\_length»
-   «upload\_content\_length»
-   «starttransfer\_time»
-   «redirect\_time»
-   «certinfo»
-   «primary\_ip»
-   «primary\_port»
-   «local\_ip»
-   «local\_port»
-   «redirect\_url»
-   «request\_header» (Значення буде заповнено, лише якщо функцією[curl\_setopt()](function.curl-setopt.md)для дескриптора включено параметр\*\*`CURLINFO_HEADER_OUT`\*\*

Врахуйте, що закриті дані не додаються до асоціативного масиву і витягуються окремо через опцію **`CURLINFO_PRIVATE`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Додані опції **`CURLINFO_CAINFO`** і **`CURLINFO_CAPATH`** |
| 8.2.0 | Додані опції **`CURLINFO_PROXY_ERROR`** **`CURLINFO_REFERER`** **`CURLINFO_RETRY_AFTER`** |
| 8.0.0 | `handle` тепер чекає екземпляр [CurlHandle](class.curlhandle.md); раніше, очікувався ресурс (resource). |
| 8.0.0 | Тепер параметр `option`принимает значение\*\*`null`\*\*. . раніше значенням за умовчанням був |
| 7.3.0 | Додані опції **`CURLINFO_CONTENT_LENGTH_DOWNLOAD_T`** **`CURLINFO_CONTENT_LENGTH_UPLOAD_T`** **`CURLINFO_HTTP_VERSION`** **`CURLINFO_PROTOCOL`** **`CURLINFO_PROXY_SSL_VERIFYRESULT`** **`CURLINFO_SCHEME`** **`CURLINFO_SIZE_DOWNLOAD_T`** **`CURLINFO_SIZE_UPLOAD_T`** **`CURLINFO_SPEED_DOWNLOAD_T`** **`CURLINFO_SPEED_UPLOAD_T`** **`CURLINFO_APPCONNECT_TIME_T`** **`CURLINFO_CONNECT_TIME_T`** **`CURLINFO_FILETIME_T`** **`CURLINFO_NAMELOOKUP_TIME_T`** **`CURLINFO_PRETRANSFER_TIME_T`** **`CURLINFO_REDIRECT_TIME_T`** **`CURLINFO_STARTTRANSFER_TIME_T`** **`CURLINFO_TOTAL_TIME_T`** |

### Приклади

**Приклад #1 Приклад використання функції** curl\_getinfo()\*\*\*\*

```php
<?php

// Создаём дескриптор cURL
$ch = curl_init('http://www.example.com/');

// Запускаем
curl_exec($ch);

// Проверяем наличие ошибок
if (!curl_errno($ch)) {
  $info = curl_getinfo($ch);
  echo 'Прошло ', $info['total_time'], ' секунд во время запроса к ', $info['url'], "\n";
}

// Закрываем дескриптор
curl_close($ch);

?>
```

**Приклад #2 Приклад використання функції** curl\_getinfo()**с параметром`option`**

```php
<?php

// Создаём дескриптор cURL
$ch = curl_init('http://www.example.com/');

// Запускаем
curl_exec($ch);

// Проверяем наличие ошибок
if (!curl_errno($ch)) {
  switch ($http_code = curl_getinfo($ch, CURLINFO_HTTP_CODE)) {
    case 200:  # OK
      break;
    default:
      echo 'Неожиданный код HTTP: ', $http_code, "\n";
  }
}

// Закрываем дескриптор
curl_close($ch);

?>
```

### Примітки

> **Зауваження** :
> 
> Інформація, яку збирає ця функція, зберігається в дескрипторі та доступна для запуску повторної передачі. Тобто поки статистика не перевизначена внутрішньо, ця функція повертає попередню інформацію.
