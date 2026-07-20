Este proyecto se podría relacionar con la rama de Electrónica de Potencia. Consiste 
en hacer que el dron se acople milimetricamente a la estación de carga, por lo que
necesitaremos un sistema que "atraiga" al dron hacia este punto.

Podemos dividir el proyecto en 3 grupos:

- Electrónica de Potencia: Diseñar un sistema de carga inductiva resonante. Simplemente
calcularlas bobinas emisoras y receptoras para maximizar la transferencia de potencia 
sin contacto físico directo.

- Automatización: Diseñar un sistema de guiado (luces infrarrojas o balizas magnéticas)
que el dron pueda seguir para posicionarse sobre la base.

- Gestión de Energía: Implementar un cargador inteligente con un algoritmo de MPPT 
(Maximum Power Point Tracking) para que el proceso de carga sea eficiente y seguro 
para la batería (LiPo o Li-Ion).

¿Cómo podemos empezar los pibes?

1. Fase de simulación.

Para empezar con el sistema de Docking Station con carga inductiva dividiremos el proyecto
en tres frentes: el sistema de guiado (para que el dron llegue al punto exacto), el sistema 
de transferencia de energía (el corazón electrónico) y la gestión de batería.

1.1. Antes de hacer una BOM deberemos de modelar la transferencia inductiva. Para ello utilizaremos
SIMULINK, simularemos las bobinas (Lo suyo es que la bobina primaria esté en la base, y la 
secundaria en el dron) como un transoformador de acoplamiento "débil".

1.2 Un análisis donde definamos la frecuencia de conmutación. Para cargas inductivas normalmente 
oscila entre los 80 kHz y 200 kHz.

1.3 Una cosa que se me ocurre es ver como varía la eficiencia al aumentar la distancia entre las 
bobinas, ya que esto nos fdará los requisitos reales de alineación.

2. Diseño del "Front-End" de Potencia

2.1 Etapa Emisora (Base): Necesitamos un Inversor de Puente Completo (Full-Bridge) o Medio Puente 
que convierta la DC de entrada en una señal AC de alta frecuencia para alimentar la bobina primaria.

2.2 Etapa Receptora (Dron): Necesitamos un circuito rectificador síncrono (diodos Schottky o MOSFETs 
para menor caída de tensión) seguido de un filtro paso bajo para obtener una DC limpia que alimente 
el cargador de la batería.

2.3 Control de lazo cerrado: Diseña un sistema donde el receptor envíe (por un canal secundario, 
como Bluetooth Low Energy o infrarrojos) el estado de carga al emisor para ajustar la potencia 
mediante PWM.

3. Sistema de Guiado (Aquí es donde el dron pasa de "volar cerca" a "aterrizar sobre la base")

3.1 Método sencillo pero robusto: Usar balizas IR (Infrarrojas). Colocar 3 o 4 LEDs infrarrojos 
en la base formando un patrón geométrico específico.

3.2 Detección: El dron, con una cámara sencilla y un filtro IR, puede detectar el centro 
geométrico de ese patrón.

3.3 Control: Implementar un bucle de control de posición en el dron (a través del controlador 
de vuelo, tipo Pixhawk o similar) que se active a menos de 50 cm de altura para "centrarse" 
sobre la base.


COSAS A TENER EN CUENTA. 
- El mayor problema es la alineación mecánica. Si el dron no aterriza exactamente encima, 
la eficiencia cae al 10-20% y las bobinas se calientan peligrosamente.
Diseñar una geometría de "embudo" o "guía mecánica" en la base. Si el dron aterriza con un error 
de 2-3 cm, la estructura debe obligarlo a deslizarse hasta la posición de acoplamiento perfecto.








