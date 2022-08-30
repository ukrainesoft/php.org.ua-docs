Складання / Компіляція з вихідного коду

-   [« Настройка во время выполнения](mysql-xdevapi.configuration.html)
    
-   [Предопределённые константы »](mysql-xdevapi.constants.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](mysql-xdevapi.setup.html)
    
-   Складання / Компіляція з вихідного коду
    

## Складання / Компіляція з вихідного коду

Міркування компіляції цього модуля з вихідного коду.

-   Ім'я модуля - 'mysqlxdevapi', тому використовуйте `--enable-mysql-xdevapi`
    
-   Boost: обов'язковий, за необхідності використовуйте параметр конфігурації --with-boost=DIR або задайте змінну оточення MYSQLXDEVAPIBOOSTROOT. Потрібні лише файли заголовків boost; не двійкові файли.
    
-   Google Protocol Buffers (protobuf): обов'язковий, за необхідності використовуйте параметр конфігурації --with-protobuf=DIR або задайте змінну оточення MYSQLXDEVAPIPROTOBUFROOT.
    
    За бажання використовуйте `make protobufs` для створення файлів protobuf (.pb.cc/.h) та `make clean-protobufs` видалення створених файлів protobuf.
    
    Примітка до protobuf на Windows: залежно від оточення може бути потрібна статична бібліотека з багатопоточним часом виконання DLL. Для підготовки використовуйте такі параметри: *DprotobufMSVCSTATICRUNTIME=OFF -DprotobufBUILDSHAREDLIBS=OFF*
    
-   Google Protocol Buffers / protocol compiler (protoc): обов'язкові, переконайтеся, що під час складання в PATH доступний правильний 'protoc'. Це особливо важливо, оскільки пакетні сценарії Windows PHP SDK можуть перезаписувати оточення.
    
-   Bison: обов'язковий і доступний з PATH.
    
    Примітка до bison на Windows: ми настійно рекомендуємо, щоб bison, що поставляється з вибраним PHP SDK, використовував ще одну помилку, схожу на "zend"globalsmacros.h(39): error C2375: 'zendparse': redefinition; different linkage Zend/zendlanguageparser.h(214): примітка: note: see declaration of 'zendparse'". Крім того, пакетні сценарії Windows PHP SDK можуть перезаписувати оточення.
    
-   Примітки для Windows: Щоб підготувати оточення, перегляньте офіційну документацію зі збирання Windows для [» поточного SDK](https://wiki.php.net/internals/windows/stepbystepbuild_sdk_2)
    
    Ми рекомендуємо використовувати зворотну косу рису '' замість косої межі '/' для всіх шляхів.