---
navigation:
  - ocilob.export.html: '« OCILob::export'
  - ocilob.free.html: 'OCILob::free »'
  - index.html: PHP Manual
  - class.ocilob.html: OCILob
title: 'OCILob::flush'
---
# OCILob::flush

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

OCILob::flush — Очищає та записує буфер об'єкта LOB на сервер

### Опис

```methodsynopsis
public OCILob::flush(int $flag = 0): bool
```

**OCILob::flush()** безпосередньо записує дані на сервер.

### Список параметрів

`flag`

За замовчуванням ресурси не звільняються, але використовуючи прапор **`OCI_LOB_BUFFER_FREE`** ви можете це зробити примусово. Однак, ви повинні бути точно впевнені в тому, що ви робите, тому що наступне читання з об'єкта буде більш ресурсомістким, ніж попередні через необхідність звернення до сервера. Тому використати прапор **`OCI_LOB_BUFFER_FREE`** рекомендується лише після того, як роботу з об'єктом вже закінчено.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

Повертає **`false`** у разі виникнення помилки або якщо буферизація об'єкта не була увімкнена.

### список змін

| Версия | Описание |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Клас **OCI-Lob** перейменований на [OCILob](class.ocilob.html) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCILob::getBuffering](ocilob.getbuffering.html)
-   [OCILob::setBuffering](ocilob.setbuffering.html)
