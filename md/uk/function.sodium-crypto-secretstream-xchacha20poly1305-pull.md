---
navigation:
  - function.sodium-crypto-secretstream-xchacha20poly1305-keygen.md: « sodiumcryptosecretstreamxchacha20poly1305keygen
  - function.sodium-crypto-secretstream-xchacha20poly1305-push.md: sodiumcryptosecretstreamxchacha20poly1305push »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptosecretstreamxchacha20poly1305pull
---
# sodiumcryptosecretstreamxchacha20poly1305pull

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptosecretstreamxchacha20poly1305pull — Розшифровує частину даних із зашифрованого потоку

### Опис

```methodsynopsis
sodium_crypto_secretstream_xchacha20poly1305_pull(string &$state, string $ciphertext, string $additional_data = ""): array|false
```

Розшифровує частину даних із зашифрованого потоку.

### Список параметрів

`state`

Дивіться [sodiumcryptosecretstreamxchacha20poly1305initpull()](function.sodium-crypto-secretstream-xchacha20poly1305-init-pull.md) і [sodiumcryptosecretstreamxchacha20poly1305initpush()](function.sodium-crypto-secretstream-xchacha20poly1305-init-push.md)

`ciphertext`

Фрагмент зашифрованого тексту, який потрібно розшифрувати.

`additional_data`

Необов'язкові додаткові дані для включення в тег аутентифікації.

### Значення, що повертаються

Масив із двома значеннями:

-   Рядок (string); Розшифрований фрагмент
    
-   Ціле число (int); Необов'язковий тег (якщо надається під час надсилання). Можливі значення:
    
    -   **`SODIUM_CRYPTO_SECRETSTREAM_XCHACHA20POLY1305_TAG_MESSAGE`**: найпоширеніший тег, який не додає жодної інформації про характер повідомлення.
    -   **`SODIUM_CRYPTO_SECRETSTREAM_XCHACHA20POLY1305_TAG_FINAL`**: вказує, що повідомлення відзначає кінець потоку, та стирає секретний ключ, використаний для шифрування попередньої послідовності.
    -   **`SODIUM_CRYPTO_SECRETSTREAM_XCHACHA20POLY1305_TAG_PUSH`**: вказує, що повідомлення вказує на кінець набору повідомлень, але не на кінець потоку. Наприклад, величезний рядок JSON, надісланий у вигляді декількох фрагментів, може використовувати цей тег, щоб вказати додатку, що рядок завершено і що його можна декодувати. Але сам потік не закривається і можуть бути додаткові дані.
    -   **`SODIUM_CRYPTO_SECRETSTREAM_XCHACHA20POLY1305_TAG_REKEY`**: "забуває" ключ, використаний для шифрування цього та попередніх повідомлень і отримує новий секретний ключ.
