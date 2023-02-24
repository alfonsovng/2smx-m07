# PHP BÀSIC

## exercici1.php

Crea una variable que contingui el nom d'un color, en anglès, i fes que es mostri un paràgraf amb el text del color de la variable.

Desprès, crea una segona variable anomenada color de fons, i que el paràgraf tingui de color de fons el valor de la variable.

*ADVANCED MODE: css en un fitxer a part i fes servir classes CSS*

## exercici2.php

Crea una variable que tingui un número i que mostri la taula de multiplicar (del 1 a 10) d'aquest número.

Fes que es mostri la operació sencera:

```txt
2x1 = 2
2x2 = 4
2x3 = 6
...
```

*ADVANCED MODE: que ho mostri en una taula*

## exercici3.php

Fes un pàgina que tingui una variable que es digui ceba. Quan aquesta variable és true, mostra aquest video https://youtu.be/i7yyMbQkEhc, i quan és false, aquest https://youtu.be/qN0AGcxGvhg

[Aquest enllaç et mostra com afegir un video youtube a la teva pàgina](https://como.help/programacion/html/como-insertar-un-video-de-youtube-en-html)

*ADVANCED MODE: minimitza el codi HTML per a evitar repetir etiquetes*

## exercici4.php

Explora la comanda `$d = date("D");`. Et mostra el dia de la setmana que hi som en anglés. Els valors que retorna són: `Sun Mon Tue Wed Thu Fri Sat`.

Fes una pàgina que mostri un missatge com `Avui és divendres` si avui és divendres, i si avui és dilluns que digui `Avui és dilluns`.

Fes també que el missatge si és cap de setmana digui, per exemple, `Avui és dissabte i no hi ha classe!`.

*ADVANCED MODE: que mostri el mes també*

## exercici5.php

Modifica l'exemple del dau per a que mostri el número escrit, és a dir, no ha de dir

`He llençat un dau i ha sortit: 3`

ha de dir

`He llençat un dau i ha sortit el tres`.

Afegeix un enllaç a la pàgina per a que torni a executar-se el teu script. Ha de ser un enllaç a la teva pròpia pàgina.

*ADVANCED MODE: que mostri una imatge amb un dau mostrant el número. Pots agafar les imatges d'aquí: https://www.random.org/dice/?num=20*

## exercici6.php

Repeteix l'exercici de la taula de multiplicar però fent servir un bucle for.

*ADVANCED MODE: que mostri el resultat en una taula*

## exercici7.php

Fes una pàgina on es calculi un valor aleatori entre 1 i 100 i es mostri per pantalla tots els números del 1 fins al valor aleatori. És a dir, que si surt el 6, es mostrin els números del 1 al 6.

*ADVANCED MODE: que mostri el resultat en una taula de 10 columnes*

## exercici8.php

Observa aquest exemple, on hi ha un bucle dins d'un altre bucle:

```php
<?php
for($i=1; $i<=3; $i++){
    for($j=1; $j<=3; $j++){
        suma = $i + $j;
        echo "$i + $j = $suma";
    }
}
?>
```

Ara fes una pàgina que mostri totes les taules de multiplicar de l'1 al 10.

*ADVANCED MODE: que mostri el resultat en una taula 10x10*

## exercici9.php

Modifica l'exemple del bucler `foreach` per a que mostri una llista numerada dels colors.

Desprès, fes que cada element de la llista es mostri del color que correspon. Per exemple, que red es mostri amb text vermell.

*ADVANCED MODE: fes servir un fitxer a part pel CSS i fes servir classes*

## exercici10.php

Crea una llista amb les 4 URLs de la wikipedia següents:

* https://ca.wikipedia.org/wiki/Barcelona
* https://ca.wikipedia.org/wiki/Tarragona
* https://ca.wikipedia.org/wiki/Lleida
* https://ca.wikipedia.org/wiki/Girona

Fes una pàgina que mostri les 4 URLs de la llista en forma d'enllaç.

*ADVANCED MODE: no guardis la URL completa a la llista, sols el nom de la ciutat*
