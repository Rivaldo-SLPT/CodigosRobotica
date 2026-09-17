# Laboratorio de Semáforos con Arduino

Este proyecto contiene una serie de prácticas básicas de electrónica y programación con Arduino para simular el funcionamiento de semáforos vehiculares y peatonales.

La intención es aprender de forma gradual:

- encendido y apagado de un LED,
- control de secuencias con temporizadores,
- uso de botones,
- simulación de un cruce peatonal,
- manejo de display LCD para mensajes visuales.

---

## Contenido del repositorio

- `CodigoLed.tex` : práctica inicial con un solo LED que parpadea cada segundo.
- `CodigoSemaforo.tex` : semáforo básico de coches con rojo, amarillo y verde.
- `CodigoSemaforoBoton.tex` : semáforo de coches con botón para solicitar paso peatonal y pantalla LCD.
- `CodigoSemaforoPeatonal.tex` : semáforo vehicular y peatonal con ciclo completo de paso y advertencia.

---

## Objetivos

- Comprender el funcionamiento de salidas digitales en Arduino.
- Programar secuencias temporizadas para señales de tránsito.
- Integrar sensores físicos como botones.
- Manejar señales de alerta para peatones y conductores.
- Practicar la lógica de control en sistemas de automatización simple.

---

## Material recomendado

- Arduino UNO o compatible
- Protoboard
- Cables jumper
- Resistencias adecuadas para LEDs
- 3 LEDs para semáforo de coches (rojo, amarillo, verde)
- 2 LEDs para semáforo peatonal (rojo, verde)
- Botón pulsador
- Display LCD 16x2 (solo en la versión con botón)
- Fuente de alimentación o conexión USB

---

## Esquema de conexión

### Semáforo básico

- Rojo: pin 13
- Amarillo: pin 12
- Verde: pin 11

### Semáforo peatonal

- Rojo peatón: pin 10
- Verde peatón: pin 9

### Botón de paso peatonal

- Botón: pin 2

### LCD (solo en `CodigoSemaforoBoton.tex`)

- RS: pin 7
- E: pin 6
- D4: pin 5
- D5: pin 4
- D6: pin 3
- D7: pin 8

> En la práctica con botón, el LCD se usa para mostrar mensajes como “PUEDE AVANZAR”, “ESPERE…” y “CRUCE AHORA”.

---

## Cómo usar este proyecto

1. Abre la carpeta en tu entorno de trabajo.
2. Copia el contenido del archivo que quieras probar a un sketch de Arduino.
3. Conecta los componentes según el esquema indicado.
4. Compila y sube el código a la placa.
5. Verifica el funcionamiento del semáforo y ajusta tiempos si es necesario.

---

## Descripción de los archivos

### 1. `CodigoLed.tex`

Ejemplo básico de un LED parpadeando cada segundo.

Se usa para aprender:

- `pinMode()`
- `digitalWrite()`
- `delay()`

### 2. `CodigoSemaforo.tex`

Semáforo vehicular con secuencia:

- rojo
- amarillo
- verde

Repite en bucle con tiempos definidos.

### 3. `CodigoSemaforoBoton.tex`

Versión más avanzada que incluye:

- semáforo de coches,
- semáforo de peatones,
- botón para solicitar paso,
- LCD con mensajes informativos.

Cuando se presiona el botón, el semáforo cambia para permitir el paso de peatones.

### 4. `CodigoSemaforoPeatonal.tex`

Semáforo con ciclo completo de tráfico y peatones, donde el paso peatonal se activa después de la fase de amarillo y antes del retorno al verde para coches.

---

## Recomendaciones

- Usa resistencias para los LEDs para protegerlos.
- Verifica bien la conexión del botón con `INPUT_PULLUP`.
- Si el LCD no muestra texto, revisa las conexiones de datos y alimentación.
- Prueba primero la versión simple antes de pasar a la versión con botón y LCD.

---

## Resultado esperado

Al final del laboratorio, se logra que el Arduino controle un sistema que se comporte como un cruce real, con señales claras para coches y peatones.

---

## Licencia

Este proyecto es de uso educativo y puede modificarse libremente para fines de aprendizaje.

---

## Autor

Proyecto desarrollado para laboratorio de robótica y electrónica digital.

