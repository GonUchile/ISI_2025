# Ejemplos y Ejercicios: Diagramas Color-Magnitud (CMD)

Este documento complementa la [Clase 1](01_poblaciones_estelares.md) con ejercicios prácticos y ejemplos de interpretación de CMDs.

---

## Ejemplo 1: Identificación de Regiones en un CMD Típico

### Diagrama Esquemático

```
        Magnitud
           ↑
           |      *  (AGB)
     Más   |    * *
   brillante    * *  (RGB tip)
           |   *  *
           |  *   *
           |  *  *   ← RGB
           | *  *
           |*  *     
           * **      ← Red Clump / HB
           |\ * 
           | \*      ← SGB
           |  *\
           |  * \    ← MSTO
           | *   \
           |*     \
           |*      \  ← MS
           |*       \
           |*        \
           |*         \
           +-----------→ Color (B-V)
         azul        rojo
```

### Ejercicio 1.1
**Pregunta:** En el diagrama anterior, ¿qué región usarías para estimar la edad de un cúmulo globular?

<details>
<summary>Ver respuesta</summary>

**Respuesta:** El **MSTO (Main Sequence Turn-Off)** es el mejor indicador de edad. La magnitud del MSTO se relaciona directamente con la masa de las estrellas que están abandonando la secuencia principal, lo cual depende del tiempo transcurrido desde la formación del cúmulo.

</details>

---

## Ejemplo 2: Efecto de la Edad en el CMD

### Comparación de SSPs de Diferentes Edades

| Edad | MSTO (M_V) | MSTO Color (B-V) | RGB Tip (M_V) |
|------|-----------|------------------|---------------|
| 1 Gyr | ~+2.0 | ~0.3 | ~−2.5 |
| 5 Gyr | ~+3.5 | ~0.5 | ~−2.8 |
| 10 Gyr | ~+4.0 | ~0.6 | ~−3.0 |
| 13 Gyr | ~+4.3 | ~0.7 | ~−3.0 |

*Valores aproximados para [Fe/H] = −1.5*

### Ejercicio 2.1
**Pregunta:** ¿Por qué el MSTO se desplaza hacia magnitudes más débiles (números más positivos) con la edad?

<details>
<summary>Ver respuesta</summary>

**Respuesta:** A medida que envejece la población, las estrellas más masivas ya han evolucionado fuera de la MS. Solo quedan estrellas de menor masa en la MS, las cuales son intrínsecamente menos luminosas. Por lo tanto, el punto de giro (MSTO) se ubica a magnitudes más débiles.

**Relación masa-luminosidad:** $L \propto M^{3.5}$ (aproximadamente)

Para estrellas de 1 M☉, el tiempo en MS es ~10 Gyr.
Para estrellas de 2 M☉, el tiempo en MS es ~1 Gyr.

</details>

---

## Ejemplo 3: Efecto de la Metalicidad

### Comparación a Edad Fija (10 Gyr)

| [Fe/H] | MSTO Color | RGB Color (a M_V = 0) |
|--------|------------|----------------------|
| −2.0 | ~0.4 | ~0.8 |
| −1.0 | ~0.5 | ~1.0 |
| −0.5 | ~0.6 | ~1.2 |
| 0.0 | ~0.7 | ~1.4 |

### Ejercicio 3.1
**Pregunta:** Un observador encuentra dos cúmulos con MSTO en colores (B-V) = 0.5 y (B-V) = 0.7. Sin información adicional, ¿puede determinar cuál es más viejo?

<details>
<summary>Ver respuesta</summary>

**Respuesta:** **No directamente**, debido a la **degeneración edad-metalicidad**. 

- El cúmulo con MSTO azul (0.5) podría ser:
  - Joven y rico en metales, O
  - Viejo y pobre en metales

- El cúmulo con MSTO rojo (0.7) podría ser:
  - Viejo y rico en metales, O
  - Aún más viejo y de metalicidad intermedia

Se necesita información adicional (espectroscopía, forma de la RGB, posición del RC) para romper la degeneración.

</details>

---

## Ejemplo 4: Identificación de Binarias

### Secuencia de Binarias en el CMD

Las binarias no resueltas aparecen más brillantes que estrellas individuales del mismo color:

```
Magnitud
   |
   |    * * * ← Secuencia de binarias
   |   * * * *
   |  * * * * *
   | * * * * * * ← MS individual
   |* * * * * * *
   |* * * * * * * *
   +----------------→ Color
```

### Cálculo del Offset

