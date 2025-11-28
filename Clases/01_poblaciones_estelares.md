# Clase 1 — Introducción a Poblaciones Estelares

## Resumen

Introducción a conceptos fundamentales de poblaciones estelares y motivos para estudiar la Vía Láctea: descomposición en halo, disco y bulbo, y conexión entre edad, química y cinemática.

## Objetivos de Estudio

- Entender el concepto de Simple Stellar Population (SSP) y su uso en CMDs.
- Relacionar IMF y SFR con la apariencia de un CMD.
- Reconocer las principales regiones del CMD y su significado físico.

---

## Glosario de Siglas y Términos

| Sigla | Nombre Completo | Descripción |
|-------|-----------------|-------------|
| **SSP** | Simple Stellar Population | Población estelar coeval (misma edad) y químicamente homogénea |
| **CMD** | Color–Magnitude Diagram | Diagrama que relaciona el color (temperatura) con la magnitud (brillo) de las estrellas |
| **IMF** | Initial Mass Function | Función que describe la distribución de masas estelares al momento de formación |
| **SFR** | Star Formation Rate | Tasa de formación estelar: masa convertida en estrellas por unidad de tiempo |
| **ZAMS** | Zero Age Main Sequence | Secuencia principal de edad cero; estrellas recién llegadas a la fusión de H |
| **MS** | Main Sequence | Secuencia principal; fase de fusión estable de hidrógeno en el núcleo |
| **MSTO** | Main Sequence Turn-Off | Punto de giro de la secuencia principal; indica la edad del sistema |
| **SGB** | Sub-Giant Branch | Rama de subgigantes; transición post-MS hacia la RGB |
| **RGB** | Red Giant Branch | Rama de gigantes rojas; fusión de H en capa, núcleo de He inerte |
| **HB** | Horizontal Branch | Rama horizontal; fusión de He en el núcleo |
| **RC** | Red Clump | Región compacta de estrellas en la HB rica en metales |
| **AGB** | Asymptotic Giant Branch | Rama asintótica de gigantes; etapa avanzada con doble capa de fusión |
| **WD** | White Dwarf | Enana blanca; remanente estelar compacto de estrellas de masa baja/intermedia |
| **BS** | Blue Straggler | Rezagadas azules; estrellas aparentemente más jóvenes que el sistema |

---

## Conceptos Clave

### 1. Simple Stellar Population (SSP)

Una **SSP** es una población estelar idealizada donde todas las estrellas:
- Nacieron al **mismo tiempo** (coevales)
- Tienen la **misma composición química** inicial
- Están a la **misma distancia** del observador

**Ejemplos naturales:** Cúmulos globulares y cúmulos abiertos son las mejores aproximaciones a SSPs.

**Importancia teórica:**
- Permiten calibrar **isócronas** (curvas teóricas de igual edad en el CMD)
- Son la base para modelar poblaciones compuestas
- Facilitan la determinación de edades y metalicidades

### 2. Color–Magnitude Diagram (CMD)

El CMD es la herramienta observacional fundamental para estudiar poblaciones estelares.

**Ejes del diagrama:**
- **Eje Y (vertical):** Magnitud aparente o absoluta (más brillante hacia arriba)
- **Eje X (horizontal):** Índice de color (e.g., B-V, V-I, G-R)

**Interpretación física:**
- El **color** es un proxy de la **temperatura efectiva** (azul = caliente, rojo = frío)
- La **magnitud** indica el **brillo intrínseco** (cuando se corrige por distancia)

### 3. Initial Mass Function (IMF)

La IMF describe cómo se distribuyen las masas de las estrellas al formarse:

$$\xi(M) = \frac{dN}{dM}$$

Donde:
- $\xi(M)$ = número de estrellas por intervalo de masa
- $dN$ = número de estrellas en el intervalo $[M, M+dM]$

**Leyes de IMF más utilizadas:**

