---
navigation:
  - yac.resources.md: « Типи ресурсів
  - class.yac.md: Yac »
  - index.md: PHP Manual
  - book.yac.md: Yac
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи визначені цим модулем і доступні або в збірках PHP з підтримкою цього модуля, або коли модуль динамічно завантажений під час виконання коду.

**`YAC_VERSION`**(string)

**`YAC_MAX_KEY_LEN`**(int)

Максимальна довжина ключа може бути 48 байт.

**`YAC_MAX_VALUE_RAW_LEN`**(int)

**`YAC_MAX_RAW_COMPRESSED_LEN`**(int)

**`YAC_SERIALIZER_PHP`**(int)

Використовувати php serialize як серіалізатор

**`YAC_SERIALIZER_JSON`**(int)

Використовувати json як серіалізатор (потрібно --enable-json)

**`YAC_SERIALIZER_IGBINARY`**(int)

Використовувати igbinary як серіалізатор (потрібно --enable-igbinary)

**`YAC_SERIALIZER_MSGPACK`**(int)

Використовувати msgpack як серіалізатор (потрібно --enable-msgpack)

**`YAC_SERIALIZER`**(string)

Який серіалізатор використовується в yac
