---
navigation:
  - function.sodium-crypto-secretstream-xchacha20poly1305-pull.md: « sodium\_crypto\_secretstream\_xchacha20poly1305\_pull
  - function.sodium-crypto-secretstream-xchacha20poly1305-rekey.md: sodium\_crypto\_secretstream\_xchacha20poly1305\_rekey »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_secretstream\_xchacha20poly1305\_push
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_secretstream\_xchacha20poly1305\_push

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_secretstream\_xchacha20poly1305\_push — Шифрує фрагмент даних, щоб можна було безпечно розшифрувати в потоковому API

### Опис

```methodsynopsis
sodium_crypto_secretstream_xchacha20poly1305_push(    string &$state,    string $message,    string $additional_data = "",    int $tag = SODIUM_CRYPTO_SECRETSTREAM_XCHACHA20POLY1305_TAG_MESSAGE): string
```

Шифрує фрагмент даних, щоб його можна було безпечно розшифрувати потоковим API.

### Список параметрів

`state`

Смотрите[sodium\_crypto\_secretstream\_xchacha20poly1305\_init\_pull()](function.sodium-crypto-secretstream-xchacha20poly1305-init-pull.md) і [sodium\_crypto\_secretstream\_xchacha20poly1305\_init\_push()](function.sodium-crypto-secretstream-xchacha20poly1305-init-push.md)

`message`

`additional_data`

`tag`

Не обов'язково. Може використовуватись для підтвердження поведінки дешифрування (тобто повторного введення ключів або вказівки останнього фрагмента в потоці).

-   **`SODIUM_CRYPTO_SECRETSTREAM_XCHACHA20POLY1305_TAG_MESSAGE`**: найпоширеніший тег, який не додає жодної інформації про характер повідомлення.
-   **`SODIUM_CRYPTO_SECRETSTREAM_XCHACHA20POLY1305_TAG_FINAL`**: вказує, що повідомлення відзначає кінець потоку, та стирає секретний ключ, використаний для шифрування попередньої послідовності.
-   **`SODIUM_CRYPTO_SECRETSTREAM_XCHACHA20POLY1305_TAG_PUSH`**: вказує, що повідомлення вказує на кінець набору повідомлень, але не на кінець потоку. Наприклад, величезний рядок JSON, надісланий у вигляді кількох фрагментів, може використовувати цей тег, щоб вказати додатку, що рядок завершено і що його можна декодувати. Але сам потік не закривається і можуть бути додаткові дані.
-   **`SODIUM_CRYPTO_SECRETSTREAM_XCHACHA20POLY1305_TAG_REKEY`**: "забуває" ключ, використаний для шифрування цього та попередніх повідомлень і отримує новий секретний ключ.

### Значення, що повертаються

Повертає зашифрований текст.
