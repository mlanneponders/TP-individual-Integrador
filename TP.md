##Análisis Léxico

####Reemplazo de trigraphs y digraphs 
El reemplazo se realiza antes del linkeo. El que lo realiza es el procesador. 

####Secuencia de tokens:
`int []={-1,}; printf("%d%d",sizeof - sizeof [0],sizeof(char)+ [0]);`

####UT lexicamente correcto 

##Análisis Sintáctico

####Arbol De Derivación
* unidad-de-traducción declaración-externa 
* declaración-externa definición-de-función 
* declaración especificadores-de-declaración
* declarador Proposición-compuesta 
* especificadores-de-declaración lista-de-declaradores-init
* especificador-de-tipo declarador-directo {Lista-declaraciones Lista-de-proposiciones}
* especificador-de-tipo declarador-init int identificador (lista-tipos-de-parametro) {especificadores-de-declaración lista-declaradores-init ; Proposición-expresión} 
* int declarador int main (lista-de-parametros) { Especificador-de-tipo Declarador-init ; expresión ; } 
* int declarador-directo int main (declaración-parámetro) { int Declarador= inicializador; Expresión-de-asignación ; } * int declarador-directo (lista-tipos-de-parametro) int main (especificadores-de-declaración) { int Declarador-directo [] = { Lista-de-inicializadores , } ; Expresión-condicional ; } 
* int identificador (lista-tipos-de-parametro) int main (especificador-de-tipo) { int identificador [] = { inicializador , } ; Expresión-lógica-OR ; } 
* int printf (lista-de-parametros, ...) int main (void)int main (void) { int _ [] = { Expresión-asignación , } ; Expresión-lógica-AND ; } 
* int printf (declaracion-parametro, ...) int main (void) { int _ [] = { Expresión-condicional , } ; Expresión-OR-inclusivo ; } 
* int printf (especificadores-de-declaración declarador, ...) int main (void) { int _ [] = { Expresión-lógica-OR , } ; Expresión-OR-exclusivo ; } 
* int printf (clasificador-de-tipo especificadores-de-declaracion declarador, ...) int main (void) { int _ [] = { Expresión-lógica-AND , } ; Expresión-AND ; } 
* int printf (const especificador-de-tipo declarador, ...) int main (void) { int _ [] = { Expresión-OR-inclusivo , } ; Expresión-de-igualdad ; } 
* int printf (const char apuntador declarador-directo, ..) int main (void) { int _ [] = { Expresión-OR-exclusivo , } ; Expresión-relacional ; }
* int printf (const char * identificador, ...) int main (void) { int _ [] = { Expresión-AND , } ; Expresión-de-corrimiento ; } 
* int printf (const char ,...) int main (void) { int _ [] = { Expresión-de-igualdad , } ; Expresión-aditiva ; } 
* int printf (const char *,...) int main (void) { int _ [] = { Expresión-relacional , } ; Expresión-multiplicativa ; } * int printf (const char *,...) int main (void) { int _ [] = { Expresión-de-corrimiento , } ; Expresión-unaria ; } 
* int printf (const char *,...) int main (void) { int _ [] = { Expresión-aditiva , } ; Expresión-posfija ; } 
* int printf (const char *,...) int main (void) { int _ [] = { Expresión-multiplicativa , } ; Expresión-posfija ( Lista-de-expresiones-argumento) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { Expresión-unaria , } ; Expresión-primaria ( Lista-de-expresiones-argumento, Expresión-asignación ) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { Operador-unario Expresión-unaria, } ; identificador ( Lista-de-expresiones-argumento , Expresión-asignación, Expresión-asignación ) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { - Operador-unario Expresión-unaria , } ; printf ( Expresión-asignación , Expresión-asignación, Expresión-asignación ) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { - ! Expresión-posfija , } ; printf ( Expresión-condicional , Expresión-condicional, Expresión-condicional ) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { - ! Expresión-primaria , } ; printf ( Expresión-lógica-OR , Expresión-lógica-OR, Expresión-lógica-OR ) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { - ! constante , } ; printf ( Expresión-lógica-AND , Expresión-lógica-AND, Expresión-lógica-AND ) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { - ! Constante-flotante , } ; printf ( Expresión-OR-inclusivo , Expresión-OR-inclusivo, Expresión-OR-inclusivo ) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( Expresión-OR-exclusivo , Expresión-OR-exclusivo, Expresión-OR-exclusivo ) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( Expresión-AND , Expresión-AND, Expresión-AND ) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( Expresión-de-igualdad , Expresión-de-igualdad, Expresión-de-igualdad ) ; }
* int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( Expresión-relacional , Expresión-relacional, Expresión-relacional ) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( Expresión-de-corrimiento , Expresión-de-corrimiento, Expresión-de-corrimiento ) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( Expresión-aditiva , Expresión-aditiva, Expresión-aditiva ) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( Expresión-multiplicativa , Expresión-aditiva- Expresión-multiplicativa , Expresión-aditiva Expresión-multiplicativa) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( Expresión-unaria , Expresión-multiplicativa- Expresión-unaria , Expresión-multiplicativa Expresión-unaria) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( Expresión-posfija , Expresión-unaria- sizeof Expresión-unaria, Expresión-unaria Expresión-posfija) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( Expresión-primaria , sizeof Expresión-unaria - sizeof Expresión-posfija, sizeof ( Nombre-de-tipo ) Expresión-posfija [ expresión ] ) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( cadena , sizeof Expresión-posfija - sizeof Expresión-posfija [ expresión ] , sizeof ( char ) Expresión-primaria [ Expresión-asignación ] ) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof Expresión-primaria - sizeof Expresión-primaria [ Expresión-asignación ] , sizeof ( char ) constante [ Expresión-condicional ] ) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof identificador - sizeof identificador [ Expresión-condicional ] , sizeof ( char ) Constante-entera [ Expresión-lógica-OR ] ) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ Expresión-lógica-OR ] , sizeof ( char ) 0 [ Expresión-lógica-AND ] ) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ Expresión-lógica-AND ] , sizeof ( char ) 0 [ Expresión-OR-inclusivo ] ) ; }
* int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ Expresión-OR-inclusivo ] , sizeof ( char ) 0 [ Expresión-OR-exclusivo ] ) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ Expresión-OR-exclusivo ] , sizeof ( char ) 0 [ Expresión-AND ] ) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ Expresión-AND ] , sizeof ( char ) 0 [ Expresión-de-igualdad ] ) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ Expresión-de-igualdad ] , sizeof ( char ) 0 [ Expresión-relacional ] ) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ Expresión-relacional ] , sizeof ( char ) 0 [ Expresión-de-corrimiento ] ) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ Expresión-de-corrimiento ] , sizeof ( char ) 0 [ Expresión-aditiva ] ) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ Expresión-aditiva ] , sizeof ( char ) 0 [ Expresión-multiplicativa ] ) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ Expresión-multiplicativa ] , sizeof ( char ) 0 [ Expresión-unaria ] ) ; }
* int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ Expresión-unaria ] , sizeof ( char ) 0 [ Expresión-posfija ] ) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ Expresión-posfija ] , sizeof ( char ) 0 [ Expresión-primaria ] ) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ Expresión-primaria ] , sizeof ( char ) 0 [ identificador ] ) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ constante ] , sizeof ( char ) 0 [ _ ] ) ; } 
* int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ Constante-entera ] , sizeof ( char ) 0 [ _ ] ) ; }
* int printf (const char *,...) int main (void) { int _ [] = { - ! .0 , } ; printf ( "%d%d" , sizeof _ - sizeof _ [ 0 ] , sizeof ( char ) 0 [ _ ] ) ; } 

####Unidad de Traducción sintácticamente correcta

##Análisis Semántico

La UT es lexicamente correcta y no viola ninguna restriccion semantica.

Primeramente el programa declara una funcion llamada printf y luego dentro de la funcion main, inicializa un arreglo de enterors e imprime por pantalla el resultado de 2 expresiones en cuyos operandos estan involucrados el arreglo y la la funcion sizeof.

Es semanticamente correcto.
La salida del programa imprime los caracteres 00.
