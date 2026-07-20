Fase 0: Base de datos del proyecto ()

1. Debemos documentar todo lo que hagamos para tener un seguimiento real de todas 
las pruebas que hagamos {Objetivo, Esquema, Resultados (fotos del osciloscopio), 
Problemas encontrados y Solución aplicada)}

2. Los repositorios de GitHub

3. Carpeta de Proyectos:  
/Simulaciones (MATLAB/Simulink), 
/Hardware (esquemas Eagle/KiCad/EasyEda) 
/Software (código fuente) 
/Documentacion (datasheets)

Fase 1: Planificación y Diseño Teórico.

- Objetivo: Clarísimamente es ver que el diseño sea viable antes de comprar nada.

1. Definición de Especificaciones:

- Potencia de salida (Pout) : 30W
- Frecuencia de Trabajo (fs) : 100Khz
- Eficiencia esperada (nu) : >= 80% 

2. Simulación Completa: 

- Modelar el puente inversor (Full-Bridge) y las bobinas en simulink (Simscape)
- Calcular el coeficiente de acoplamiento (Variará en función de la distancia).

3. Lista BOM:

Una vez hecha la simulación podemos hacer una lista de materiales para ir probando
y comparando la simulación con la realidad.
