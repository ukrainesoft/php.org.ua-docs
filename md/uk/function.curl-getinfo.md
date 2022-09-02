---
navigation:
  - function.curl-file-create.md: « curlfilecreate
  - function.curl-init.md: curlinit »
  - index.md: PHP Manual
  - ref.curl.md: Функции cURL
title: curlgetinfo
---
# curlgetinfo

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

curlgetinfo — Повертає інформацію про певну операцію

### Опис

```methodsynopsis
curl_getinfo(CurlHandle $handle, ?int $option = null): mixed
```

Повертає інформацію про останню операцію.

### Список параметрів

`handle`

Дескриптор cURL, отриманий з [curlinit()](function.curl-init.md)

`option`

Одна з перерахованих констант:

-   **`CURLINFO_EFFECTIVE_URL`** - Останній використаний URL
-   **`CURLINFO_HTTP_CODE`** - Останній код відповіді. Починаючи з cURL 7.10.8, це застарілий псевдонім **`CURLINFO_RESPONSE_CODE`**
-   **`CURLINFO_FILETIME`** - Видалена (серверна) дата завантаженого документа, якщо увімкнена опція **`CURLOPT_FILETIME`**; якщо отримано -1, то цей час невідомий
-   **`CURLINFO_TOTAL_TIME`** - Загальний час виконання транзакції в секундах останньої передачі
-   **`CURLINFO_NAMELOOKUP_TIME`** - Час дозволу імені сервера в секундах
-   **`CURLINFO_CONNECT_TIME`** - Час у секундах, витрачений на встановлення з'єднання
-   **`CURLINFO_PRETRANSFER_TIME`** - Час у секундах, що минув від початку операції до готовності до фактичної передачі даних
-   **`CURLINFO_STARTTRANSFER_TIME`** - Час у секундах до передачі першого байта даних
-   **`CURLINFO_REDIRECT_COUNT`** - Число перенаправлень із включеною опцією **`CURLOPT_FOLLOWLOCATION`**
-   **`CURLINFO_REDIRECT_TIME`** - Загальний час у секундах, витрачений на перенаправлення до початку останньої транзакції із включеною опцією **`CURLOPT_FOLLOWLOCATION`**
-   **`CURLINFO_REDIRECT_URL`** - При відключеній опції **`CURLOPT_FOLLOWLOCATION`**: URL перенаправлення, знайдений у минулій ітерації, який потрібно вимагати вручну. Якщо опція **`CURLOPT_FOLLOWLOCATION`** включено: порожнє значення. URL перенаправлення в цьому випадку доступний у **`CURLINFO_EFFECTIVE_URL`**
-   **`CURLINFO_PRIMARY_IP`** - IP-адреса останнього з'єднання
-   **`CURLINFO_PRIMARY_PORT`** - Порт отримувача останнього з'єднання
-   **`CURLINFO_LOCAL_IP`** - локальна (вихідна) IP адреса останнього з'єднання
-   **`CURLINFO_LOCAL_PORT`** - локальний (вихідний) порт останнього з'єднання
-   **`CURLINFO_SIZE_UPLOAD`** - Загальна кількість байт при закачуванні
-   **`CURLINFO_SIZE_DOWNLOAD`** - Загальна кількість байт під час завантаження
-   **`CURLINFO_SPEED_DOWNLOAD`** - Середня швидкість завантаження
-   **`CURLINFO_SPEED_UPLOAD`** - Середня швидкість закачування
-   **`CURLINFO_HEADER_SIZE`** - Сумарний розмір усіх отриманих заголовків
-   **`CURLINFO_HEADER_OUT`** - Рядок запиту, що посилається. Для роботи цього параметра додайте опцію **`CURLINFO_HEADER_OUT`** до дескриптора за допомогою виклику [curlsetopt()](function.curl-setopt.md)
-   **`CURLINFO_REQUEST_SIZE`** - Сумарний розмір всіх надісланих запитів, що нині використовується тільки для HTTP-запитів
-   **`CURLINFO_SSL_VERIFYRESULT`** - Результат перевірки SSL-сертифіката, запрошеного за допомогою установки параметра **`CURLOPT_SSL_VERIFYPEER`**
-   **`CURLINFO_CONTENT_LENGTH_DOWNLOAD`** - розмір завантажених даних, прочитаний із заголовка `Content-Length:`
-   **`CURLINFO_CONTENT_LENGTH_UPLOAD`** - Розмір даних, що закачуються
-   **`CURLINFO_CONTENT_TYPE`** - Вміст отриманого заголовка `Content-Type:`. Якщо NULL, то сервер не надіслав правильний заголовок `Content-Type:`
-   **`CURLINFO_PRIVATE`** - Внутрішні дані, пов'язані з цим cURL-обробником, раніше встановлені за допомогою опції **`CURLOPT_PRIVATE`** у функції [curlsetopt()](function.curl-setopt.md)
-   **`CURLINFO_RESPONSE_CODE`** - Останній код повернення
-   **`CURLINFO_HTTP_CONNECTCODE`** - Код відповіді операції CONNECT
-   **`CURLINFO_HTTPAUTH_AVAIL`** - бітова маска, що показує можливі методи аутентифікації, доступні при попередній відповіді
-   **`CURLINFO_PROXYAUTH_AVAIL`** - бітова маска, що показує можливі методи аутентифікації на проксі, доступні при попередній відповіді
-   **`CURLINFO_OS_ERRNO`** - Номер помилки під час спроби з'єднання. Код може різнитися залежно від системи та ОС
-   **`CURLINFO_NUM_CONNECTS`** - Кількість з'єднань, скоєних curl для забезпечення попередньої передачі
-   **`CURLINFO_SSL_ENGINES`** - Підтримка OpenSSL
-   **`CURLINFO_COOKIELIST`** - Усі відомі куки
-   **`CURLINFO_FTP_ENTRY_PATH`** - Шлях входу на FTP-сервер
-   **`CURLINFO_APPCONNECT_TIME`** - Час у секундах від початку та до встановлення SSL/SSH connect/handshake з віддаленим хостом
-   **`CURLINFO_CERTINFO`** - зв'язування ключів TLS
-   **`CURLINFO_CONDITION_UNMET`** - інформація про незадоволені тимчасові умови
-   **`CURLINFO_RTSP_CLIENT_CSEQ`** - Наступний RTSP клієнтського CSeq
-   **`CURLINFO_RTSP_CSEQ_RECV`** - Нещодавно отриманий CSeq
-   **`CURLINFO_RTSP_SERVER_CSEQ`** - Наступний RTSP серверний CSeq
-   **`CURLINFO_RTSP_SESSION_ID`** - ID сесії RTSP
-   **`CURLINFO_CONTENT_LENGTH_DOWNLOAD_T`** - Content-length завантаження. Це значення зчитується з поля `Content-Type:`. -1 якщо розмір не відомий
-   **`CURLINFO_CONTENT_LENGTH_UPLOAD_T`** - Вказаний розмір завантаження. -1 якщо розмір не відомий
-   **`CURLINFO_HTTP_VERSION`** - версія, використана в останньому HTTP-з'єднанні. Значення, що повертається, буде однією з певних констант **`CURL_HTTP_VERSION_*`** або 0, якщо версія не може бути визначена
-   **`CURLINFO_PROTOCOL`** - Протокол, використаний в останній HTTP-з'єднанні. Значення, що повертається, буде точно одним із значень **`CURLPROTO_*`**
-   **`CURLINFO_PROXY_SSL_VERIFYRESULT`** - Результат перевірки сертифіката, який було запитано (з використанням параметра **`CURLOPT_PROXY_SSL_VERIFYPEER`**). Використовується тільки для HTTPS-проксі.
-   **`CURLINFO_SCHEME`** - Схема URL, яка використовується для останнього з'єднання
-   **`CURLINFO_SIZE_DOWNLOAD_T`** - загальна кількість скачаних байтів. Номер призначений лише для останньої передачі та скидатиметься для кожної нової передачі.
-   **`CURLINFO_SIZE_UPLOAD_T`** - Загальна кількість завантажених байтів
-   **`CURLINFO_SPEED_DOWNLOAD_T`** - Середня швидкість завантаження в байтах/секунду, виміряна для повного завантаження
-   **`CURLINFO_SPEED_UPLOAD_T`** - Середня швидкість завантаження в байтах/секунду, виміряна для повного завантаження
-   **`CURLINFO_APPCONNECT_TIME_T`** - Час у мікросекундах, який пройшов з самого початку, доки з'єднання/рукостискання SSL/SSH не було завершено
-   **`CURLINFO_CONNECT_TIME_T`** - Загальний час, що витрачається в мікросекундах від початку до моменту підключення до віддаленого хоста (або проксі-сервера)
-   **`CURLINFO_FILETIME_T`** - Віддалений час вилученого документа (як позначка часу Unix), альтернатива **`CURLINFO_FILETIME`**, щоб дозволити системам з 32-бітними long-змінними витягувати дати поза діапазоном 32-бітових тимчасових міток
-   **`CURLINFO_NAMELOOKUP_TIME_T`** -в Час у мікросекундах від початку до дозволу імені
-   **`CURLINFO_PRETRANSFER_TIME_T`** - Час у мікросекундах, витрачений від початку до початку передачі файлу
-   **`CURLINFO_REDIRECT_TIME_T`** - Загальний час у мікросекундах, який був потрібний для всіх кроків перенаправлення, включаючи пошук імені, підключення, попереднє перенесення та передачу до запуску остаточної транзакції
-   **`CURLINFO_STARTTRANSFER_TIME_T`** - Час у мікросекундах, який минув від початку до отримання першого байта
-   **`CURLINFO_TOTAL_TIME_T`** - Загальний час у мікросекундах для попередньої передачі, включаючи роздільну здатність імен, TCP-з'єднання тощо.

