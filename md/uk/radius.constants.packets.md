типи пакетів RADIUS

-   [« Опции RADIUS](radius.constants.options.md)
    
-   [Типи атрибутів RADIUS »](radius.constants.attributes.md)
    
-   [PHP Manual](index.md)
    
-   [Обумовлені константи](radius.constants.md)
    
-   типи пакетів RADIUS
    

## типи пакетів RADIUS

Пакети RADIUS, будь то запит або відповідь, завжди включають тип. Ці константи корисні при заданні типу при використанні [radiuscreaterequest()](function.radius-create-request.html) та при обробці відповіді [radiussendrequest()](function.radius-send-request.html)

**`RADIUS_ACCESS_REQUEST`** (int)

Запит Access-Request (Запит доступу) використовується для автентифікації користувача сервером RADIUS. Дані пакети повинні містити атрибут [**`RADIUS_NAS_IP_ADDRESS`**](radius.constants.attributes.html#constant.radius-nas-ip-address) або [**`RADIUS_NAS_IDENTIFIER`**](radius.constants.attributes.html#constant.radius-nas-identifier) , також повинні містити [**`RADIUS_USER_PASSWORD`**](radius.constants.attributes.html#constant.radius-user-password) [**`RADIUS_CHAP_PASSWORD`**](radius.constants.attributes.html#constant.radius-chap-password) або [**`RADIUS_STATE`**](radius.constants.attributes.html#constant.radius-state) , і можуть містити атрибут [**`RADIUS_USER_NAME`**](radius.constants.attributes.html#constant.radius-user-name)

**`RADIUS_ACCESS_ACCEPT`** (int)

Відповідь Access-Accept (Доступ дозволено) надходить у відповідь на запит Access-Request і означає, що сервер RADIUS успішно автентифікував користувача.

**`RADIUS_ACCESS_REJECT`** (int)

Відповідь Access-Reject (Заборонено) надходить у відповідь на запит Access-Request і означає, що сервер RADIUS не зміг аутентифікувати користувача.

**`RADIUS_ACCESS_CHALLENGE`** (int)

Відповідь Access-Challenge (Зміна у праві на доступ) надходить у відповідь на запит Access-Request і означає, що серверу RADIUS потрібна додаткова інформація для прийняття рішення щодо автентифікації.

**`RADIUS_ACCOUNTING_REQUEST`** (int)

Запит Accounting-Request (Запит облікових даних) використовується для передачі облікової інформації для служби на сервер RADIUS.

**`RADIUS_ACCOUNTING_RESPONSE`** (int)

Відповідь Accounting-Response (Облікові дані) є відповіддю на запит Accounting-Request.

**`RADIUS_COA_REQUEST`** (int)

Запит CoA-Request надсилається із сервера RADIUS і означає, що змінилася авторизація у сеансі користувача. Відповідь має бути надіслано у формі CoA-ACK або CoA-NAK.

Ця константа доступна в PECL radius 1.3.0 та вище.

**`RADIUS_COA_ACK`** (int)

Відповідь CoA-ACK надсилається на сервер RADIUS для позначення, що авторизація користувача оновлена.

Ця константа доступна в PECL radius 1.3.0 та вище.

**`RADIUS_COA_NAK`** (int)

Відповідь CoA-NAK надсилається на сервер RADIUS для позначення, що авторизація користувача не може бути оновлена.

Ця константа доступна в PECL radius 1.3.0 та вище.

**`RADIUS_DISCONNECT_REQUEST`** (int)

Запит Disconnect-Request (Запит переривання сесії) надсилається з сервера RADIUS і означає, що необхідно перервати сеанс користувача.

Ця константа доступна в PECL radius 1.3.0 та вище.

**`RADIUS_DISCONNECT_ACK`** (int)

Відповідь Disconnect-ACK, посилається на сервер RADIUS і означає, що сесія користувача завершена.

Ця константа доступна в PECL radius 1.3.0 та вище.

**`RADIUS_DISCONNECT_NAK`** (int)

Відповідь Disconnect-NAK, посилається на сервер RADIUS і означає, що сесія користувача не може бути завершена.

Ця константа доступна в PECL radius 1.3.0 та вище.