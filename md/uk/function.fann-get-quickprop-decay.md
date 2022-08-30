Повертає зниження, яке є фактором, при якому ваги повинні зменшуватись на кожній ітерації під час навчання quickprop

-   [« fanngetnumoutput](function.fann-get-num-output.html)
    
-   [fanngetquickpropmu »](function.fann-get-quickprop-mu.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Fann](ref.fann.md)
    
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

-   [fannsetquickpropdecay()](function.fann-set-quickprop-decay.html) - Встановлює коефіцієнт загасання quickprop