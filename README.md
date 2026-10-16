# PDF-en-RStudio
Una guía para el uso de archivos pdf en RStudio, usando las paqueterías qpdf (Ooms, 2025) y pdftools (Ooms, 2026), con Ghostscript.

## Origen de esta Guía

**¿Por qué necesitamos un editor más de PDF?** Estoy de acuerdo en que ya existe ilovepdf (que es la principal herramienta de uso común hoy en día), CamScanner, Adobe, los propios exploradores web al imprimir, PDFGuru, etc. 

En mi caso particular, fue porque cuando necesité editar un pdf con más de 4000 páginas (y con menos de 6 MB de peso), lo que tenía que hacer era sencillo, quitar las páginas 15 a la 20 que no eran necesarias, un extracto pequeño, pero al momento de usar alguna de las herramientas anteriores, todas en cierta medida me pusieron peros, ya sea por la cantidad de hojas, o porque al exportar el archivo, subía a más de 70 MB en su peso final, o no cambiaba el peso (se mantenía en 6 MB), pero como exportar tomó mucho tiempo, el archivo final siempre aparecía en blanco. 

Entonces, investigando si el maravilloso software R y la IDE RStudio podían hacer algo con los pdf, me topé con que existían los paquetes qpdf y pdftools. **Basta con decir que cuando creé el documento quitando las páginas que sobraban, el procedimiento tomó segundos, conservó el resto del contenido original y el peso del archivo no cambió.** E indagando más en la documentación de estos paquetes y con las IA, decidí crear esta guía para todo aquel que quiera usar y editar documentos PDF empleando R.

## Paqueterías

```{r}
install.packages("qpdf") #Para manipular páginas (rotar, unir, separar, recortar, comprimir)
install.packages("pdftools") #Lee el contenido (texto, metadatos, fuentes y convierte páginas a imagen)
library(qpdf) #para cargar el paquete
library(pdftools) #para cargar el paquete
```

Para descargar [Ghostscript](https://ghostscript.com/releases/gsdnld.html)

## Referencias
-  Artifex Software. (2026). Ghostscript (Versión 10.08.0) [Software]. https://www.ghostscript.com
-  Ooms, J. (2025). qpdf: Split, Combine and Compress PDF Files (Versión 1.4.1) [Software]. https://doi.org/10.32614/CRAN.package.qpdf
-  Ooms, J. (2026). pdftools: Text Extraction, Rendering and Converting of PDF Documents (Versión 3.9.1) [Software]. https://doi.org/10.32614/CRAN.package.pdftools
-  Posit team. (2026). RStudio: Integrated Development Environment for R [Software]. Posit Software, PBC. http://www.posit.co/
-  R Core Team. (2026). R: A Language and Environment for Statistical Computing [Software]. R Foundation for Statistical Computing. https://www.R-project.org/
