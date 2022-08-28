Встановлює callback-функцію для використання під час навчання

-   [« fann\_set\_bit\_fail\_limit](function.fann-set-bit-fail-limit.html)
    
-   [fann\_set\_cascade\_activation\_functions »](function.fann-set-cascade-activation-functions.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Встановлює callback-функцію для використання під час навчання
    

# fannsetcallback

(PECL fann> = 1.0.0)

fannsetcallback - Встановлює callback-функцію для використання під час навчання

### Опис

```methodsynopsis
fann_set_callback(resource $ann, callable $callback): bool
```

Встановлює callback-функцію використання під час навчання. Це означає, що вона викликається з [fann\_train\_on\_data()](function.fann-train-on-data.html) або [fann\_train\_on\_file()](function.fann-train-on-file.html)

### Список параметрів

`ann`

Ресурс нейронної мережі.

`callback`

Callback-функція, що поставляється, приймає наступні параметри:

-   `ann` - Ресурс (resource) нейронної мережі
-   `train` - ресурс даних для навчання або **`null`**, якщо викликається з [fann\_train\_on\_file()](function.fann-train-on-file.html)
-   `max_epochs` - Максимальна кількість періодів, у яких має продовжуватися навчання
-   `epochs_between_reports` - Кількість періодів між викликами цієї функції
-   `desired_error` - Бажана функція [fann\_get\_MSE()](function.fann-get-mse.html) або [fann\_get\_bit\_fail()](function.fann-get-bit-fail.html), залежно від функції зупинки, вибраної [fann\_set\_train\_stop\_function()](function.fann-set-train-stop-function.html)
-   `epochs` - Поточний період

Callback-функція має повернути **`true`**. Якщо вона поверне **`false`**, навчання буде припинено.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fann\_train\_on\_data()](function.fann-train-on-data.html) - Навчання на всьому обсязі даних на часовому інтервалі
-   [fann\_train\_on\_file()](function.fann-train-on-file.html) - Навчання на повному наборі даних, прочитаному з файлу, на часовому інтервалі