### Значення, що повертаються

Якщо параметр `option` вказано, то повертається його значення. Інакше повертається асоціативний масив із наступними елементами (які відповідають значенням аргументу `option`) або **`false`** у разі виникнення помилки:

-   "url"
-   "contenttype"
-   "httpcode"
-   "headersize"
-   "requestsize"
-   "filetime"
-   "sslverifyresult"
-   "redirectcount"
-   "totaltime"
-   "namelookuptime"
-   "connecttime"
-   "pretransfertime"
-   "sizeupload"
-   "sizedownload"
-   "speeddownload"
-   "speedupload"
-   "downloadcontentlength"
-   "uploadcontentlength"
-   "starttransfertime"
-   "redirecttime"
-   "certinfo"
-   "primaryip"
-   "primaryport"
-   "localip"
-   "localport"
-   "redirecturl"
-   "requestheader" (повертається тільки за встановленої опції **`CURLINFO_HEADER_OUT`** за допомогою виклику [curlsetopt()](function.curl-setopt.md) до виконання запиту)

Врахуйте, що внутрішні дані не додаються до асоціативного масиву і повинні виходити окремо за допомогою опції **`CURLINFO_PRIVATE`**

### список змін

| Версия | Описание |
| --- | --- |
|  | `handle` тепер чекає екземпляр [CurlHandle](class.curlhandle.md); раніше, очікувався ресурс (resource). |
|  | `option` is nullable now; previously, the default was `0` |
|  | Додані **`CURLINFO_CONTENT_LENGTH_DOWNLOAD_T`** **`CURLINFO_CONTENT_LENGTH_UPLOAD_T`** **`CURLINFO_HTTP_VERSION`** **`CURLINFO_PROTOCOL`** **`CURLINFO_PROXY_SSL_VERIFYRESULT`** **`CURLINFO_SCHEME`** **`CURLINFO_SIZE_DOWNLOAD_T`** **`CURLINFO_SIZE_UPLOAD_T`** **`CURLINFO_SPEED_DOWNLOAD_T`** **`CURLINFO_SPEED_UPLOAD_T`** **`CURLINFO_APPCONNECT_TIME_T`** **`CURLINFO_CONNECT_TIME_T`** **`CURLINFO_FILETIME_T`** **`CURLINFO_NAMELOOKUP_TIME_T`** **`CURLINFO_PRETRANSFER_TIME_T`** **`CURLINFO_REDIRECT_TIME_T`** **`CURLINFO_STARTTRANSFER_TIME_T`** **`CURLINFO_TOTAL_TIME_T`** |

