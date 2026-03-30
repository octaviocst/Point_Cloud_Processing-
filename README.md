# ☕ Coffee Point Cloud Height

**Pipeline em R para modelagem estrutural de cafezais a partir de nuvens
de pontos LiDAR de drone**

[![R](https://img.shields.io/badge/R-276DC3?style=flat&logo=r&logoColor=white)](https://www.r-project.org/)
[![Status](https://img.shields.io/badge/Status-Ativo-brightgreen)]()
[![UFLA](https://img.shields.io/badge/Desenvolvido%20em-UFLA-green)]()

> Script em **R** para processamento de **nuvens de pontos (.LAS)** e
> geração de modelos estruturais do dossel de café, incluindo **MDT, MDS
> e CHM**, com extração de métricas por planta a partir de pontos GPS.

**Autor:** Octávio Pereira da Costa --- UFLA

------------------------------------------------------------------------

## 📋 Visão Geral

O **Coffee Point Cloud Height** implementa um fluxo básico de
processamento de nuvem de pontos usando o pacote `lidR`.

Pipeline geral:

    LAS → Classificação do solo → MDT → Normalização → CHM / DSM → Estatísticas por planta

Principais produtos gerados:

-   **MDT (DTM)** --- Modelo Digital do Terreno\
-   **MDS (DSM)** --- Modelo de Superfície\
-   **CHM** --- Modelo de Altura do Dossel\
-   **Estatísticas zonais de altura por planta**

------------------------------------------------------------------------

## ✨ Funcionalidades

-   Leitura e verificação de nuvens de pontos `.las`
-   Classificação automática do solo (CSF)
-   Geração de **MDT, DSM e CHM**
-   Visualização 2D e 3D dos modelos
-   Extração de métricas de altura via **buffers em pontos GPS**
-   Exportação de rasters e tabelas para análise posterior

------------------------------------------------------------------------

## 🗂 Estrutura do Repositório

    Coffee_PointCloud_Height/

    │
    ├── Coffee_PointCloud_Height.Rmd   # Script principal
    │
    ├── LAS/                           # Nuvens de pontos (não versionadas)
    │
    ├── Shp/                           # Pontos GPS ou parcelas
    │
    ├── Raster/                        # Modelos gerados (MDT, DSM, CHM)
    │
    ├── data/                          # Resultados tabulares
    │
    └── README.md

------------------------------------------------------------------------

## 🚀 Como Usar

### 1. Instalar pacotes

``` r
install.packages(c(
  "lidR",
  "terra",
  "sf",
  "ggplot2",
  "dplyr"
))
```

### 2. Executar o script

Abra o arquivo:

    Coffee_PointCloud_Height.Rmd

no **RStudio** e execute os chunks ou utilize **Knit** para gerar o
relatório completo.

------------------------------------------------------------------------

## 📦 Pacotes Principais

  Pacote      Função
  ----------- ----------------------------------------
  `lidR`      Processamento de nuvem de pontos LiDAR
  `terra`     Manipulação de rasters
  `sf`        Manipulação de shapefiles
  `ggplot2`   Visualização

------------------------------------------------------------------------

## 🌱 Aplicação

Pipeline desenvolvido para **fenotipagem estrutural de cafezais com
drones**, utilizado em pesquisas da **Universidade Federal de Lavras
(UFLA)**.

Aplicações incluem:

-   estimativa de **altura de plantas**
-   análise estrutural do dossel
-   geração de variáveis para **modelagem estatística e machine
    learning**

------------------------------------------------------------------------

## 📬 Contato

**Octávio Pereira da Costa**\
🎓 Doutorando em Fitotecnia --- UFLA

📧 octavio.cst@gmail.com

🔗 https://linkedin.com/in/octavio-costa-3b32a7b2\
🐙 https://github.com/octaviocst
