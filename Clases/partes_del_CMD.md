# Partes del Diagrama Color-Magnitud (CMD) — Guía Ampliada

Este documento reúne definiciones detalladas y pistas observacionales para identificar las regiones más importantes de un Diagrama Color-Magnitud (CMD). Úsalo como referencia y enlázalo desde los apuntes de cada clase.

---

## Tabla de Contenidos

1. [Introducción](#introducción)
2. [Regiones del CMD y su Significado Físico](#regiones-del-cmd-y-su-significado-físico)
3. [Efectos Observacionales que Alteran el CMD](#efectos-observacionales-que-alteran-el-cmd)
4. [Funciones de la Población: IMF y SFR](#funciones-de-la-población-imf-y-sfr)
5. [Cómo Usar esta Guía](#cómo-usar-esta-guía)
6. [Diagrama Esquemático del CMD](#diagrama-esquemático-del-cmd)
7. [Resumen de Diagnósticos](#resumen-de-diagnósticos)
8. [Referencias](#referencias)

---

## Introducción

El Diagrama Color-Magnitud (CMD) es la herramienta observacional más potente para estudiar poblaciones estelares. En él se representa:

- **Eje Y (vertical):** Magnitud (más brillante hacia arriba, valores numéricos menores)
- **Eje X (horizontal):** Índice de color (proxy de temperatura; azul/caliente a la izquierda, rojo/frío a la derecha)

Cada región del CMD corresponde a una fase específica de la evolución estelar y proporciona información única sobre las propiedades físicas y la historia de las poblaciones estelares.

---

## Regiones del CMD y su Significado Físico

### ZAMS (Zero-Age Main Sequence)

**Definición:**  
Posición teórica de la secuencia principal justo cuando las estrellas inician la fusión de hidrógeno en el núcleo. Representa el "punto de partida" de la vida estelar en la secuencia principal.

**Características observacionales:**
- Marca la "línea de partida" de la MS
- Las estrellas más jóvenes de una población se sitúan cerca de la ZAMS
- Define el límite inferior (más débil y azul) de la MS para cada masa

**Indicador físico:**
- La masa inicial y composición química (metalicidad Z, fracción de helio Y) determinan la ubicación sobre la ZAMS
- Las estrellas se desplazan ligeramente de la ZAMS a medida que evolucionan en la MS

---

### MS (Main Sequence) — Secuencia Principal

**Definición:**  
Banda donde las estrellas queman hidrógeno en el núcleo mediante fusión nuclear estable. Es la fase más larga de la vida estelar (~90% del tiempo total).

**Características observacionales:**
- Diagonal desde azul y brillante (estrellas masivas) hacia rojo y débil (estrellas de baja masa)
- La pendiente y dispersión informan sobre la mezcla de masas, extinción y presencia de binarias
- Ancho aparente aumentado por errores fotométricos, binarias no resueltas y variaciones de metalicidad

**Procesos físicos:**
- Fusión H → He en el núcleo (cadena p-p para M < 1.3 M☉, ciclo CNO para masas mayores)
- Equilibrio hidrostático entre presión de radiación y gravedad
- Cambios graduales en composición química del núcleo

---

### MSTO (Main Sequence Turn-Off) — Punto de Giro

**Definición:**  
Punto donde las estrellas más masivas aún presentes en la MS comienzan a agotar el hidrógeno central y se alejan de la secuencia principal.

**Características observacionales:**
- Aparece como un "codo" o punto de inflexión en el CMD
- Su magnitud y color son **muy sensibles a la edad**
- Poblaciones más viejas tienen MSTO más débil (magnitud mayor) y más rojo
- Poblaciones más jóvenes tienen MSTO más brillante y más azul

**Uso práctico:**
- **Indicador primario de edad** para poblaciones coevales (SSPs)
- Medir la edad comparando la magnitud del MSTO con isócronas teóricas
- Determinar la masa de las estrellas que están abandonando la MS

| Edad aproximada | MSTO (M_V) | MSTO Color (B-V) |
|-----------------|------------|------------------|
| 1 Gyr           | ~+2.0      | ~0.3             |
| 5 Gyr           | ~+3.5      | ~0.5             |
| 10 Gyr          | ~+4.0      | ~0.6             |
| 13 Gyr          | ~+4.3      | ~0.7             |

*Valores aproximados para [Fe/H] = −1.5*

---

### SGB (Subgiant Branch) — Rama de Subgigantes

**Definición:**  
Fase de transición entre el MSTO y la RGB; corresponde a estrellas que han terminado la fusión central de hidrógeno y expanden su envoltura.

**Características observacionales:**
- Banda corta y casi horizontal que conecta MSTO con RGB
- Relativamente despoblada debido a su corta duración
- Se desplaza hacia colores más rojos

**Indicador físico:**
- El tiempo de transición y la forma de la SGB pueden indicar diferencias de edad y mezcla convectiva
- El núcleo de helio inerte se contrae mientras la envoltura se expande
- Comienza la fusión de hidrógeno en capa (shell burning)

---

### RGB (Red Giant Branch) — Rama de Gigantes Rojas

**Definición:**  
Fase de fusión de hidrógeno en una capa alrededor del núcleo inerte de helio; las estrellas se vuelven muy luminosas y frías.

**Características observacionales:**
- Secuencia roja y casi vertical o diagonal en el CMD
- La pendiente y color dependen **fuertemente de la metalicidad**:
  - Mayor [Fe/H] → RGB más roja
  - Menor [Fe/H] → RGB más azul y empinada
- La punta de la RGB (TRGB) es un indicador de distancia estándar

**Indicador físico:**
- Núcleo de helio degenerado (para estrellas de baja masa)
- Expansión de la envoltura hasta cientos de veces el radio original
- Pérdida de masa significativa a través de vientos estelares
- Eventos de dragado (dredge-up) que traen material procesado a la superficie

**Uso:**
- Medir [Fe/H] relativo comparando el color de la RGB
- Distinguir poblaciones por la posición y pendiente de la RGB
- Estimar distancias mediante el TRGB

---

### HB (Horizontal Branch) / Red Clump

**Definición:**  
Fase de fusión de helio en el núcleo mediante el proceso triple-alfa (He → C, O).

**Características observacionales:**

| Tipo | Población típica | Apariencia en CMD |
|------|------------------|-------------------|
| **HB (Horizontal Branch)** | Poblaciones antiguas, pobres en metales | Distribución extendida en temperatura (azul a rojo) |
| **Red Clump** | Poblaciones intermedias/ricas en metales | Concentración prominente y compacta |

**Indicador físico:**
- Después del flash de helio, se establece la fusión estable de He
- Doble fuente de energía: fusión de He en núcleo + fusión de H en capa
- La morfología de la HB depende de la metalicidad, edad y pérdida de masa previa

**Uso:**
- Trazador de edad y pérdida de masa en RGB
- Las estrellas RR Lyrae ocupan parte de la HB (zona de inestabilidad)
- El Red Clump sirve como candela estándar para medir distancias

---

### Instability Strip — Franja de Inestabilidad (IS)

**Definición:**  
Región del CMD donde las estrellas son susceptibles a pulsaciones radiales regulares debido al mecanismo κ (kappa).

**Características observacionales:**
- Cruza la HB y la región de supergigantes
- Estrellas en esta franja varían periódicamente en magnitud, temperatura y radio
- Posición en temperatura: ~5500–7500 K

**Tipos de variables en la IS:**

| Tipo | Descripción | Período típico |
|------|-------------|----------------|
| **Cefeidas clásicas** | Supergigantes masivas | Días a semanas |
| **RR Lyrae** | Estrellas de HB, pobres en metales | ~0.2–1.0 días |
| **δ Scuti** | MS superior a subgigantes | Horas |
| **W Virginis** | Cefeidas de Población II | Días |

**Posición respecto al MSTO:**
- La IS suele localizarse a **magnitudes más brillantes** (por encima en el eje vertical del CMD) que el MSTO de una población coeval típica
- Ejemplo: RR Lyrae ocupan la HB y son más luminosas que el MSTO en poblaciones antiguas
- En poblaciones muy jóvenes el MSTO puede ser excepcionalmente brillante, por lo que la comparación depende de la edad

**Uso práctico:**
- Localizar variables para calibrar distancias (relación período-luminosidad)
- RR Lyrae como trazadores de distancia en poblaciones viejas
- Cefeidas como candelas estándar en el universo cercano

---

### AGB (Asymptotic Giant Branch) — Rama Asintótica de Gigantes

**Definición:**  
Fase posterior a la HB con núcleos de carbono y oxígeno, envolturas expandidas y frecuentemente pulsantes; muy luminosa especialmente en el infrarrojo.

**Características observacionales:**
- Se sitúa por encima de la RGB en luminosidad
- Gran dispersión en color debido a envolturas y formación de polvo circunestelar
- Algunas estrellas AGB son variables de largo período (Miras)
- Rama casi paralela a la RGB pero "asintótica" a ella

**Indicador físico:**
- Núcleo inerte de C/O
- Doble capa de fusión: He en capa interna, H en capa externa
- Pulsos térmicos que provocan eventos de dragado
- Pérdida de masa intensa (eventual expulsión de envolturas → nebulosas planetarias)
- Nucleosíntesis del proceso-s (producción de elementos pesados)

**Uso:**
- Estudiar pérdida de masa y evolución química
- Contribución al enriquecimiento químico del medio interestelar
- Trazadores de poblaciones de edad intermedia

---

### WD Cooling Sequence — Secuencia de Enfriamiento de Enanas Blancas

**Definición:**  
Secuencia de enanas blancas que se enfrían progresivamente tras perder sus envolturas en la fase AGB.

**Características observacionales:**
- Secuencia tenue y azul-gris hacia magnitudes débiles
- Diagonal descendente: las WD más antiguas son más frías y débiles
- El "corte" de enfriamiento (punto más débil observable) proporciona una cota de edad

**Características físicas:**
- No hay fusión nuclear activa
- Soportadas por presión de degeneración electrónica
- Masa típica: ~0.6 M☉
- Radio típico: comparable al de la Tierra
- Enfriamiento sigue una relación predecible con el tiempo

**Uso:**
- **Estimar edad absoluta** de poblaciones antiguas mediante el punto de corte más luminoso en la secuencia de WDs
- Método independiente de determinación de edad (alternativo al MSTO)
- Estudio de la física de materia degenerada

---

### Blue Stragglers — Rezagadas Azules

**Definición:**  
Estrellas más azules y brillantes que el MSTO de la población; no encajan en la evolución estelar simple de estrellas individuales.

**Origen probable:**
- Fusiones estelares en sistemas binarios cercanos
- Transferencia de masa desde una compañera evolucionada
- Colisiones directas en regiones densas (núcleos de cúmulos)

**Características observacionales:**
- Aparecen hacia la MS superior, por encima y a la izquierda del MSTO
- Más frecuentes en núcleos densos de cúmulos globulares
- Algunas tienen compañeras enana blanca (evidencia de transferencia de masa)
- Pueden mostrar rotación rápida (evidencia de fusión)

**Uso:**
- Trazadores de interacciones dinámicas en cúmulos
- Estudio de evolución de binarias
- Indicadores de la densidad central del cúmulo

---

## Efectos Observacionales que Alteran el CMD

### Extinción y Enrojecimiento

El polvo interestelar absorbe y dispersa la luz estelar, afectando tanto el color como la magnitud observada.

**Correcciones:**
- Exceso de color: $E(B-V) = (B-V)_{\text{obs}} - (B-V)_0$
- Extinción en banda V: $A_V \approx 3.1 \times E(B-V)$ (ley estándar)
- Color intrínseco: $(B-V)_0 = (B-V)_{\text{obs}} - E(B-V)$
- Magnitud corregida: $m_0 = m_{\text{obs}} - A_\lambda$

**Efecto en el CMD:**
- Vector de extinción desplaza puntos hacia más rojos y más débiles en magnitud
- Puede simular poblaciones más viejas o más metálicas si no se corrige

---

### Distancia

El alejamiento de una población estelar cambia únicamente su magnitud aparente, sin afectar el color.

**Módulo de distancia:**
$$m - M = 5\log_{10}(d/\text{pc}) - 5$$

Donde:
- $m$ = magnitud aparente
- $M$ = magnitud absoluta
- $d$ = distancia en parsecs

**Efecto en el CMD:**
- Translación vertical pura (todas las estrellas se desplazan igual)
- No afecta la forma de las secuencias ni los colores

---

### Binarias No Resueltas

Sistemas binarios que aparecen como una única fuente debido a limitaciones de resolución angular.

**Efecto cuantitativo:**
Para dos estrellas idénticas combinadas:
$$\Delta m = -2.5 \log_{10}(2) \approx -0.75 \text{ mag}$$

**Efecto en el CMD:**
- Causan una secuencia paralela a la MS principal, hasta ~0.75 mag más brillante
- Aumentan la dispersión en color y magnitud
- Binarias con componentes de masas diferentes producen colores intermedios

---

### Errores Fotométricos y Sesgos de Selección

**Efectos:**
- Ruido aleatorio genera dispersión artificial en todas las secuencias
- Saturación de detectores en estrellas brillantes
- Límites de detección cortan las secuencias en magnitudes débiles
- Sesgos de completitud afectan la densidad relativa de diferentes regiones

**Mitigación:**
- Caracterizar errores fotométricos como función de magnitud
- Aplicar correcciones de completitud estadísticas
- Usar estrellas artificiales para cuantificar sesgos

---

## Funciones de la Población: IMF y SFR

### IMF (Initial Mass Function) — Función de Masa Inicial

**Definición:**  
Distribución de masas iniciales con la que nacen las estrellas en una población.

**Expresión matemática:**
$$\xi(M) = \frac{dN}{dM} \propto M^{-\alpha}$$

Donde:
- $\xi(M)$ = número de estrellas por intervalo de masa
- $dN$ = número de estrellas en el intervalo $[M, M+dM]$
- $\alpha$ = índice de pendiente (exponente)

**Unidades:** "número de estrellas por unidad de masa" (ej. estrellas por $M_\odot$)

**Formas habituales:**

| IMF | Expresión | Características |
|-----|-----------|-----------------|
| **Salpeter (1955)** | $\xi(M) \propto M^{-2.35}$ | Ley de potencia única, $M > 0.5 M_\odot$ |
| **Kroupa (2001)** | Segmentada con quiebres | Más realista para todo el rango de masas |
| **Chabrier (2003)** | Log-normal + power law | Popular en estudios extragalácticos |

**IMF de Kroupa (segmentada):**
- $\xi(M) \propto M^{-0.3}$ para $0.01 \leq M/M_\odot < 0.08$
- $\xi(M) \propto M^{-1.3}$ para $0.08 \leq M/M_\odot < 0.5$
- $\xi(M) \propto M^{-2.3}$ para $M/M_\odot \geq 0.5$

**Uso observacional:**
- La IMF determina la fracción de estrellas masivas (luminosas, vidas cortas) frente a estrellas de baja masa (débiles, vidas largas)
- Afecta la apariencia del CMD: una IMF con más estrellas masivas produce más gigantes luminosas y más Cefeidas en poblaciones jóvenes
- Influye en la pendiente y densidad de la MS

---

### SFR (Star Formation Rate) — Tasa de Formación Estelar

**Definición:**  
Tasa de formación estelar en una región o galaxia.

**Expresión matemática:**
$$\psi(t) = \frac{dM_\star}{dt}$$

Donde:
- $\psi(t)$ = tasa de formación estelar
- $dM_\star$ = masa convertida en estrellas en el intervalo $dt$

**Unidades:** $M_\odot \, \text{yr}^{-1}$

**Tipos de historia de formación estelar:**

| Tipo | Descripción | Apariencia en CMD |
|------|-------------|-------------------|
| **Burst instantáneo** | Toda la población se forma simultáneamente | Secuencias bien definidas (SSP ideal) |
| **Constante** | SFR uniforme en el tiempo | Superposición de edades |
| **Exponencial decreciente** | $\psi(t) \propto e^{-t/\tau}$ | Dominada por estrellas viejas |
| **Retardada** | $\psi(t) \propto t \cdot e^{-t/\tau}$ | Formación gradual con pico tardío |

**Interpretación en el CMD:**
- SFR puntual (burst) → población coeval, ideal para estudiar isócronas
- SFR continua → superposición de edades, CMD más complejo con múltiples MSTOs

**Uso práctico:**
- La forma del MS superior y la presencia de objetos muy brillantes indican SFR reciente
- La densidad relativa en el MSTO y SGB muestra la historia de formación estelar
- Poblaciones mixtas muestran secuencias más anchas y menos definidas

---

### Combinando IMF + SFR

Para modelar un CMD sintético se necesita especificar tanto la IMF como la SFR (y la metalicidad):

- **IMF:** Fija cuántas estrellas nacen en cada intervalo de masa
- **SFR:** Determina cuándo nacen las estrellas
- **Juntas:** Controlan la distribución de puntos en el CMD y la abundancia relativa de fases evolutivas observadas

**Ejemplo:** Un CMD sintético requiere:
1. Elegir IMF (ej. Kroupa)
2. Definir SFR (ej. burst a 10 Gyr)
3. Especificar metalicidad [Fe/H]
4. Aplicar módulo de distancia y extinción
5. Añadir errores fotométricos realistas

---

## Cómo Usar esta Guía

### Para identificar la **edad** de una población coeval:
1. Localizar el MSTO en el CMD
2. Medir su magnitud y color
3. Comparar con isócronas de distintas edades
4. La isócrona que mejor ajuste el MSTO da la edad

### Para estimar **metalicidad** relativa:
1. Identificar la RGB en el CMD
2. Comparar su posición y pendiente con isócronas
3. RGB más roja → mayor metalicidad
4. RGB más empinada → menor metalicidad

### Para detectar **poblaciones múltiples**:
1. Buscar secuencias dobles o ensanchadas en:
   - MS (diferentes edades o metalicidades)
   - SGB (diferencias de edad)
   - RGB (variaciones químicas)
2. Analizar la dispersión más allá de errores fotométricos

### Para estudiar **variables**:
1. Localizar la Instability Strip (región de ~5500–7500 K)
2. Identificar estrellas con variabilidad fotométrica
3. Clasificar por tipo (RR Lyrae, Cefeidas, δ Scuti)
4. Usar relaciones período-luminosidad para distancias

---

## Diagrama Esquemático del CMD

```
         Magnitud (más brillante ↑)
            │
            │        ★ (AGB tip)
            │       ★ ★
      Más   │      ★  ★
    brillante      ★   ★  ← AGB
            │     ★    ★
            │    ★  ★★ ★  ← RGB tip
            │   ★   ★  ★
            │  ★    ★   ★
            │ ★     ★    ★  ← RGB
            │★      ★     ★
            │★     ★★      ★
            │★   ★★★★★     ★  ← Red Clump / HB
            │★  ★★★★       ★
            ├─────────────────────── IS (Instability Strip)
            │★ ★★★  ★★★
            │★★★★    ★★★  ← SGB
            │ ★★★     ★★★
            │  ★★★★★   ★★★ ← MSTO
            │   ★★★★★★  ★★★
            │ BS ★★★★★★★ ★★★ ← MS
            │ ↖   ★★★★★★★★★★★
            │      ★★★★★★★★★★★ ← ZAMS
            │       ★★★★★★★★★★★
            │
            │      ○○○○
            │       ○○○○○  ← WD cooling sequence
            │        ○○○○○○
            │         ○○○○○○○
            └────────────────────────────────────→
                  azul        Color         rojo
               (caliente)                 (frío)
```

**Leyenda:**
- ★ = Estrellas en diferentes fases evolutivas
- ○ = Enanas blancas
- BS = Blue Stragglers
- IS = Instability Strip (franja vertical)

---

## Resumen de Diagnósticos

| Característica del CMD | Diagnóstico / Información |
|------------------------|---------------------------|
| **Posición del MSTO** | Edad de la población |
| **Color de la RGB** | Metalicidad [Fe/H] |
| **Pendiente de la RGB** | Metalicidad (más empinada = menor [Fe/H]) |
| **Extensión de la HB** | Edad + pérdida de masa en RGB |
| **Morfología del Red Clump** | Metalicidad y edad |
| **Ancho de la MS** | Binarias + errores + dispersión en [Fe/H] |
| **Blue Stragglers** | Dinámica + historia de binarias |
| **Luminosidad del RC** | Distancia (candela estándar) |
| **Corte de WD** | Edad del sistema (método independiente) |
| **Densidad relativa SGB/RGB** | Historia de formación estelar |

---

## Referencias

### Artículos fundamentales

- **Salpeter, E.E. (1955)** ApJ, 121, 161 — IMF original
- **Kroupa, P. (2001)** MNRAS, 322, 231 — IMF segmentada moderna
- **Chabrier, G. (2003)** PASP, 115, 763 — IMF log-normal
- **Harris, W.E. (1996)** AJ, 112, 1487 — Catálogo de cúmulos globulares

### Isócronas y modelos

- **PARSEC/COLIBRI** — http://stev.oapd.inaf.it/cgi-bin/cmd
- **MIST** — http://waps.cfa.harvard.edu/MIST/
- **BaSTI** — http://basti-iac.oa-teramo.inaf.it/
- **IAC-STAR** — http://iac-star.iac.es/

### Libros de texto recomendados

- Kippenhahn, R., Weigert, A., & Weiss, A. (2012). *Stellar Structure and Evolution*. Springer.
- Salaris, M., & Cassisi, S. (2005). *Evolution of Stars and Stellar Populations*. Wiley.
- Carroll, B. W., & Ostlie, D. A. (2017). *An Introduction to Modern Astrophysics*. Cambridge University Press.

---

## Documentos Relacionados

- [Clase 1: Introducción a Poblaciones Estelares](01_poblaciones_estelares.md)
- [Ejemplos y Ejercicios de CMD](13_examples_cmd.md)
- [Evolución Estelar en el CMD](evolucion_estelar_CMD.md)

---

*Documento creado para el repositorio ISI_2025 — Guía de Referencia del Diagrama Color-Magnitud*
