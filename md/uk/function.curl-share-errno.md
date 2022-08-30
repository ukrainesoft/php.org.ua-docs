Повертає код останньої помилки оброблюваного обробника curl

-   [« curlshareclose](function.curl-share-close.html)
    
-   [curlshareinit »](function.curl-share-init.html)
    
-   [PHP Manual](index.html)
    
-   [Функции cURL](ref.curl.html)
    
-   Повертає код останньої помилки оброблюваного обробника curl
    

# curlshareerrno

(PHP 7> = 7.1.0, PHP 8)

curlshareerrno — Повертає код останньої помилки оброблюваного обробника curl

### Опис

```methodsynopsis
curl_share_errno(CurlShareHandle $share_handle): int
```

Повертає код останньої помилки оброблюваного curl, що розділяється, у вигляді цілого числа.

### Список параметрів

`share_handle`

Обробник cURL, що розділяється, повертається [curlshareinit()](function.curl-share-init.html)

### Значення, що повертаються

Повертає код останньої помилки curl, що розділяється, у вигляді цілого числа або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція більше не повертає **`false`** у разі виникнення помилки. |
|  | `share_handle` expects a [CurlShareHandle](class.curlsharehandle.html) instance now; Попередньо, як ресурс був виявлений. |

### Дивіться також

-   [curlerrno()](function.curl-errno.html) - Повертає код останньої помилки