Unix-сокети: UNIX та UDG

-   [Інтернет-сокети: TCP, UDP, SSL і TLS](transports.inet.html)
    
-   [Таблица сравнения типов в PHP »](types.comparisons.html)
    
-   [PHP Manual](index.html)
    
-   [Список підтримуваних транспортних протоколів](transports.html)
    
-   Unix-сокети: UNIX та UDG
    

## Unix-сокети: UNIX та UDG

`unix://` і `udg://`

-   `unix:///tmp/mysock`
-   `udg:///tmp/mysock`

`unix://` дає можливість використовувати unix-сокети, а `udg://` надає альтернативний спосіб передачі даних у них, з використанням протоколу користувача датаграм.

Unix-сокети, на відміну від Інтернет-сокетів, не вимагають вказівки порту. В разі [fsockopen()](function.fsockopen.html) параметр `portno` повинен дорівнювати 0.

> **Зауваження**: Unix-сокети не підтримуються у Windows.