Para dos estrellas idénticas combinadas:
$$\Delta m = -2.5 \log_{10}(2) \approx -0.75 \text{ mag}$$

### Ejercicio 4.1
**Pregunta:** Si una estrella de MS tiene m_V = 18.0, ¿cuál sería la magnitud de un sistema binario de dos estrellas idénticas?

<details>
<summary>Ver respuesta</summary>

**Respuesta:** 
$$m_\mathrm{binaria} = m_\mathrm{individual} - 2.5\log_{10}(2)$$
$$m_\mathrm{binaria} = 18.0 - 0.75 = 17.25 \text{ mag}$$

El sistema binario aparece **0.75 magnitudes más brillante**.

</details>

---

## Ejemplo 5: Corrección por Distancia y Extinción

### Datos de Observación

Un cúmulo presenta:
- Magnitud aparente del MSTO: $m_V = 18.5$
- Color observado del MSTO: $(B-V)_\mathrm{obs} = 0.8$
- Enrojecimiento: $E(B-V) = 0.2$

### Ejercicio 5.1
**Pregunta:** Calcula el color intrínseco del MSTO y la magnitud absoluta si la distancia es d = 10 kpc.

<details>
<summary>Ver respuesta</summary>

**Respuesta:**

1. **Color intrínseco:**
$$(B-V)_0 = (B-V)_\mathrm{obs} - E(B-V) = 0.8 - 0.2 = 0.6$$

2. **Extinción en V:**
$$A_V = 3.1 \times E(B-V) = 3.1 \times 0.2 = 0.62 \text{ mag}$$

3. **Magnitud aparente corregida:**
$$m_{V,0} = m_V - A_V = 18.5 - 0.62 = 17.88 \text{ mag}$$

4. **Módulo de distancia:**
$$(m-M) = 5\log_{10}(d/\mathrm{pc}) - 5 = 5\log_{10}(10000) - 5 = 15.0$$

5. **Magnitud absoluta:**
$$M_V = m_{V,0} - (m-M) = 17.88 - 15.0 = 2.88 \text{ mag}$$

</details>

---

## Ejemplo 6: Estimación de Número de Estrellas con la IMF

### Problema

Se forma un cúmulo con masa total $M_\mathrm{tot} = 10^4\, M_\odot$. Usando la IMF de Salpeter ($\xi(M) \propto M^{-2.35}$) entre 0.1 y 100 M☉, estima:

a) El número total de estrellas
b) El número de estrellas con M > 8 M☉ (supernovas potenciales)

### Ejercicio 6.1

<details>
<summary>Ver solución paso a paso</summary>

**Solución:**

La IMF de Salpeter: $\xi(M) = A \cdot M^{-2.35}$

1. **Normalización por masa total:**
$$M_\mathrm{tot} = \int_{0.1}^{100} M \cdot \xi(M) \, dM = A \int_{0.1}^{100} M^{-1.35} \, dM$$

$$M_\mathrm{tot} = A \left[\frac{M^{-0.35}}{-0.35}\right]_{0.1}^{100} = A \times 7.92$$

Para $M_\mathrm{tot} = 10^4\, M_\odot$: $A = 1263$

2. **Número total de estrellas:**
$$N = \int_{0.1}^{100} \xi(M) \, dM = A \int_{0.1}^{100} M^{-2.35} \, dM$$

$$N = A \left[\frac{M^{-1.35}}{-1.35}\right]_{0.1}^{100} = A \times 16.5 \approx 20,800 \text{ estrellas}$$

3. **Estrellas masivas (M > 8 M☉):**
$$N_{>8} = A \int_{8}^{100} M^{-2.35} \, dM \approx A \times 0.052 \approx 66 \text{ estrellas}$$

**Conclusión:** Solo ~0.3% de las estrellas tienen masa suficiente para explotar como supernova.

</details>

---

## Ejemplo 7: Uso de Isócronas

### Procedimiento para Ajustar Isócronas

1. **Obtener fotometría** del cúmulo en al menos dos bandas (ej.: V y I)
2. **Corregir por enrojecimiento** usando mapas de extinción
3. **Ajustar distancia** (módulo de distancia como parámetro libre)
4. **Seleccionar metalicidad** (si se conoce por espectroscopía)
5. **Comparar con grid de isócronas** de diferentes edades
6. **Minimizar residuos** entre datos y modelo

### Ejercicio 7.1
**Pregunta:** ¿Por qué es importante tener espectroscopía además de fotometría para determinar la edad de un cúmulo?

