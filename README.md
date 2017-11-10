# webcam_circleis
Circle detection from online webcam images

# The Hough Transform

La Transformada de Hough va ser inventada inicialment per a l'anàlisi de la Càmera de bombolles(Hough, 1959).

La Transformada de Hough és una tècnica popular per detectar qualsevol forma, si es pot representar aquesta forma en forma matemàtica. Pot detectar la forma fins i tot si es trenca o es destrueix una mica.

Es basa en transformar punts de la imatge en un espai de paràmetres amb la idea bàsica de trobar corbes que puguin ser parametritzades com a rectes, polinomis i circumferències.

En principi, està pensada per a la detecció de rectes, però també és aplicable a qualsevol funció de la forma f(v,c) =0. On v és un vector de coordenades i c és un vector de coeficients.

En aquesta aplicació s’implementa la transformada de Hough espcialitzada en la detecció de cercles. La idea es detectar cercles en imatges imperfectes, contant el número dels cercles candidats dins l’espai «hough» i posteriorment seleccionant el valor màxim en la matriu d’acumulació. 

Com a particularitat s’ha afegit el text en la imatge de les coordenades x i y del centre del cercle detectat.

Referencies:

https://ca.wikipedia.org/wiki/Transformada_de_Hough

http://tomaszkacmajor.pl/index.php/2017/06/05/hough-lines-transform-explained/

https://docs.opencv.org/3.0-beta/doc/py_tutorials/py_imgproc/py_houghlines/py_houghlines.html

https://docs.opencv.org/2.4/doc/tutorials/imgproc/imgtrans/hough_circle/hough_circle.html
