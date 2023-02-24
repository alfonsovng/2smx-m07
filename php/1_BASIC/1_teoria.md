# PHP BÀSIC

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

**[Fes l'exercici 1](1_exercicis.md)**


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

**[Fes l'exercici 2](1_exercicis.md)**

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

**[Fes l'exercici 3](1_exercicis.md)**

**[Fes l'exercici 4](1_exercicis.md)**

## Valors aleatoris

```php
<?php
$dau = random_int(1, 6);
echo "He llençat un dau i ha sortit: $dau";
?>
```

**[Fes l'exercici 5](1_exercicis.md)**

## Bucles

Els bucles s'utilitzen per executar el mateix bloc de codi una vegada i una altra, sempre que es compleixi una determinada condició. La idea bàsica darrere d'un bucle és automatitzar les tasques repetitives dins d'un programa per estalviar temps i esforç.

PHP admet quatre tipus diferents de bucles.

* while: fa un bucle a través d'un bloc de codi sempre que la condició especificada s'avaluï com a vertadera.
* do ... while: el bloc de codi executat una vegada i després s'avalua la condició. Si la condició és certa, la declaració es repeteix sempre que la condició especificada sigui certa.
* for: recorre un bloc de codi fins que el comptador arriba a un número especificat.
* foreach: recorre un bloc de codi per a cada element d'una llista.

## FOR

El bucle `for` repeteix un bloc de codi sempre que es compleixi una determinada condició. Normalment s'utilitza per executar un bloc de codi un nombre determinat de vegades.

```text
for(inicialització; condició; increment){
    // Codi a executar
}
```

Exemple:

```php
<?php
for($i=1; $i<=3; $i = $i + 1){
    echo "The number is " . $i . "<br>";
}
?>
```

**[Fes l'exercici 6](1_exercicis.md)**

**[Fes l'exercici 7](1_exercicis.md)**

**[Fes l'exercici 8](1_exercicis.md)**

## FOREACH

El bucle foreach s'utilitza per iterar sobre llistes.

```text
foreach ($array com a $valor){
    // Codi a executar
}
```

Exemple:

```php
<?php
$colors = array("red", "green", "blue");
 
// Loop through colors array
foreach($colors as $value){
    echo $value . "<br>";
}
?>
```

**[Fes l'exercici 9](1_exercicis.md)**

**[Fes l'exercici 10](1_exercicis.md)**
