---
navigation:
  - cubrid.configuration.md: « Налаштування під час виконання
  - cubrid.constants.md: Обумовлені константи »
  - index.md: PHP Manual
  - cubrid.setup.md: Встановлення та налаштування
title: Типи ресурсів
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Типи ресурсів

Існує чотири типи ресурсів, що використовуються в CUBRID. Перший - ідентифікатор з'єднання, другий - ресурс, що зберігає результат запиту, і останні два містять результати запиту типів BLOB/CLOB.

## ідентифікатор з'єднання

Ідентифікатор з'єднання, що повертається функціями [cubrid\_connect()](function.cubrid-connect.md) [cubrid\_connect\_with\_url()](function.cubrid-connect-with-url.md) [cubrid\_pconnect()](function.cubrid-pconnect.md) і [cubrid\_pconnect\_with\_url()](function.cubrid-pconnect-with-url.md)

## request identifier

Ідентифікатор запиту, що повертається функціями [cubrid\_prepare()](function.cubrid-prepare.md) і [cubrid\_execute()](function.cubrid-execute.md)

## Ідентифікатор LOB

Ідентифікатор LOB, який повертається функцією [cubrid\_lob\_get()](function.cubrid-lob-get.md)

## LOB2 identifier

Ідентифікатор LOB, який повертається функцією [cubrid\_lob2\_new()](function.cubrid-lob2-new.md) або взятий із результуючого набору.
