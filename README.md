# Práctica 2 – Optimización Estocástica  
## Portafolios mean–CVaR: SAA vs. DRO-Wasserstein (p = 1, 2)

Este repositorio contiene un **notebook reproducible** y **código Python** para construir y evaluar portafolios **mean–CVaR** usando:
- **SAA** (Sample Average Approximation) para mean–CVaR.
- **DRO Wasserstein** con **p = 1** y **p = 2** (robustificación sobre la distribución empírica).
- **Backtesting rolling** con rebalanceo y comparación frente a **asignación constante (EW)**.

Incluye utilidades para **graficar riqueza** por ε (y benchmark constante) y un **informe LaTeX** que resume el análisis.

---

## Requisitos

- Python 3.10+ (recomendado 3.11)
- 
## 🔧 Librerías usadas (Python)

| Librería       | Uso principal |
|----------------|---------------|
| **numpy**      | álgebra y manejo de matrices de retornos |
| **pandas**     | ETL de series de tiempo y tablas de métricas |
| **matplotlib** | gráficos de riqueza/curvas comparativas |
| **tqdm**       | barras de progreso en corridas rolling |
| **cvxpy**      | modelado convex y resolución de DRO (W₁/W₂) |
| **scs**        | solver para `cvxpy` (fallback robusto) |
| **ecos**       | solver para `cvxpy` (rápido en SOCP) |
| **yfinance**   | descarga de precios históricos (opcional) |
| **jupyter**    | ejecución del notebook |
| **nbconvert**  | exportar `.ipynb` a HTML/PDF |
| **nbconvert[webpdf]** | exportar a PDF vía navegador (sin LaTeX) |
| **pyppeteer**  | motor headless para `webpdf` |

> **Nota:** Si vienes de una versión previa con Gurobi, aquí **no es necesario**. Todo el flujo usa **cvxpy** con **SCS/ECOS**.

