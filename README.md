# Práctica 2 – Optimización Estocástica  
## Portafolios mean–CVaR: SAA vs. DRO-Wasserstein (p = 1, 2)

Este repositorio contiene un **notebook reproducible** y **código Python** para construir y evaluar portafolios **mean–CVaR** usando:
- **SAA** (Sample Average Approximation) para mean–CVaR.
- **DRO Wasserstein** con **p = 1** y **p = 2** (robustificación sobre la distribución empírica).
- **Backtesting rolling** con rebalanceo y comparación frente a **asignación constante (EW)**.

Incluye utilidades para **graficar riqueza** por ε (y benchmark constante) y un **informe LaTeX** que resume el análisis.

---

## Contenidos

- `notebooks/Practica2-OptSth-Rios-Brahyan.ipynb`  
  Notebook principal del trabajo (análisis, corridas y figuras).
- `src/dro_solvers.py`  
  Implementaciones **cvxpy** de DRO W₁/W₂ y runner rolling.
- `src/plots.py`  
  Funciones para graficar riqueza por ε, comparación p=1 vs p=2, y benchmark constante.
- `reports/informe_opt_estocastica.tex`  
  Plantilla LaTeX del informe (lista para compilar).
- `figures/`  
  Carpeta sugerida para exportar las figuras (`wealth_w1_constante.png`, etc.).
- `data/`  
  (Opcional) Datos procesados o CSVs de métricas.
- `requirements.txt`  
  Dependencias mínimas del proyecto.

> **Nota:** Si solo usarás el notebook, bastará con tener instaladas las dependencias de `requirements.txt`.

---

## Requisitos

- Python 3.10+ (recomendado 3.11)
- Dependencias:
  ```bash
  pip install -r requirements.txt
