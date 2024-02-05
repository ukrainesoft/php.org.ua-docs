---
navigation:
  - mqseries.resources.md: « Типи ресурсів
  - ref.mqseries.md: Функції mqseries »
  - index.md: PHP Manual
  - book.mqseries.md: mqseries
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Для кожної константи WebSphere MQ існує її відображення в mqseries.

Про їх значення та використання читайте у книгах "WebSphere MQ Application Programming Guide" та "WebSphere MQ Application Programming Reference".

Імена двійників констант в mqseries можна визначити, прибравши з констант PHP префікс MQSERIES\_. Наприклад, константи CompletionCode:

**Константи mqseries**

| Константа PHP | Константа MQ |
| --- | --- |
| MQSERIES\_MQCC\_OK | MQCC\_OK |
| MQSERIES\_MQCC\_WARNING | MQCC\_WARNING |
| MQSERIES\_MQCC\_FAILED | MQCC\_FAILED |
| MQSERIES\_MQCC\_UNKNOWN | MQCC\_UNKNOWN |
