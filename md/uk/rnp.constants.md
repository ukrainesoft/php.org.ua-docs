---
navigation:
  - rnp.resources.md: « Типи ресурсів
  - rnp.examples.md: Приклади »
  - index.md: PHP Manual
  - book.rnp.md: Rnp
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи визначені цим модулем і доступні або в збірках PHP з підтримкою цього модуля, або коли модуль динамічно завантажений під час виконання коду.

**`RNP_KEYSTORE_GPG`**(string)

Формат сховища ключів "GPG".

**`RNP_KEYSTORE_KBX`**(string)

Формат сховища ключів KBX. Лише для відкритих ключів. Сховище ключів - це формат файлу, який використовується для зберігання відкритих ключів разом із метаінформацією та індексами.

**`RNP_KEYSTORE_G10`**(string)

Формат сховища ключів "G10". Для закритих ключів

**`RNP_LOAD_SAVE_PUBLIC_KEYS`**(integer)

Завантаження або збереження лише відкритих ключів. Можливо АБО з константою **`RNP_LOAD_SAVE_SECRET_KEYS`** для завантаження відкритих та закритих ключів у контекст FFI або збереження їх із контексту.

**`RNP_LOAD_SAVE_SECRET_KEYS`**(integer)

Завантаження або збереження лише секретних ключів. Можливо АБО з константою **`RNP_LOAD_SAVE_PUBLIC_KEYS`** для завантаження відкритих та закритих ключів у контекст FFI або збереження їх із контексту.

**`RNP_LOAD_SAVE_PERMISSIVE`**(integer)

Дозволяє ігнорувати пакети поганих підписів/ключів/дочірніх ключів під час імпорту ключів.

**`RNP_LOAD_SAVE_SINGLE`**(integer)

Якщо встановлено, буде завантажено лише перший ключ.

**`RNP_LOAD_SAVE_BASE64`**(integer)

Дозволити імпортувати base64-кодовані ключі (autocrypt).

**`RNP_FEATURE_SYMM_ALG`**(string)

Список доступних алгоритмів симетричного шифрування.

**`RNP_FEATURE_AEAD_ALG`**(string)

Список доступних алгоритмів AEAD.

**`RNP_FEATURE_PROT_MODE`**(string)

Список доступних режимів захисту.

**`RNP_FEATURE_PK_ALG`**(string)

Список доступних алгоритмів відкритих ключів

**`RNP_FEATURE_HASH_ALG`**(string)

Список доступних хеш-алгоритмів.

**`RNP_FEATURE_COMP_ALG`**(string)

Список доступних алгоритмів стиснення.

**`RNP_FEATURE_CURVE`**(string)

Список доступних еліптичних кривих.

**`RNP_DUMP_MPI`**(integer)

Вивантаження значень MPI (багатоточкових цілих чисел).

**`RNP_DUMP_RAW`**(integer)

Вивантаження вмісту необробленого пакета.

**`RNP_DUMP_GRIP`**(integer)

Вивантаження цифрового відбитка та захоплення клавіш.

**`RNP_JSON_DUMP_MPI`**(integer)

Вивантаження значень MPI (багатоточкових цілих чисел).

**`RNP_JSON_DUMP_RAW`**(integer)

Вивантаження вмісту необробленого пакета.

**`RNP_JSON_DUMP_GRIP`**(integer)

Вивантаження цифрових відбитків пальців та захватів клавіш.

**`RNP_ENCRYPT_NOWRAP`**(integer)

Дозволяє зашифрувати підписане повідомлення. Повідомлення не загортається в малий пакет даних.

**`RNP_KEY_EXPORT_ARMORED`**(integer)

Увімкнення ASCII-перетворення експортованих даних.

**`RNP_KEY_EXPORT_PUBLIC`**(integer)

Експорт відкритий ключ.

**`RNP_KEY_EXPORT_SECRET`**(integer)

Експорт закритого ключа.

**`RNP_KEY_EXPORT_SUBKEYS`**(integer)

Якщо первинний ключ експортується, всі дочірні ключі також будуть експортовані.

**`RNP_KEY_EXPORT_BASE64`**(integer)

Експорт ключа автоматичного шифрування в base64-кодуванні замість двійкового.

**`RNP_KEY_REMOVE_PUBLIC`**(integer)

Видалення відкритого ключа.

**`RNP_KEY_REMOVE_SECRET`**(integer)

Видалення закритого ключа.

**`RNP_KEY_REMOVE_SUBKEYS`**(integer)

Якщо видаляється первинний ключ, всі його дочірні ключі також будуть видалені.