<details>
<summary>Ver respuesta</summary>

**Respuesta:** 

La espectroscopía proporciona:

1. **Metalicidad directa** ([Fe/H]) → rompe la degeneración edad-metalicidad
2. **Velocidades radiales** → confirma membresía al cúmulo
3. **Abundancias individuales** ([α/Fe], etc.) → información sobre origen químico
4. **Temperaturas efectivas** independientes del enrojecimiento

Sin espectroscopía, tanto la metalicidad como la edad quedan como parámetros libres correlacionados, lo que aumenta la incertidumbre.

</details>

---

## Ejemplo 8: Blue Stragglers

### Características Observacionales

Las Blue Stragglers (BS) aparecen:
- Más **azules** que el MSTO
- Más **brillantes** que el MSTO
- En una extensión de la MS hacia arriba

### Mecanismos de Formación

| Mecanismo | Descripción | Evidencia |
|-----------|-------------|-----------|
| **Coalescencia** | Fusión de dos estrellas en binaria cercana | Pulsaciones, rotación rápida |
| **Transferencia de masa** | Acreción desde compañera evolucionada | Compañera WD detectada |
| **Colisiones** | Encuentros en regiones densas | Más frecuentes en núcleo de cúmulos |

### Ejercicio 8.1
**Pregunta:** En un cúmulo globular antiguo (12 Gyr), encuentras una estrella en la MS con masa estimada de 1.3 M☉. ¿Es consistente con la edad del cúmulo?

<details>
<summary>Ver respuesta</summary>

**Respuesta:** **No**, no es consistente.

Una estrella de 1.3 M☉ tiene un tiempo de vida en la MS de aproximadamente:
$$t_\mathrm{MS} \approx 10 \text{ Gyr} \times \left(\frac{M}{M_\odot}\right)^{-2.5} \approx 10 \times 1.3^{-2.5} \approx 5.2 \text{ Gyr}$$

Si el cúmulo tiene 12 Gyr, las estrellas de 1.3 M☉ deberían haber abandonado la MS hace ~7 Gyr.

Esta estrella es probablemente una **Blue Straggler**, formada por fusión de binarias o transferencia de masa, lo que le permitió "rejuvenecer" y aparecer como una estrella más masiva.

</details>

---

## Simulaciones Prácticas

### Recursos para Generar CMDs Sintéticos

1. **PARSEC/COLIBRI** (http://stev.oapd.inaf.it/cgi-bin/cmd)
   - Isócronas y poblaciones sintéticas
   - Múltiples sistemas fotométricos

2. **MIST** (http://waps.cfa.harvard.edu/MIST/)
   - Modelos estelares modernos
   - Incluye rotación

3. **BaSTI** (http://basti-iac.oa-teramo.inaf.it/)
   - Énfasis en poblaciones viejas
   - Buenos para cúmulos globulares

4. **IAC-STAR** (http://iac-star.iac.es/)
   - Simulador de CMDs sintéticos
   - Interfaz gráfica intuitiva

### Ejercicio de Simulación

**Tarea:** Usa el servidor de PARSEC para generar:
1. Una isócrona de 10 Gyr con [Fe/H] = −1.0
2. Una isócrona de 1 Gyr con [Fe/H] = 0.0

Compara las posiciones del MSTO y la extensión de la RGB.

---

## Resumen de Diagnósticos del CMD

| Característica | Diagnóstico |
|----------------|-------------|
| **Posición MSTO** | Edad de la población |
| **Color RGB** | Metalicidad |
| **Pendiente RGB** | Metalicidad (más empinada = menor [Fe/H]) |
| **Extensión HB** | Edad + pérdida de masa |
| **Ancho MS** | Binarias + errores fotométricos |
| **Blue Stragglers** | Dinámica + historia de binarias |
| **RC luminosidad** | Distancia (candela estándar) |
| **WD cooling sequence** | Edad del sistema (método independiente) |

---

## Referencias para Ejercicios Adicionales

- Harris, W.E. (1996) AJ, 112, 1487 — Catálogo de cúmulos globulares galácticos
- Piotto, G. et al. (2002) A&A, 391, 945 — CMDs de cúmulos globulares HST
- De Angeli, F. et al. (2005) AJ, 130, 116 — Edades relativas de cúmulos globulares
- VandenBerg, D.A. et al. (2013) ApJ, 775, 134 — Isócronas Victoria-Regina

---

*Regresa a [Clase 1](01_poblaciones_estelares.md) para revisar los conceptos teóricos.*
