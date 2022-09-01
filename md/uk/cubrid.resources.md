---
navigation:
  - cubrid.configuration.html: « Налаштування під час виконання
  - cubrid.constants.html: Обумовлені константи »
  - index.html: PHP Manual
  - cubrid.setup.html: Встановлення та налаштування
title: Типи ресурсів
---
## Типи ресурсів

Існує чотири типи ресурсів, що використовуються в CUBRID. Перший - ідентифікатор з'єднання, другий - ресурс, що зберігає результат запиту, і останні два містять результати запиту типів BLOB/CLOB.

## ідентифікатор з'єднання

Ідентифікатор з'єднання, що повертається функціями [cubridconnect()](function.cubrid-connect.html) [cubridconnectwithurl()](function.cubrid-connect-with-url.html) [cubridpconnect()](function.cubrid-pconnect.html) і [cubridpconnectwithurl()](function.cubrid-pconnect-with-url.html)

## request identifier

Ідентифікатор запиту, що повертається функціями [cubridprepare()](function.cubrid-prepare.html) і [cubridexecute()](function.cubrid-execute.html)

## Ідентифікатор LOB

Ідентифікатор LOB, який повертається функцією [cubridlobget()](function.cubrid-lob-get.html)

## LOB2 identifier

Ідентифікатор LOB, який повертається функцією [cubridlob2new()](function.cubrid-lob2-new.html) або взятий із результуючого набору.
