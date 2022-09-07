---
navigation:
  - function.sodium-crypto-secretstream-xchacha20poly1305-pull.md: « sodiumcryptosecretstreamxchacha20poly1305pull
  - function.sodium-crypto-secretstream-xchacha20poly1305-rekey.md: sodiumcryptosecretstreamxchacha20poly1305rekey »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptosecretstreamxchacha20poly1305push
---
# sodiumcryptosecretstreamxchacha20poly1305push

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptosecretstreamxchacha20poly1305push — Шифрує фрагмент даних, щоб можна було безпечно розшифрувати в потоковому API

### Опис

```methodsynopsis
sodium_crypto_secretstream_xchacha20poly1305_push(    string &$state,    string $message,    string $additional_data = "",    int $tag = SODIUM_CRYPTO_SECRETSTREAM_XCHACHA20POLY1305_TAG_MESSAGE): string
```

Шифрує фрагмент даних, щоб його можна було безпечно розшифрувати потоковим API.

### Список параметрів

`state`

Дивіться [sodiumcryptosecretstreamxchacha20poly1305initpull()](function.sodium-crypto-secretstream-xchacha20poly1305-init-pull.md) і [sodiumcryptosecretstreamxchacha20poly1305initpush()](function.sodium-crypto-secretstream-xchacha20poly1305-init-push.md)

`message`

`additional_data`

`tag`

Не обов'язково. Може використовуватись для підтвердження поведінки дешифрування (тобто повторного введення ключів або вказівки останнього фрагмента в потоці).

-   **`SODIUM_CRYPTO_SECRETSTREAM_XCHACHA20POLY1305_TAG_MESSAGE`**: найпоширеніший тег, який не додає жодної інформації про характер повідомлення.
-   **`SODIUM_CRYPTO_SECRETSTREAM_XCHACHA20POLY1305_TAG_FINAL`**: вказує, що повідомлення відзначає кінець потоку, та стирає секретний ключ, використаний для шифрування попередньої послідовності.
-   **`SODIUM_CRYPTO_SECRETSTREAM_XCHACHA20POLY1305_TAG_PUSH`**: вказує, що повідомлення вказує на кінець набору повідомлень, але не на кінець потоку. Наприклад, величезний рядок JSON, надісланий у вигляді декількох фрагментів, може використовувати цей тег, щоб вказати додатку, що рядок завершено і що його можна декодувати. Але сам потік не закривається і можуть бути додаткові дані.
-   **`SODIUM_CRYPTO_SECRETSTREAM_XCHACHA20POLY1305_TAG_REKEY`**: "забуває" ключ, використаний для шифрування цього та попередніх повідомлень і отримує новий секретний ключ.

### Значення, що повертаються

Повертає зашифрований текст.