| IMF | Expresión | Rango de Validez |
|-----|-----------|------------------|
| **Salpeter (1955)** | $\xi(M) \propto M^{-2.35}$ | $M > 0.5\, M_\odot$ |
| **Kroupa (2001)** | Múltiples pendientes según masa | $0.01 - 100\, M_\odot$ |
| **Chabrier (2003)** | Log-normal + power law | $0.01 - 100\, M_\odot$ |

**IMF de Kroupa (forma segmentada):**
- $\xi(M) \propto M^{-0.3}$ para $0.01 \leq M/M_\odot < 0.08$
- $\xi(M) \propto M^{-1.3}$ para $0.08 \leq M/M_\odot < 0.5$
- $\xi(M) \propto M^{-2.3}$ para $M/M_\odot \geq 0.5$

### 4. Star Formation Rate (SFR)

La SFR cuantifica la intensidad de formación estelar:

$$\psi(t) = \frac{dM_\star}{dt}$$

Donde:
- $\psi(t)$ = tasa de formación estelar [M☉/yr]
- $dM_\star$ = masa convertida en estrellas en el intervalo $dt$

**Tipos de historia de formación estelar:**
- **Burst instantáneo:** Toda la población se forma simultáneamente
- **Constante:** SFR uniforme en el tiempo
- **Exponencial decreciente:** $\psi(t) \propto e^{-t/\tau}$
- **Retardada:** $\psi(t) \propto t \cdot e^{-t/\tau}$

---

## Interpretación del CMD

### Efectos de la Edad

| Característica | Población Joven | Población Vieja |
|----------------|-----------------|-----------------|
| MSTO | Azul y brillante | Rojo y débil |
| Presencia de estrellas masivas | Sí | No |
| RGB | Poco poblada | Prominente |
| AGB | Posible AGB luminosa | AGB menos luminosa |

### Efectos de la Metalicidad

- **Mayor [Fe/H]:** Desplaza MS y RGB hacia colores más rojos
- **Menor [Fe/H]:** MS y RGB más azules, RGB más empinada

**Degeneración edad-metalicidad:** Una población vieja y pobre en metales puede parecerse a una joven y rica en metales.

### Efectos de Binarias

Las estrellas binarias no resueltas crean:
- Una secuencia paralela hasta **~0.75 mag más brillante** que la MS individual
- Ensanchamiento aparente de la MS

### Efectos de Extinción y Distancia

| Efecto | Descripción | Fórmula |
|--------|-------------|---------|
| **Enrojecimiento** | Extinción selectiva por polvo; E(B-V) | $A_V \approx 3.1 \times E(B-V)$ |
| **Módulo de distancia** | Diferencia entre magnitud aparente y absoluta | $(m-M) = 5\log_{10}(d) - 5$ |

---

## Regiones del CMD (Descripción Detallada)

### ZAMS (Zero Age Main Sequence)
Línea que marca el inicio de la fusión de hidrógeno en el núcleo. Representa el límite inferior (más débil y azul) de la MS para cada masa.

### MS (Main Sequence)
Banda diagonal donde las estrellas pasan ~90% de su vida fusionando H→He en el núcleo. Las estrellas más masivas están arriba a la izquierda (brillantes y calientes).

### MSTO (Main Sequence Turn-Off)
El punto donde las estrellas más masivas aún en MS agotan su hidrógeno central. **Indicador primario de edad** de una SSP.

### SGB (Sub-Giant Branch)
Fase corta entre el MSTO y la RGB. El núcleo se contrae mientras la envoltura comienza a expandirse.

### RGB (Red Giant Branch)
Ascenso hacia mayores luminosidades y colores rojos. Fusión de H en capa alrededor de un núcleo de He degenerado.

### HB (Horizontal Branch) / Red Clump
- **HB:** Distribución horizontal de estrellas fusionando He en el núcleo (poblaciones pobres en metales)
- **RC:** Agrupación compacta equivalente en poblaciones ricas en metales

### AGB (Asymptotic Giant Branch)
Segunda fase de gigante después del agotamiento del He central. Doble capa de fusión (He y H). Estrellas variables de largo período.

