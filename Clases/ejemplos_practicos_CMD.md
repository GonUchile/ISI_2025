# Ejemplos Prácticos para Interpretar CMDs

Este archivo presenta ejemplos concretos de cómo interpretar los cambios en un Diagrama Color–Magnitud (CMD) cuando varían diferentes parámetros físicos estelares. Cada sección incluye: explicación física, efecto esperado en el CMD, y ejercicios sugeridos para practicar.

Este documento complementa la [Clase 1](01_poblaciones_estelares.md), el archivo de [Ejemplos CMD](13_examples_cmd.md) y el documento de [Evolución Estelar](evolucion_estelar_CMD.md).

---

## Tabla de Contenidos

1. [Edad (efecto en el MSTO)](#1-edad-efecto-en-el-msto)
2. [Metalicidad (efecto en MS y RGB)](#2-metalicidad-efecto-en-ms-y-rgb)
3. [Abundancia de Helio (Y)](#3-abundancia-de-helio-y)
4. [Binarias no resueltas](#4-binarias-no-resueltas)
5. [Extinción y Reddening](#5-extinción-y-reddening)
6. [Distancia (módulo de distancia)](#6-distancia-módulo-de-distancia)
7. [Resumen de Vectores de Desplazamiento](#7-resumen-de-vectores-de-desplazamiento)
8. [Notas Finales y Consejos de Estudio](#8-notas-finales-y-consejos-de-estudio)
9. [Herramientas y Recursos](#9-herramientas-y-recursos)

---

## 1) Edad (efecto en el MSTO)

### Explicación Física

A medida que una población estelar envejece, las estrellas más masivas agotan su hidrógeno central y abandonan la secuencia principal. El punto donde la secuencia principal se curva hacia la subgigante (**Main Sequence Turn-Off, MSTO**) se desplaza progresivamente a colores más rojos y magnitudes más tenues.

La relación entre edad y masa en el MSTO sigue aproximadamente:

$$t_{\text{MSTO}} \approx 10 \text{ Gyr} \times \left(\frac{M_{\text{MSTO}}}{M_\odot}\right)^{-2.5}$$

### Efecto en el CMD

| Cambio | Dirección del desplazamiento |
|--------|------------------------------|
| Envejecimiento | MSTO → más rojo (derecha) y más débil (abajo) |
| Rejuvenecimiento | MSTO → más azul (izquierda) y más brillante (arriba) |

```
Magnitud
   ↑
   │       Población joven (1 Gyr)
   │           MSTO ←─ más brillante y azul
   │              ↘
   │                \
   │                 \
   │       Población vieja (10 Gyr)
   │           MSTO ←─ más débil y rojo
   │              ↘
   │                \
   +──────────────────────→ Color (B-V)
         azul          rojo
```

### Tabla de Referencia: MSTO vs Edad

| Edad (Gyr) | Masa MSTO (M☉) | M_V (MSTO) | (B-V) MSTO |
|------------|----------------|------------|------------|
| 0.5 | ~2.5 | ~+1.0 | ~0.2 |
| 1.0 | ~2.0 | ~+2.0 | ~0.3 |
| 5.0 | ~1.2 | ~+3.5 | ~0.5 |
| 10.0 | ~1.0 | ~+4.0 | ~0.6 |
| 13.0 | ~0.9 | ~+4.3 | ~0.7 |

*Valores aproximados para [Fe/H] ≈ −1.5*

### Ejercicio Sugerido (Conceptual)

**Ejercicio 1.1:** Compara dos poblaciones con la misma metalicidad ([Fe/H] = −1.0) pero edades de 1 Gyr y 10 Gyr.

<details>
<summary>Ver análisis esperado</summary>

**Análisis:**
- **Población de 1 Gyr:** Tendrá un MSTO más brillante (M_V ~ +2) y más azul ((B-V) ~ 0.3). Estrellas de mayor masa (~2 M☉) aún están en la MS.
- **Población de 10 Gyr:** MSTO más débil (M_V ~ +4) y más rojo ((B-V) ~ 0.6). Solo estrellas de ~1 M☉ permanecen en MS.

La diferencia en brillo del MSTO es de ~2 magnitudes, y en color de ~0.3 mag.

</details>

### Cómo Simular

Usa isócronas de **PARSEC**, **MIST** o **BaSTI**:

```python
# Ejemplo conceptual con Python
# Instalar: pip install isochrones
from isochrones import get_ichrone

# Descargar isócronas MIST
mist = get_ichrone('mist')

# Generar isócronas para diferentes edades
edad_joven = mist.isochrone(age=1e9, feh=-1.0)  # 1 Gyr
edad_vieja = mist.isochrone(age=1e10, feh=-1.0)  # 10 Gyr

# Plotear para comparar
```

---

## 2) Metalicidad (efecto en MS y RGB)

### Explicación Física

Mayor metalicidad introduce más líneas de absorción en los espectros estelares (**line-blanketing**), lo que:

1. Reduce la emisión en UV/azul
2. Cambia la estructura estelar (mayor opacidad)
3. Modifica la temperatura efectiva para una masa dada

El efecto neto es un enrojecimiento de la MS y la RGB.

### Efecto en el CMD

| Cambio | Dirección del desplazamiento |
|--------|------------------------------|
| Aumentar [Fe/H] | MS y RGB → más rojas (derecha) |
| Disminuir [Fe/H] | MS y RGB → más azules (izquierda) |

```
Magnitud
   ↑
   │   RGB baja Z        RGB alta Z
   │       │                 │
   │       ╲                 ╲
   │        ╲                 ╲
   │         ╲                 ╲  ← más roja
   │       ↙  ╲              ↙  ╲
   │      /    ╲            /    ╲
   │     /      ╲          /      ╲
   │    MS       ╲        MS       ╲
   │   (azul)     ╲      (roja)     ╲
   +────────────────────────────────────→ Color
       Z = 0.0001              Z = 0.02
```

### Tabla de Referencia: Color RGB vs Metalicidad

| [Fe/H] | Z | RGB Color (a M_V = 0) | MSTO Color |
|--------|---|----------------------|------------|
| −2.0 | 0.0001 | ~0.8 | ~0.4 |
| −1.0 | 0.001 | ~1.0 | ~0.5 |
| −0.5 | 0.006 | ~1.2 | ~0.6 |
| 0.0 | 0.02 | ~1.4 | ~0.7 |

*Valores aproximados para edad = 10 Gyr*

### Concepto: UV-excess (UVX)

El **UV-excess** es una medida de cuánto más azul es una estrella respecto a una referencia de metalicidad solar. Se utiliza como indicador fotométrico de **baja metalicidad**:

$$\delta(U-B) = (U-B)_{\text{estrella}} - (U-B)_{\text{Hyades}}$$

Estrellas con $\delta(U-B) < 0$ son más azules que las Hyades → candidatas a baja metalicidad.

### Ejercicio Sugerido

**Ejercicio 2.1:** Toma isócronas con edad fija (10 Gyr) y compara Z = 0.0001, Z = 0.001 y Z = 0.02.

<details>
<summary>Ver análisis esperado</summary>

**Análisis:**

1. **Z = 0.0001 ([Fe/H] ≈ −2.0):** RGB muy azul, MS compacta y azul
2. **Z = 0.001 ([Fe/H] ≈ −1.0):** RGB intermedia, separación clara MS-RGB
3. **Z = 0.02 ([Fe/H] ≈ 0.0):** RGB muy roja, MS desplazada a colores rojos

**Observaciones clave:**
- La pendiente de la RGB cambia con Z (más empinada a menor Z)
- La separación entre MSTO y base de RGB aumenta con Z
- El Red Clump se vuelve más rojo a mayor Z

</details>

---

## 3) Abundancia de Helio (Y)

### Explicación Física

Un mayor contenido de helio (Y) tiene varios efectos:

1. Incrementa la **temperatura media molecular** ($\mu$)
2. Modifica la **opacidad** del material estelar
3. Cambia la relación masa-luminosidad

El resultado neto es que la ZAMS se vuelve más brillante y ligeramente más caliente para la misma masa.

### Relación entre μ y Y

$$\mu = \frac{4}{3 + 5X - Z} \approx \frac{4}{3 + 5(1-Y-Z) - Z}$$

donde X, Y, Z son las fracciones de masa de hidrógeno, helio y metales respectivamente.

### Efecto en el CMD

| Cambio | Dirección del desplazamiento |
|--------|------------------------------|
| Aumentar Y | ZAMS → más brillante (arriba) y más azul (izquierda) |
| Disminuir Y | ZAMS → más débil (abajo) y más roja (derecha) |

```
Magnitud
   ↑
   │    Y = 0.30   Y = 0.25
   │       │          │
   │       ╲          ╲
   │        ╲          ╲
   │         ╲          ╲  ← Y alto = más brillante
   │          ╲          ╲
   │           ╲          ╲
   │            ╲          ╲
   +──────────────────────────→ Color
        más azul    más rojo
```

### Tabla de Referencia: Efecto de Y en la ZAMS

| Y | ΔM_V (respecto a Y=0.25) | Δ(B-V) |
|---|--------------------------|--------|
| 0.23 | +0.1 | +0.02 |
| 0.25 | 0.0 (referencia) | 0.0 |
| 0.28 | −0.15 | −0.01 |
| 0.30 | −0.25 | −0.02 |
| 0.35 | −0.45 | −0.04 |

### Ejercicio Sugerido

**Ejercicio 3.1:** Compara dos isócronas con la misma edad (12 Gyr) y metalicidad ([Fe/H] = −1.5) pero con Y = 0.25 y Y = 0.30.

<details>
<summary>Ver análisis esperado</summary>

**Análisis:**

- **Y = 0.25 (estándar):** ZAMS en posición normal para esa metalicidad
- **Y = 0.30 (enriquecida):** ZAMS ~0.25 mag más brillante y ligeramente más azul

**Implicaciones:**
- En cúmulos globulares con múltiples poblaciones, las diferencias en Y producen secuencias principales múltiples
- El efecto es más notable en la MS que en la RGB
- Un error en Y de 0.05 puede traducirse en un error de ~1 Gyr en la edad derivada

</details>

---

## 4) Binarias no resueltas

### Explicación Física

En una población estelar observada, muchos sistemas binarios no pueden resolverse espacialmente. La contribución del flujo del secundario:

1. Eleva el brillo total del sistema
2. Modifica el color según la temperatura del secundario

Para sistemas con masas iguales (q = M₂/M₁ = 1):

$$\Delta m = -2.5 \log_{10}(2) \approx -0.75 \text{ mag}$$

### Efecto en el CMD

| Tipo de binaria | Efecto en magnitud | Efecto en color |
|-----------------|-------------------|-----------------|
| q = 1.0 (iguales) | −0.75 mag (más brillante) | Sin cambio |
| q = 0.5 | ~−0.4 mag | Ligeramente más rojo |
| q < 0.3 | Mínimo | Mínimo |

```
Magnitud
   ↑
   │
   │   * * * * * ← Secuencia de binarias (0.75 mag arriba)
   │  * * * * * *
   │ * * * * * * *
   │* * * * * * * * ← MS de estrellas simples
   │ * * * * * * * *
   │  * * * * * * *
   │   * * * * * *
   +────────────────────→ Color
```

### Distribución de la Secuencia de Binarias

La fracción de binarias crea un **ensanchamiento** de la MS:

- **MS simple:** Secuencia delgada definida por errores fotométricos
- **Con binarias:** Distribución bimodal con "segunda secuencia" paralela
- **Efecto fotométrico:** Puede confundirse con dispersión de edad

### Ejercicio Sugerido

**Ejercicio 4.1:** Simula añadir un 30% de binarios con razones de masa aleatorias (q uniforme entre 0.3 y 1.0) a una población simple.

<details>
<summary>Ver análisis esperado</summary>

**Procedimiento:**

1. Para cada estrella binaria, sortear q ∈ [0.3, 1.0]
2. Calcular luminosidad combinada: $L_{total} = L_1 + L_2 = L_1(1 + q^{3.5})$
3. Calcular magnitud combinada: $m_{bin} = m_1 - 2.5\log_{10}(1 + q^{3.5})$
4. Ajustar color según temperatura promedio ponderada por flujo

**Resultado esperado:**
- MS ensanchada asimétricamente hacia arriba
- Aparición de "cola" brillante
- Dispersión típica de ~0.3-0.4 mag perpendicular a la MS

**Precaución:** Si no se considera la fracción de binarias, se puede subestimar la edad (población parece más joven) o sobreestimar la dispersión de metalicidad.

</details>

---

## 5) Extinción y Reddening

### Explicación Física

El polvo interestelar atenúa la luz estelar de forma selectiva con la longitud de onda, causando:

1. **Extinción (A_λ):** Reducción del brillo en todas las bandas
2. **Enrojecimiento (E(B-V)):** Cambio diferencial de color

### Ley de Extinción

Para la Vía Láctea (ley de Cardelli et al. 1989):

$$A_V = R_V \times E(B-V)$$

donde $R_V \approx 3.1$ para el medio interestelar difuso.

### Ecuaciones de Corrección

**Color observado:**
$$(B-V)_{\text{obs}} = (B-V)_0 + E(B-V)$$

**Magnitud observada:**
$$V_{\text{obs}} = V_0 + A_V = V_0 + 3.1 \times E(B-V)$$

### Efecto en el CMD

| Parámetro | Efecto |
|-----------|--------|
| E(B-V) > 0 | Desplazamiento diagonal: más rojo + más débil |
| A_V > 0 | Desplazamiento vertical: más débil |

```
Magnitud
   ↑
   │
   │                    ★ Posición observada
   │                   ↗   (con extinción)
   │                 ↗
   │    Vector de  ↗
   │   reddening ↗
   │           ↗
   │         ↗
   │       ★ Posición intrínseca
   │         (sin extinción)
   +────────────────────────────→ Color
```

### Vector de Enrojecimiento en Diferentes Filtros

| Sistema | Pendiente del vector | Conversión |
|---------|---------------------|------------|
| B, V | A_V/E(B-V) = 3.1 | E(B-V) = A_V/3.1 |
| V, I | A_V/E(V-I) = 2.4 | E(V-I) = 1.3 E(B-V) |
| g, r (SDSS) | A_r/E(g-r) = 2.3 | E(g-r) = 1.4 E(B-V) |
| G, BP-RP (Gaia) | A_G/E(BP-RP) = 1.9 | E(BP-RP) = 1.3 E(B-V) |

### Ejercicio Sugerido

**Ejercicio 5.1:** Marca en un CMD el vector de enrojecimiento y aplica distintas A_V (0.0, 0.5, 1.0) a una población simple.

<details>
<summary>Ver análisis esperado</summary>

**Para una estrella con (B-V)_0 = 0.6 y V_0 = 4.0:**

| A_V | E(B-V) | (B-V)_obs | V_obs |
|-----|--------|-----------|-------|
| 0.0 | 0.00 | 0.60 | 4.00 |
| 0.5 | 0.16 | 0.76 | 4.50 |
| 1.0 | 0.32 | 0.92 | 5.00 |
| 2.0 | 0.65 | 1.25 | 6.00 |

**Observaciones:**
- El desplazamiento es diagonal en el CMD
- La pendiente del vector es aproximadamente ΔV/Δ(B-V) ≈ 3.1
- La extinción diferencial a lo largo de la línea de visual puede ensanchar las secuencias

</details>

### Mapas de Extinción Útiles

- **Schlegel et al. (1998):** Mapas 2D basados en emisión de polvo en IR lejano
- **Green et al. (2019):** Mapas 3D "Bayestar19" hasta ~5 kpc
- **Planck Collaboration:** Mapas de polvo galáctico de alta resolución

---

## 6) Distancia (módulo de distancia)

### Explicación Física

Alejar una población estelar **no cambia** su color intrínseco, pero todas las magnitudes aparentes se vuelven más débiles por el mismo factor.

### Ecuación del Módulo de Distancia

$$\mu = m - M = 5\log_{10}(d) - 5$$

donde:
- $\mu$ = módulo de distancia (magnitudes)
- $m$ = magnitud aparente
- $M$ = magnitud absoluta
- $d$ = distancia en parsecs

### Relaciones Útiles

| Si la distancia cambia por... | El módulo cambia en... |
|------------------------------|----------------------|
| ×2 | +1.5 mag |
| ×5 | +3.5 mag |
| ×10 | +5.0 mag |

### Efecto en el CMD

| Cambio | Dirección del desplazamiento |
|--------|------------------------------|
| Aumentar distancia | Toda la población → más débil (abajo) |
| Disminuir distancia | Toda la población → más brillante (arriba) |

**Característica clave:** El color NO cambia (desplazamiento puramente vertical).

```
Magnitud aparente
   ↑
   │
   │  ★★★ ← d = 1 kpc (μ = 10)
   │   ↓
   │    ↓  Desplazamiento vertical puro
   │     ↓
   │  ★★★ ← d = 10 kpc (μ = 15)
   │      ↓
   │       ↓
   │        ↓
   │  ★★★ ← d = 100 kpc (μ = 20)
   │
   +────────────────────────────→ Color (sin cambio)
```

### Tabla de Módulos de Distancia

| Distancia | μ (mag) | Ejemplo |
|-----------|---------|---------|
| 10 pc | 0.0 | Definición de M absoluta |
| 100 pc | 5.0 | Vecindario solar |
| 1 kpc | 10.0 | Disco galáctico |
| 8 kpc | 14.5 | Centro galáctico |
| 10 kpc | 15.0 | Cúmulos halo cercanos |
| 50 kpc | 18.5 | LMC/SMC |
| 780 kpc | 24.5 | M31 (Andrómeda) |

### Ejercicio Sugerido

**Ejercicio 6.1:** Mueve una población a diferentes distancias (1 kpc, 10 kpc, 100 kpc) y observa el desplazamiento vertical en el CMD.

<details>
<summary>Ver análisis esperado</summary>

**Para un cúmulo con MSTO en M_V = +4.0:**

| Distancia | μ | m_V (MSTO) |
|-----------|---|------------|
| 1 kpc | 10.0 | 14.0 |
| 10 kpc | 15.0 | 19.0 |
| 100 kpc | 20.0 | 24.0 |

**Implicaciones observacionales:**
- A 1 kpc: MSTO fácilmente observable con telescopios pequeños
- A 10 kpc: Requiere telescopios de 2-4m
- A 100 kpc: Solo accesible con HST o telescopios de 8m+

**Nota:** La pendiente de la MS permanece idéntica; solo cambia la escala de magnitudes aparentes.

</details>

---

## 7) Resumen de Vectores de Desplazamiento

### Diagrama Integrado

```
Magnitud
   ↑
   │
   │  ← Disminuir distancia (vertical arriba)
   │     
   │        ↖ Aumentar Y (arriba-izquierda)
   │         
   │  ★ Posición inicial
   │         
   │        ↘ Aumentar edad (abajo-derecha)
   │     
   │  → Aumentar distancia (vertical abajo)
   │
   │           ↘ Extinción (diagonal abajo-derecha)
   │
   │              → Aumentar [Fe/H] (derecha)
   │
   +────────────────────────────────────────→ Color
```

### Tabla Resumen de Efectos

| Parámetro | Cambio en Color | Cambio en Magnitud | Tipo de desplazamiento |
|-----------|----------------|-------------------|----------------------|
| **Edad ↑** | → (más rojo) | ↓ (más débil) | Diagonal (MSTO) |
| **[Fe/H] ↑** | → (más rojo) | ≈ 0 | Horizontal (MS, RGB) |
| **Y ↑** | ← (más azul) | ↑ (más brillante) | Diagonal inverso |
| **Binarias** | ≈ 0 | ↑ (más brillante) | Vertical/dispersión |
| **A_V ↑** | → (más rojo) | ↓ (más débil) | Diagonal (vector fijo) |
| **Distancia ↑** | 0 | ↓ (más débil) | Vertical puro |

### Degeneraciones Importantes

| Degeneración | Parámetros involucrados | Cómo romperla |
|--------------|------------------------|---------------|
| Edad-Metalicidad | Edad ↔ [Fe/H] | Espectroscopía, forma RGB |
| Distancia-Extinción | d ↔ A_V | Mapas de extinción, RGB tip |
| Edad-Binarias | Edad ↔ f_bin | Análisis de dispersión MS |
| Y-Edad | Y ↔ Edad | Múltiples indicadores |

---

## 8) Notas Finales y Consejos de Estudio

### Recomendaciones Prácticas

1. **Análisis visual:** Cuando analices CMDs reales, haz siempre un diagrama de densidad (contornos o bins) para visualizar poblaciones superpuestas.

2. **Identificación de "huellas":**
   - **MSTO** → indicador primario de edad
   - **RGB color/pendiente** → indicador de metalicidad
   - **HB/RR Lyrae** → poblaciones antiguas (>10 Gyr)
   - **Secuencia binaria** → fracción de binarias
   - **Dispersión MS** → errores + binarias + edad

3. **Correcciones necesarias:**
   - Siempre corregir por extinción antes de interpretar
   - Verificar membresía (movimiento propio, velocidad radial)
   - Considerar contaminación de campo

### Flujo de Trabajo Sugerido

```
1. Obtener fotometría calibrada
         ↓
2. Corregir por extinción (mapas)
         ↓
3. Aplicar módulo de distancia (si conocido)
         ↓
4. Identificar secuencias principales (MS, RGB, HB)
         ↓
5. Localizar MSTO
         ↓
6. Comparar con grid de isócronas
         ↓
7. Estimar edad, metalicidad, fracción binarias
```

---

## 9) Herramientas y Recursos

### Bases de Datos de Isócronas

| Recurso | URL | Características |
|---------|-----|-----------------|
| **PARSEC/COLIBRI** | http://stev.oapd.inaf.it/cgi-bin/cmd | Múltiples sistemas fotométricos |
| **MIST** | http://waps.cfa.harvard.edu/MIST/ | Incluye rotación |
| **BaSTI** | http://basti-iac.oa-teramo.inaf.it/ | Énfasis en poblaciones viejas |
| **DSEP** | Dartmouth Stellar Evolution | Modelos alpha-enhanced |

### Herramientas de Software

```python
# Paquetes Python recomendados
pip install isochrones    # Acceso a isócronas MIST/PARSEC
pip install astropy       # Coordenadas y unidades
pip install dustmaps      # Mapas de extinción
pip install matplotlib    # Visualización
```

### Simuladores Web

- **IAC-STAR:** http://iac-star.iac.es/ — Simulador de CMDs sintéticos con interfaz gráfica
- **CMD 3.7:** http://stev.oapd.inaf.it/cgi-bin/cmd — Generador web de PARSEC

### Mapas de Extinción

- **SFD (1998):** https://irsa.ipac.caltech.edu/applications/DUST/
- **Bayestar19:** https://dustmaps.readthedocs.io/
- **Planck:** https://wiki.cosmos.esa.int/planck-legacy-archive/

---

## Referencias

- Girardi, L. et al. (2002) A&A, 391, 195 — Isócronas PARSEC
- Choi, J. et al. (2016) ApJ, 823, 102 — MIST models
- Pietrinferni, A. et al. (2004) ApJ, 612, 168 — BaSTI database
- Cardelli, J.A. et al. (1989) ApJ, 345, 245 — Ley de extinción
- Schlegel, D.J. et al. (1998) ApJ, 500, 525 — Mapas de polvo

---

*Este documento complementa los materiales del repositorio ISI_2025. Consulta [01_poblaciones_estelares.md](01_poblaciones_estelares.md) para conceptos teóricos, [13_examples_cmd.md](13_examples_cmd.md) para ejercicios adicionales, y [evolucion_estelar_CMD.md](evolucion_estelar_CMD.md) para detalles de evolución estelar.*
