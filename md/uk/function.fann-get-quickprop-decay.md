Повертає зниження, яке є фактором, при якому ваги повинні зменшуватись на кожній ітерації під час навчання quickprop

-   [« fann\_get\_num\_output](function.fann-get-num-output.html)
    
-   [fann\_get\_quickprop\_mu »](function.fann-get-quickprop-mu.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Повертає зниження, яке є фактором, при якому ваги повинні зменшуватись на кожній ітерації під час навчання quickprop
    

# fanngetquickpropdecay

(PECL fann> = 1.0.0)

fanngetquickpropdecay — Повертає зниження, яке є фактором, при якому ваги повинні зменшуватись на кожній ітерації під час навчання quickprop

### Опис

```methodsynopsis
fann_get_quickprop_decay(resource $ann): float
```

Зниження - це невелике число з негативними значеннями, яке є фактором, за яким ваги повинні зменшуватися на кожній ітерації під час навчання quickprop. Використовується для того, щоб під час навчання ваги не ставали надто високими.

The default decay is -0.0001.

### Список параметрів

`ann`

Ресурс нейронної мережі.

### Значення, що повертаються

Зниження або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fann\_set\_quickprop\_decay()](function.fann-set-quickprop-decay.html) - Встановлює коефіцієнт загасання quickprop