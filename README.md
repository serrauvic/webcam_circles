# webcam_circleis
Circle detection from online webcam images

# The Hough Transform

La Transformada de Hough va ser inventada inicialment per a l'anàlisi de la Càmera de bombolles(Hough, 1959).

La Transformada de Hough és una tècnica popular per detectar qualsevol forma, si es pot representar aquesta forma en forma matemàtica. Pot detectar la forma fins i tot si es trenca o es destrueix una mica.

Es basa en transformar punts de la imatge en un espai de paràmetres amb la idea bàsica de trobar corbes que puguin ser parametritzades com a rectes, polinomis i circumferències.

En principi, està pensada per a la detecció de rectes, però també és aplicable a qualsevol funció de la forma f(v,c) =0. On v és un vector de coordenades i c és un vector de coeficients.

En aquesta aplicació s’implementa la transformada de Hough espcialitzada en la detecció de cercles. La idea es detectar cercles en imatges imperfectes, contant el número dels cercles candidats dins l’espai «hough» i posteriorment seleccionant el valor màxim en la matriu d’acumulació.

Donat el fet que podem jugar amb la mida del radi dels cercles que volem detectar, podem reduir l’espai de paràmetres (a,b,r) en el que volem buscar els cercles. 

Podem definir un cercle en 2D com:

 (x – a)² + (y - b)² = r²

On a,b son el centre del cerlce,  Per cada punt x,y de la circumferència es pot definir una circumferència centrada en x,y amb un determinar radi conegut.

Es fa servir una matriu d’acumulació dividint en una grid l’espai de paràmetres per puntuar o sumar el número de vegades que un cercle passa per cada cel·la. De manera que es pugi determinar per quina cel·la hi ha més cercles que interseccionen,  de maner que aquesta cel·la serà la candidata per als centres dels cercles en la imatge original. 

Com a particularitat s’ha afegit el text en la imatge de les coordenades x i y del centre del cercle detectat.

En aquesta aplicació jugant amb els diferents paràmetres de la implementació de l’algoritme, com per exemple el paràmetre MIN_CIRCLE_DIST, que permet definir una distància menor entre els cercles detectats dins de l’espai hough, com menor sigui aquest valor més cercles es detectaran. 

Jugant amb el paràmetre MIN_RADIUS es possible detectar cercles més allunyats de la càmera.

Referencies:

https://ca.wikipedia.org/wiki/Transformada_de_Hough

http://tomaszkacmajor.pl/index.php/2017/06/05/hough-lines-transform-explained/

https://docs.opencv.org/3.0-beta/doc/py_tutorials/py_imgproc/py_houghlines/py_houghlines.html

https://docs.opencv.org/2.4/doc/tutorials/imgproc/imgtrans/hough_circle/hough_circle.html
