# Apunts de PHP

## Introducció

Un script PHP comença amb `<?php` i acaba amb l'etiqueta `?>`.

Els fitxers PHP són fitxers de text senzill amb .phpextensió. Dins d'un fitxer PHP, podeu escriure HTML com ho feu a les pàgines HTML habituals, així com incrustar codis PHP per a l'execució del costat del servidor.

```php
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>A Simple PHP File</title>
</head>
<body>
    <h1><?php echo "Hello, world!"; ?></h1>
</body>
</html>
```

Podeu escriure codi html amb `echo`:

```php
<?php
// Displaying HTML code
echo "<h4>This is a simple heading.</h4>";
echo "<h4 style='color: red;'>This is heading with style.</h4>";
?>
```

## Comentaris

```php
<?php
// This is a single line comment
# This is also a single line comment
echo "Hello, world!";
?>
```

```php
<?php
/*
This is a multiple line comment block
that spans across more than
one line
*/
echo "Hello, world!";
?>
```

## Variables

Les variables s'utilitzen per emmagatzemar dades, com ara una cadena de text, números, etc. Els valors de les variables poden canviar al llarg d'un script.

En PHP, la variable es pot declarar com: `$var_name = value;`

```php
<?php
// Declaring variables
$txt = "Hello World!";
$number = 10;
 
// Displaying variables value
echo $txt;  // Output: Hello World!
echo $number; // Output: 10
?>
```

## Convencions sobre el nom de les variables

* Totes les variables en PHP comencen amb un signe `$`, seguit del nom de la variable.
* El nom d'una variable ha de començar amb una lletra o el caràcter de guió baix _.
* Un nom de variable no pot començar amb un número.
* Un nom de variable en PHP només pot contenir caràcters alfanumèrics i guions baixos ( A-z, 0-9, i _).
* Un nom de variable no pot contenir espais.

## Majúscules i minúscules en el nom de les variables

```php
<?php
// Assign value to variable
$color = "blue";
 
// Try to print variable value
echo "The color of the sky is $color <br>";
echo "The color of the sky is $Color <br>";
echo "The color of the sky is $COLOR <br>";
?>
```

## exercici1.php

Crea una variable que contingui el nom d'un color, en anglès, i fes que es mostri un paràgraf amb el text del color de la variable.

Desprès, crea una segona variable anomenada color de fons, i que el paràgraf tingui de color de fons el valor de la variable.

## Tipus de dades

Nombres enters i decimals:

```php
<?php
$a = 123; // decimal number
echo $a;

$b = -123; // a negative number
echo $b;

$c = 1.234; //a decimal number
echo $c;
?>
```

Booleans:

```php
<?php
$major_edat = false;
echo $major_edat;

$accepta_condicions = true;
echo $accepta_condicions;
?>
```

Cadenes de text:

```php
<?php
$a = 'Hello world!';
echo $a;

$b = 'Ha trucat l\'Alfonso que es troba malament';
echo $b;
?>
```

Text... cometes dobles o simples?

```php
<?php
$my_str = 'World';
echo "Hello, $my_str!<br>";      // Displays: Hello World!
echo 'Hello, $my_str!<br>';      // Displays: Hello, $my_str!
?>
```

Com unir (concatenar) text:

```php
<?php
$x = "Hello";
$y = " World!";
$z = $x . $y;
echo $z // Outputs: Hello World!
?>
```

Llistes:

```php
<?php
$colors = array("Red", "Green", "Blue");
echo $colors[0];
echo "<br />";
echo $colors[1];
echo "<br />";
echo $colors[2];
?>
```

## Operadors aritmètics

```php
<?php
$x = 10;
$y = 4;
echo($x + $y); // suma
echo($x - $y); // resta
echo($x * $y); // multiplicació
echo($x / $y); // divisió
echo($x % $y); // mòdul (resta de la divisió entera)
?>
```

## exercici2.php

Crea una variable que tingui un número i que mostri la taula de multiplicar (del 1 a 10) d'aquest número.

Fes que es mostri la operació sencera:

```txt
2x1 = 2
2x2 = 4
2x3 = 6
...
```

## IF... condicionals

Com la majoria dels llenguatges de programació, PHP també us permet escriure codi que realitzi diferents accions basades en els resultats d'una prova lògica o comparativa de condicions en temps d'execució.

```php
<?php
$edat = 14;
if($edat < 18){
    echo "Ets menor d'edat";
}
?>
```

## IF ... ELSE

```php
<?php
$edat = 24;
if($edat < 18){
    echo "Ets menor d'edat";
} else {
    echo "Ets major d'edat";
}
?>
```

## IF ... ELSEIF ... IF

```php
<?php
$edat = 24;
if($edat < 18){
    echo "Ets menor d'edat";
} elseif ($edat > 65) {
    echo "T'hauries de jubilar";
} else {
    echo "Ets major d'edat";
}
?>
```

## Operadors de comparació

```php
<?php
$x = 25;
$y = 35;

if ($x == $y) {
    echo "$x i $y són iguals";
}

if ($x > $y) {
    echo "$x és més gran que $y";
}

if ($x >= $y) {
    echo "$x és més gran o igual que $y";
}

if ($x < $y) {
    echo "$x és més petit que $y";
}

if ($x <= $y) {
    echo "$x és més petit o igual que $y";
}

if ($x != $y) {
    echo "$x és diferent de $y";
}

if ($x <> $y) {
    echo "$x és diferent de $y";
}
?>
```

```php
<?php
$nom = "alfonso";
if ($nom == "alfonso") {
    echo "Ets l'alfonso";
} else {
    echo "No ets l'alfonso ;(";
}
```

```php
<?php
$accepta_condicions = true;
if ($accepta_condicions) {
?>
    <p>Has acceptat les condicions</p>
<?php
} else {
?>
    <p>No has acceptat les condicions</p>
<?php
}
?>
```

## exercici3.php

Fes un pàgina que tingui una variable que es digui ceba. Quan aquesta variable és true, mostra aquest video https://youtu.be/i7yyMbQkEhc, i quan és false, aquest https://youtu.be/qN0AGcxGvhg

## exercici4.php

Explora la comanda `$d = date("D");`. Et mostra el dia de la setmana que hi som en anglés. Els valors que retorna són: `Sun Mon Tue Wed Thu Fri Sat`.

Fes un programa que mostri un missatge com `Avui és divendres` si avui és divendres, i si avui és dilluns que digui `Avui és dilluns`.

Fes també que el missatge si és cap de setmana digui, per exemple, `Avui és dissabte i no hi ha classe!`.

## Valors aleatoris

```php
<?php
$dau = random_int(1, 6);
echo "He llençat un dau i ha sortit: $dau";
?>
```

## exercici5.php

Modifica l'exemple anterior per a que mostri el número escrit, és a dir, no ha de dir `He llençat un dau i ha sortit: 3`, ha de dir `He llençat un dau i ha sortit el tres`.

Afegeix un enllaç a la pàgina per a que torni a executar-se el teu script. Ha de ser un enllaç a la teva pròpia pàgina.

## Bucles

https://www-tutorialrepublic-com.translate.goog/php-tutorial/php-loops.php?_x_tr_sl=en&_x_tr_tl=ca&_x_tr_hl=ca&_x_tr_pto=wapp