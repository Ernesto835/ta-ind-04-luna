# TA-IND-04: Análisis de Rendimiento Paralelo aplicado al Proyecto Fin de Curso (PFC BCEL - SGA)

**Universidad Técnica Estatal de Quevedo**  
**Facultad de Ciencias de la Computación — Carrera de Ingeniería de Software**  
**Asignatura:** Aplicaciones Distribuidas (ISR-701) — Unidad 4  
**Estudiante:** Ernesto Gregory Luna Mora  
**Período Académico:** 2026–2027 PPA  
**Docente Responsable:** Gleiston C. Guerrero-Ulloa, M.Sc.  

---

## 1. Declaración de Contexto e Identificación

- **Código de Actividad:** TA-IND-04 — Informe Técnico Individual
- **PFC de Origen:** **BCEL — SGA (Sistema de Gestión Académica de la Escuela Provincias Unidas)**
- **Roles del SGA:** **Secretaría, Docente, Rector, Soporte Técnico**
- **PFC de Referencia (PE-U4):** ACC — Soporte Técnico ISP
- **Modalidad de Trabajo:** Individual  
- **Autor:** Ernesto Gregory Luna Mora (BCEL / SGA)  
- **Transformación Declarada como Foco Individual:** **T3 — Join relacional entre DataFrames**

---

## 2. Trazabilidad de los Datos Base

Los datos experimentales medidos corresponden a la práctica sumativa grupal **GA-SUM-05 / PE-U4**:

- **URL del Repositorio de Origen:** [https://github.com/CristhianP03/pe-u4-spark-equipoA.git](https://github.com/CristhianP03/pe-u4-spark-equipoA.git)
- **Commit Hash de Origen:** `6e70e75865b0e873bfc876b6029ff49fbfc1df33`
- **Plataforma de Ejecución:** Google Colab (Linux, PySpark 3.5.3, Spark Engine 3.5.3 con Java 17.0.19, Pandas 2.2.3, Python 3.12).
- **Archivo de Tiempos Base Versionado:** [`datos/tiempos_base.csv`](datos/tiempos_base.csv)

---

## 3. Estructura del Repositorio Individual

```text
ta-ind-04-luna/
├── README.md               # Identificación, trazabilidad e instrucciones exactas de compilación
├── LICENSE                 # Licencia MIT de distribución del código e informe
├── TA-IND-04_LunaErnesto.pdf # Documento PDF de 1 página para la entrega en SGA / LMS
├── docs/
│   ├── TA_IND_04_Informe.tex # Documento LaTeX principal del informe individual (≥ 4 pág. contenido)
│   ├── TA_IND_04_Informe.pdf # Documento PDF compilado reproducible
│   └── references.bib      # Bibliografía IEEE gestionada con biblatex + biber
├── datos/
│   └── tiempos_base.csv    # Copia fidedigna de resultados/tiempos_resumen.csv del commit de origen
└── figuras/
    ├── fig_speedup.png     # Gráfica propia a 300 DPI: Speedup medido vs Amdahl (Foco T3)
    ├── fig_karp_flatt.png   # Gráfica propia a 300 DPI: Tendencia de la métrica de Karp-Flatt
    ├── fig_breakeven.png    # Gráfica propia a 300 DPI: Escalabilidad por volumen y umbral n*
    └── fig_arch_integration.png # Gráfica propia a 300 DPI: Diagrama de integración en PFC BCEL (SGA)
```

---

## 4. Instrucciones Exactas de Compilación

El documento `docs/TA_IND_04_Informe.tex` se compila en un entorno LaTeX moderno (por ejemplo, MiKTeX 25.12 / TeX Live 2024) utilizando `pdflatex` y la herramienta de bibliografía `biber`.

### Secuencia Exacta de Comandos (Terminal / CLI)

Ejecutar la siguiente secuencia de comandos desde el directorio raíz del repositorio:

```bash
# 1. Navegar a la carpeta docs/
cd docs

# 2. Primera pasada de pdflatex (genera auxiliares y citas pendientes)
pdflatex TA_IND_04_Informe.tex

# 3. Procesar las referencias bibliográficas con biber
biber TA_IND_04_Informe

# 4. Segunda pasada de pdflatex (resuelve citas y números de bibliografía)
pdflatex TA_IND_04_Informe.tex

# 5. Tercera pasada de pdflatex (resuelve referencias cruzadas e índices de páginas)
pdflatex TA_IND_04_Informe.tex
```

El resultado final se generará en `docs/TA_IND_04_Informe.pdf`.

---

## 5. Declaración de Uso de Inteligencia Artificial Generativa

Se declara que se utilizó asistencia de inteligencia artificial únicamente como una guía superficial y puntual en aspectos menores de maquetación en LaTeX y formato de ecuaciones. Todo el análisis cuantitativo, desarrollo matemático, gráficos y decisiones de arquitectura del PFC BCEL (SGA) son de autoría directa e individual responsabilidad del estudiante.
