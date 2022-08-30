Встановлює МЮ-фактор quickprop

-   [« fannsetquickpropdecay](function.fann-set-quickprop-decay.html)
    
-   [fannsetrpropdecreasefactor »](function.fann-set-rprop-decrease-factor.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Fann](ref.fann.html)
    
-   Встановлює МЮ-фактор quickprop
    

# fannsetquickpropму

(PECL fann> = 1.0.0)

fannsetquickpropmu - Встановлює МЮ-фактор quickprop

### Опис

```methodsynopsis
fann_set_quickprop_mu(resource $ann, float $quickprop_mu): bool
```

Встановлює МЮ-фактор quickprop.

### Список параметрів

`ann`

Ресурс нейронної мережі.

`quickprop_mu`

МЮ-фактор quickprop.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`** в іншому випадку.

### Дивіться також

-   [fanngetquickpropmu()](function.fann-get-quickprop-mu.html) - Повертає коефіцієнт mu