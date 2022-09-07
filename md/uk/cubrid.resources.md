---
navigation:
  - cubrid.configuration.md: « Налаштування під час виконання
  - cubrid.constants.md: Обумовлені константи »
  - index.md: PHP Manual
  - cubrid.setup.md: Встановлення та налаштування
title: Типи ресурсів
---
## Типи ресурсів

Існує чотири типи ресурсів, що використовуються в CUBRID. Перший - ідентифікатор з'єднання, другий - ресурс, що зберігає результат запиту, і останні два містять результати запиту типів BLOB/CLOB.

## ідентифікатор з'єднання

Ідентифікатор з'єднання, що повертається функціями [cubridconnect()](function.cubrid-connect.md) [cubridconnectwithurl()](function.cubrid-connect-with-url.md) [cubridpconnect()](function.cubrid-pconnect.md) і [cubridpconnectwithurl()](function.cubrid-pconnect-with-url.md)

## request identifier

Ідентифікатор запиту, що повертається функціями [cubridprepare()](function.cubrid-prepare.md) і [cubridexecute()](function.cubrid-execute.md)

## Ідентифікатор LOB

Ідентифікатор LOB, який повертається функцією [cubridlobget()](function.cubrid-lob-get.md)

## LOB2 identifier

Ідентифікатор LOB, який повертається функцією [cubridlob2new()](function.cubrid-lob2-new.md) або взятий із результуючого набору.