### WD Cooling Sequence
Secuencia de enfriamiento de enanas blancas. Diagonal hacia magnitudes más débiles y colores más rojos con el tiempo.

### Instability Strip
Región vertical del CMD donde ocurren pulsaciones estelares:
- **Cefeidas clásicas** (estrellas masivas)
- **RR Lyrae** (HB, pobres en metales)
- **δ Scuti** (MS superior)

### Blue Stragglers
Estrellas que aparecen más azules y brillantes que el MSTO. Origen probable: fusión de binarias o transferencia de masa.

---

## Fórmulas Útiles

### Relaciones de Magnitud

**Ecuación de Pogson:**
$$\Delta m = m_1 - m_2 = -2.5\log_{10}\left(\frac{f_1}{f_2}\right)$$

**Magnitud aparente vs. absoluta:**
$$m - M = 5\log_{10}(d) - 5$$

Donde $d$ está en parsecs.

### Relaciones de Flujo y Luminosidad

**Flujo a partir de luminosidad:**
$$f = \frac{L}{4\pi d^2}$$

**Ley de Stefan-Boltzmann:**
$$L = 4\pi R^2 \sigma T_\mathrm{eff}^4$$

Donde $\sigma = 5.67 \times 10^{-8}\, \mathrm{W\,m^{-2}\,K^{-4}}$

### Magnitud Bolométrica

$$M_\mathrm{bol} = M_{\mathrm{bol},\odot} - 2.5\log_{10}\left(\frac{L}{L_\odot}\right)$$

**Constantes IAU:**
- $M_{\mathrm{bol},\odot} = 4.74$ mag
- $L_\odot = 3.828 \times 10^{26}$ W

### Conversión SFR a Número de Estrellas

Para convertir masa formada ($M_\mathrm{tot}$) a número de estrellas:

$$N_\star = M_\mathrm{tot} \times \frac{\int_{M_\mathrm{min}}^{M_\mathrm{max}} \xi(M)\, dM}{\int_{M_\mathrm{min}}^{M_\mathrm{max}} M \cdot \xi(M)\, dM}$$

---

## Componentes de la Vía Láctea

| Componente | Edad Típica | Metalicidad [Fe/H] | Cinemática |
|------------|-------------|---------------------|------------|
| **Disco delgado** | 0–8 Gyr | −0.5 a +0.3 | Rotación ordenada, σ ~ 20 km/s |
| **Disco grueso** | 8–12 Gyr | −1.0 a −0.3 | Rotación + dispersión mayor |
| **Bulbo** | 8–13 Gyr | −1.5 a +0.5 | Dispersión alta, rotación lenta |
| **Halo** | 10–13 Gyr | −3.0 a −1.0 | Sin rotación neta, σ ~ 150 km/s |

---

## Notas Prácticas

1. **Para determinar edad de una SSP:** Ubicar el MSTO y comparar con isócronas teóricas.

2. **Para estimar metalicidad:** Observar el color de la RGB y comparar con modelos.

3. **Para corregir extinción:** Usar mapas de polvo (e.g., Schlegel, SFD, Planck) y leyes de extinción.

4. **IMFs comunes en la literatura:**
   - Salpeter: Uso histórico, sobreestima estrellas de baja masa
   - Kroupa: Más realista para todo el rango de masas
   - Chabrier: Popular en estudios extragalácticos

---

## Referencias Sugeridas

- Salpeter, E.E. (1955) ApJ, 121, 161 — IMF original
- Kroupa, P. (2001) MNRAS, 322, 231 — IMF segmentada
- Chabrier, G. (2003) PASP, 115, 763 — IMF log-normal
- Girardi, L. et al. (PARSEC isochrones)
- Marigo, P. et al. (2017) — PARSEC + COLIBRI tracks

---

*Consulta [13_examples_cmd.md](13_examples_cmd.md) para ejercicios y simulaciones prácticas.*
