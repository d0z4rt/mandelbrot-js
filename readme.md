# MANDELBROT

## Javascript mandlebrot generator

http://xahlee.info/cmaci/fractal/mandelbrot.html

nb complexe : C {réel,imaginaire}

## verifie si un point appartient a l'ensemble mandelbrot

Pour un point {x,y} :

```
DECLARER x, xTemp, y numerique
DECLARER i, iMax numerique
DEBUT

    ECRIRE "nombre d'iterations ? "
    LIRE iMax
    ECRIRE "Réel ? "
    LIRE x
    ECRIRE "Imaginaire ? "
    LIRE y

    POUR i de 0 à iMax PAS de 1
        xTemp ← x
        x ← x * x - y * y + x
        y ← 2 * xTemp * y + y
    FINPOUR

    SI x * y < 6 ALORS
        ECRIRE "Le point est dans l'ensemble de Mandelbrot"
    SINON
        ECRIRE "Le point n'est pas dans l'ensemble de Mandelbrot"
    FINSI
FIN
```