### Приклади

**Приклад #1 Приклад використання **curlgetinfo()****

```php
<?php
// Создаём дескриптор cURL
$ch = curl_init('http://www.example.com/');

// Запускаем
curl_exec($ch);

// Проверяем наличие ошибок
if (!curl_errno($ch)) {
  $info = curl_getinfo($ch);
  echo 'Прошло ', $info['total_time'], ' секунд во время запроса к ', $info['url'], "\n";
}

// Закрываем дескриптор
curl_close($ch);
?>
```

**Приклад #2 Приклад використання **curlgetinfo()** з параметром `option`**

```php
<?php
// Создаём дескриптор cURL
$ch = curl_init('http://www.example.com/');

// Запускаем
curl_exec($ch);

// Проверяем наличие ошибок
if (!curl_errno($ch)) {
  switch ($http_code = curl_getinfo($ch, CURLINFO_HTTP_CODE)) {
    case 200:  # OK
      break;
    default:
      echo 'Неожиданный код HTTP: ', $http_code, "\n";
  }
}

// Закрываем дескриптор
curl_close($ch);
?>
```

### Примітки

> **Зауваження**
> 
> Інформація, зібрана цією функцією, буде збережена під час подальшого використання дескриптора. Це означає, що якщо статистика не буде перезаписана функцією, повертатиметься інформація за попереднім запитом.
