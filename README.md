---
output:
  html_document: default
  pdf_document: default
---

# Arbol filogenético de Prunus con gen ortólogo *rbcL*

![generado por FigTree](C:\Users\Usuario\Desktop\proyectofinal24\results\Imag.png?raw=true "Filogenia")

![*Prunus persica*](https://upload.wikimedia.org/wikipedia/commons/d/de/Illustration_Prunus_persica0.jpg)


## Preguntas sobre el proyecto


1.¿Que tipo de datos quieres utilizar?

Se utilizarán datos del gen rbcL para el género Prunus, descargados de la base de datos NCBI bajo los filtros de "protein-coding" y "RefSeq", de los cuales, al día de hoy 25/06/2024, se generaron 81 resultados. De estos, se escogieron 20 para trabajar junto con un grupo externo perteneciente al género Rubus.

¿En qué formato están tus datos?

Todos los datos se encuentran en formato FASTA. El dataset fue descargado en formato de secuencias proteicas (FASTA), alineados con MUSCLE, procesados por IQ-TREE y visualizados en FigTree al estar en formato treefile.

¿Qué quisieras hacer con estos datos?

Con una filogenia de Prunus basada en el gen ortólogo rbcL, se pueden determinar relaciones evolutivas entre las especies, estudiar patrones de diversificación, reconstruir ancestros comunes y comparar con otros géneros de la familia Rosaceae. Además, se pueden identificar eventos de hibridación, realizar estudios de conservación, análisis biogeográficos y explorar adaptaciones específicas de las especies.

### Prerequisites

GIT BASH
FigTree
IQTREE

En el siguiente link se encuentra toda la informacion nescesaria para descargar los programas usados en este proyecto
```
https://carpentries.github.io/workshop-template/install_instructions/#shell
```

### Procesamiento 

####NCBI
Primero se descargaron los datos de NCBI. Para este proyecto en particular se escogieron 20 datos de los resultados filtrados al buscar Prunus con "protein-coding" y "RefSeq". Se descargaron las secuencias proteicas, de las cuales se utilizaron los archivos con terminación *.faa* 

####Sublime Text

Una vez descargados los archivos, se colocan en una carpeta nueva, la cual llamaremos DatosProteinas/. En Sublime Text se abre la carpeta y se copian los documentos a un solo archivo. Una vez realizado esto, se editarán los nombres de la primera fila de manera que solo quede la especie con la que se está trabajando:

```
>Prunus_persica
```

Para esto se utilizará esta serie de comandos en Find y Replace:

FIND
```
\w+.\w\s\w+\s.\w+.(\w+\s\w+.)\w+.*
```
REPLACE
```
\1_\2
```
####MUSCLE
MUSCLE es un programa de alineación de secuencias que puede alinear hasta 500 secuencias y no puede superar más de 1MB por archivo. Introduciremos el documento FASTA con las secuencias ya modificadas en su nombre y pediremos que el archivo que se genere sea titulado PrunusAligned y sea en formato FASTA.

Aquí está el enlace para acceder al programa:
```
https://www.ebi.ac.uk/jdispatcher/msa/muscle
```
####IQTREE
Para manejar IQ-TREE primero se debe descargar la versión más actualizada:
```
https://github.com/iqtree/iqtree2/releases/download/v2.2.0/iqtree-2.2.0-Linux.tar.gz
```
Puedes utilizar esta línea de comandos en GIT:

```
wget https://github.com/iqtree/iqtree2/releases/download/v2.2.0/iqtree-2.2.0-Linux.tar.gz
tar -xzvf iqtree-2.2.0-Linux.tar.gz && rm iqtree-2.2.0-Linux.tar.gz
export PATH=$PATH:$TOOLS_DIR/iqtree-2.2.0-Linux/bin/
```

Asegúrate de crear un path o estar en el mismo nivel de iqtree2:

```
srun iqtree2 -s PrunusAligned -B 1000
```
####FigTree
Entre los archivos resultantes se utiliza el que tiene terminacion en *.treefile* y en el programa se modifica el aspecto que se quiera dar a la filogenia



## Authors

**Natasha Albán** - *Initial work* - [KNVAx]( https://github.com/KNVAx)


## Acknowledgments

No es mucho, pero es trabajo honesto 

