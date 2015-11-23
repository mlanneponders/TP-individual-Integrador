##Análisis Léxico

####Reemplazo de trigraphs y digraphs 
El reemplazo se realiza antes del linkeo. El que lo realiza es el procesador. 

####Secuencia de tokens:
`int []={-1,}; printf("%d%d",sizeof - sizeof [0],sizeof(char)+ [0]);`

####UT lexicamente correcto 

##Análisis Sintáctico

####Arbol De Derivación
unidad-de-traducción unidad-de-traducción declaración-externa declaración-externa definición-de-función declaración (DESARROLLO DEL PRINTF)
especificadores-de-declaración declarador lista-de-declaraciones especificador-de-tipo especificadores-de-declaración declarador lista-de-declaraciones INT declarador INT declarador-directo INT declarador-directo (lista-tipos-de-parametros) INT identificador (lista-de-parametros, ...) INT printf (declaración-parametro,...) INT printf (especificadores-de-declaración declarador,...) INT printf (clasificador-de-tipo especificadores-de-declaraciob declarador, ...) INT printf (const especificador-de-tipo declarador,...) INT printf (const char apuntador declarador-directo,..) INT printf (const char * identificador,...) INT printf (const char *,...) definición-de-función (DESARROLLO DEL MAIN) especificadores-de-declaración declarador lista-de-declaraciones especificador-de-tipo especificadores-de-declaración declarador lista-de-declaraciones INT declarador INT declarador-directo INT declarador-directo (lista-tipo-de-parametros){ INT identificador (lista-de-parametros){ INT main (declaración-parámetro){ INT main (especificadores-de-declaración){ INT main (especificador-de-tipo){ INT main (VOID){
unidad-de-traducción declaración-externa declaración especificadores-de-declaración lista-declaradores-init; especificador-de-tipo declarador-init; INT declarador = inicializador; INT declarador-directo = {lista-de-inicializadores}; INT declarador-directo [expresión-constante] = {inicializador}; INT identificador [expresión-condicional] = {expresión-asignación}; INT a[expresión-lógica-OR] = {expresión-condicional}; INT a[expresión-lógica-AND] = {expresión-lógica-OR}; INT a[expresión-OR-exclusivo] = {expresión-lógica-AND}; INT a[expresión-AND] = {expresión-lógica-AND && expresión-OR-inclusivo}; INT a[expresión-de-igualdad] = {expresión-lógica-AND && expresión-lógica-AND && expresión-OR-inclusivo}; INT a[expresión-de-igualdad] = {expresión-OR-inclusivo && expresión-OR-inclusivo && expresión-OR-inclusivo}; INT a[expresión-racional] = {expresión-OR-exclusivo && expresión-OR-exclusivo && expresión-OR-exclusivo}; INT a[expresión-racional] = {expresión-AND && expresión-AND && expresión-AND}; INT a[expresión-racional] = {expresión-de-igualdad && expresión-de-igualdad && expresión-de-igualdad}; INT a[expresión-de-corrimiento] = {expresión-racional && expresión-racional && expresión-racional}; INT a[expresión-aditiva] = {expresión-de-corrimiento && expresión-de-corrimiento && expresión-de-corrimiento}; INT a[expresión-multiplicativa] = {expresión-aditiva && expresión-aditiva && expresión-aditiva}; INT a[expresión-unaria] = {expresión-multiplicativa && expresión-multiplicativa && expresión-multiplicativa}; INT a[expresión-posfija] = {expresión-unaria && expresión-unaria && expresión-posfija}; INT a[expresión-primaria] = {operador-unario expresión-cast && operador-unario expresión-cast && expresión-primaria}; INT a[constante] = {- expresión-cast && ! expresión-cast && constante}; INT a[constante-entera] = {- expresión-cast && ! expresión-cast && constante-entera}; INT a[] = {- expresión-cast && ! expresión-cast && 0}; INT a[] = {- expresión-cast && ! 0.00}; INT a[] = {-!.0};

####Unidad de Traducción sintácticamente correcta

##Análisis Semántico

La UT es lexicamente correcta y no viola ninguna restriccion semantica.

Primeramente el programa declara una funcion llamada printf y luego dentro de la funcion main, inicializa un arreglo de enterors e imprime por pantalla el resultado de 2 expresiones en cuyos operandos estan involucrados el arreglo y la la funcion sizeof.

Es semanticamente correcto.
La salida del programa imprime los caracteres 00.
