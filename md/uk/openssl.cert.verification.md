---
navigation:
  - openssl.certparams.md: « Параметри ключа/сертифіката
  - ref.openssl.md: Функції OpenSSL »
  - index.md: PHP Manual
  - book.openssl.md: OpenSSL
title: Перевірка сертифікатів
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Перевірка сертифікатів

Коли відбувається функція перевірки підпису/сертифіката, параметр `ca_info` повинен містити масив файлів та директорій, що вказують на розміщення довірених кореневих сертифікатів. Якщо вказується директорія, вона має відповідати директорії, яку зможе використати команда **openssl**
