---
title: Setup
---

El ‘Curso en ciencia de datos en salud pública y modelamiento de enfermedades infecciosas’ es liderado por la Pontificia Universidad Javeriana en el marco del proyecto Epiverse-TRACE-LAC y cuenta con el apoyo de la Universidad de los Andes, el London School of Hygiene and Tropical Medicine, data.org, el Centro Internacional de Investigaciones para el Desarrollo (IDRC) de Canadá, la Secretaría de Salud de Bogotá, el Instituto Nacional de Salud (INS), el Field Epidemiology Training Program (FETP), la Red de Programas de Epidemiología de Campo en América del Sur (REDSUR), el Imperial College de Londres y la Universidad de Sussex. 


Este curso asincrónico tiene como objetivo fortalecer la capacidad de análisis y modelamiento de brotes de enfermedades infecciosas en la región de América Latina y el Caribe, mediante el uso de herramientas de alta calidad, de código abierto e interoperables que ayuden en la toma de decisiones en salud pública. El curso está dirigido a 1000 profesionales de la salud y otras áreas de STEM que buscan mejorar sus habilidades dentro del ecosistema de ciencia de datos y salud pública para responder a futuras crisis de salud.

En esta página encontrará el material práctico de los talleres.

Para más información sobre el proyecto consulte nuestra página: [Página del proyecto en github](https://epiverse-trace.github.io/epi-training-kit/)


## Normas del curso

Conozca nuestro [código de conducta TRACE-LAC](https://drive.google.com/file/d/1z9EecMJR0CIyrUI6hzUugS4i9aAgSD-5/view?usp=sharing).

## Configuración del software

Siga estos dos pasos:

### 1. Instale o actualice R y RStudio

R y RStudio son dos piezas separadas de software: 

* **R** es un lenguaje de programación y software utilizado para ejecutar código escrito en R.
* **RStudio** es un entorno de desarrollo integrado (IDE) que facilita el uso de R. Recomendamos utilizar RStudio para interactuar con R. 

Para instalar R y RStudio, siga estas instrucciones <https://posit.co/download/rstudio-desktop/>.

::::::::::::::::::::::::::::: callout

### ¿Ya está instalado? 

Espere: Este es un buen momento para asegurarse de que su instalación de R está actualizada.

Este tutorial requiere **R versión 4.0.0 o posterior**.

:::::::::::::::::::::::::::::

Para comprobar si tu versión de R está actualizada:

- En RStudio tu versión de R se imprimirá en [la ventana de la consola](https://docs.posit.co/ide/user/ide/guide/code/console.html). O ejecute `sessionInfo()` allí.

- **Para actualizar R**, descargue e instale la última versión desde el [sitio web del proyecto R](https://cran.rstudio.com/) para su sistema operativo.

  - Después de instalar una nueva versión, tendrás que reinstalar todos tus paquetes con la nueva versión. 

  - Para Windows, el paquete `{installr}` puede actualizar su versión de R y migrar su biblioteca de paquetes.

- **Para actualizar RStudio**, abra RStudio y haga clic en 
Ayuda > Buscar actualizaciones`. Si hay una nueva versión disponible siga las 
instrucciones en pantalla.

::::::::::::::::::::::::::::: callout

### Buscar actualizaciones regularmente

Aunque esto puede sonar aterrador, es **mucho más común** encontrarse con problemas debido al uso de versiones desactualizadas de R o de paquetes de R. Mantenerse al día con las últimas versiones de R, RStudio, y cualquier paquete que utilice regularmente es una buena práctica.

:::::::::::::::::::::::::::::

### 2. Instale los paquetes R necesarios

<!--
During the tutorial, we will need a number of R packages. Packages contain useful R code written by other people. We will use packages from the [Epiverse-TRACE](https://epiverse-trace.github.io/). 
-->

Abra RStudio y **copie y pegue** el siguiente fragmento de código en la [ventana de la consola](https://docs.posit.co/ide/user/ide/guide/code/console.html), luego presione < kbd>Enter</kbd> (Windows y Linux) o <kbd>Return</kbd> (MacOS) para ejecutar el comando:

```r
# para episodios los primeros 4 episodios

if(!require("pak")) install.packages("pak")

new_packages <- c(
  "cleanepi",
  "rio",
  "tidyverse",
  "knitr"
)

pak::pkg_install(new_packages)
```

```r
# para episodio Construyendo un modelo deterministico simple

if(!require("pak")) install.packages("pak")

new_packages <- c(
  "deSolve",
  "cowplot",
  "tidyverse"
)

pak::pkg_install(new_packages)
```

Debería actualizar **todos los paquetes** necesarios para el tutorial, aunque los haya instalado hace relativamente poco. Las nuevas versiones traen mejoras y correcciones de errores importantes.

Cuando la instalación haya terminado, puedes intentar cargar los paquetes pegando el siguiente código en la consola:

```r
# para los primeros 4 episodios

library(tidyverse) # contiene ggplot2, dplyr, tidyr, readr, purrr, tibble
library(readxl) # para leer archivos Excel
library(knitr) # para crear tablas bonitas con kable()
library(cleanepi) # para limpieza de datos
library(rio) # para importar y exportar tablas de datos
```

```r
# para episodio sobre modelo matemático

library(deSolve)   # Paquete deSolve para resolver las ecuaciones diferenciales
library(tidyverse) # Paquetes ggplot2 y dplyr de tidyverse
library(cowplot) # Paquete gridExtra para unir gráficos.
```

## Dataset

Recuerde almacenarlos en la carpeta **data** en la ubicación de su proyecto.

Episodio Introducción a R y Rstudio:  

- Datos para [la práctica](https://raw.githubusercontent.com/TRACE-LAC/TRACE-LAC-data/main/datos_covid.xlsx)
- Datos para [Actividad de afianzamiento](https://github.com/TRACE-LAC/TRACE-LAC-data/raw/refs/heads/main/otros/datos_limpios_covid.RDS) 

Episodio Reporte e informes tecnicos en R Markdown:  
 
- Datos para [la práctica](https://github.com/TRACE-LAC/TRACE-LAC-data/blob/main/otros/muestra_covid.RDS?raw=true)    
 
Episodio Introducción a la visualizacion de datos en R con ggplot2:

- Datos para [la práctica](https://github.com/TRACE-LAC/TRACE-LAC-data/blob/main/otros/muestra_covid.RDS?raw=true) (Son los mismos datos de la práctica de R Markdown)

Episodio Limpieza de datos epidemiológicos usando R:

- Datos para [la práctica](https://github.com/TRACE-LAC/TRACE-LAC-data/raw/main/data_limpieza.zip) Descomprimados y ponga el contenido en su carpeta **data**
