---
navigation:
  - function.rnp-op-sign.md: « rnp\_op\_sign
  - function.rnp-op-verify.md: rnp\_op\_verify »
  - index.md: PHP Manual
  - ref.rnp.md: Функції Rnp
title: rnp\_op\_verify\_detached
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rnp\_op\_verify\_detached

(PECL rnp >= 0.1.1)

rnp\_op\_verify\_detached — Перевіряє від'єднані підписи

### Опис

```methodsynopsis
rnp_op_verify_detached(RnpFFI $ffi, string $data, string $signature): array|false
```

### Список параметрів

`ffi`

Об'єкт FFI, що повертається функцією rnp\_ffi\_create.

`data`

Вихідні дані.

`signature`

Дані від'єднаного підпису.

### Значення, що повертаються

Асоціативний масив, що містить інформацію про результати перевірки або \*\*`false`\*\*в случае возникновения ошибки.

| Ключ | Тип данных | Опис |
| --- | --- | --- |
| `"verification_status"` | string | Загальний результат перевірки або рядок "Success", або відповідне повідомлення про помилку. Результат "Success" встановлюється, якщо хоча б один підпис є дійсним та успішно перевірений. Індивідуальні результати перевірки для кожного підпису можна перевірити у масиві "signatures". |
| `"file_name"` | string | Ім'я файлу. |
| `"file_mtime"` | integer | Час зміни файлу. |
| `"mode"` | string | Режим захисту даних (шифрування), що використовується в повідомленні, що обробляється. В даний час визначено такі значення: "none", "cfb", "cfb-mdc", "aead-ocb", "aead-eax". |
| `"cipher"` | string | Симетричний шифр, який використовується для шифрування даних. |
| `"valid_integrity"` | boolean | **`true`**, якщо використовувався захист цілісності повідомлення (тобто MDC або AEAD) і він успішно підтверджено. |
| `"signatures"` | array | Асоціативний масив, що описує кожен знайдений підпис. Дивіться опис нижче. |

Дочірній масив "signatures".

| Ключ | Тип данных | Опис |
| --- | --- | --- |
| "verification\_status" | string | Статус перевірки підпису або рядок "Success" або відповідне повідомлення про помилку. |
| "creation\_time" | integer | Час створення підпису в секундах з 1 січня 1970 року за Грінвічем. |
| "expiration\_time" | integer | Час закінчення терміну дії підпису в секундах з моменту створення або 0, якщо термін дії підпису не закінчується. |
| "hash" | string | Алгоритм хеш-функції, який використовується для обчислення підпису. |
| "signing\_key" | string | Цифровий відбиток ключа для підпису. Може мати значення Not found, якщо відповідний відкритий ключ не завантажений в об'єкт FFI. |
| "signature\_type" | string | Тип підпису. В даний час визначені наступні значення: 'binary', 'text', 'standalone', 'certification (generic)', 'certification (persona)', 'certification (casual)', 'certification (positive)', 'subkey binding ', 'primary key binding', 'direct', 'key revocation', 'subkey revocation', 'certification revocation', 'timestamp', 'uknown: 0..255'. |
