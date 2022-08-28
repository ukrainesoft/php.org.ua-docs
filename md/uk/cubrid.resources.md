Типи ресурсів

-   [« Настройка во время выполнения](cubrid.configuration.html)
    
-   [Предопределённые константы »](cubrid.constants.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](cubrid.setup.html)
    
-   Типи ресурсів
    

## Типи ресурсів

Існує чотири типи ресурсів, що використовуються в CUBRID. Перший - ідентифікатор з'єднання, другий - ресурс, що зберігає результат запиту, і останні два містять результати запиту типів BLOB/CLOB.

## ідентифікатор з'єднання

Ідентифікатор з'єднання, що повертається функціями [cubrid\_connect()](function.cubrid-connect.html) [cubrid\_connect\_with\_url()](function.cubrid-connect-with-url.html) [cubrid\_pconnect()](function.cubrid-pconnect.html) і [cubrid\_pconnect\_with\_url()](function.cubrid-pconnect-with-url.html)

## request identifier

Ідентифікатор запиту, що повертається функціями [cubrid\_prepare()](function.cubrid-prepare.html) і [cubrid\_execute()](function.cubrid-execute.html)

## Ідентифікатор LOB

Ідентифікатор LOB, який повертається функцією [cubrid\_lob\_get()](function.cubrid-lob-get.html)

## LOB2 identifier

Ідентифікатор LOB, який повертається функцією [cubrid\_lob2\_new()](function.cubrid-lob2-new.html) або взятий із результуючого набору.