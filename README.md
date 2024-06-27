---
output:
  html_document: default
  pdf_document: default
---

# Arbol filogenético de Prunus con gen ortólogo *rbcL*

![AAAA](C:\Users\Usuario\Desktop\proyectofinal24\data\results\Imag.PNG?raw=true "Filogenia")

![*Prunus persica*](https://upload.wikimedia.org/wikipedia/commons/d/de/Illustration_Prunus_persica0.jpg)


## Preguntas sobre el proyecto


1.¿Que tipo de datos quieres utilizar?

Se utilizarán datos del gen rbcL para el género Prunus, descargados de la base de datos NCBI bajo los filtros de "protein-coding" y "RefSeq", de los cuales, al día de hoy 25/06/2024, se generaron 81 resultados. De estos, se escogieron 20 para trabajar junto con un grupo externo perteneciente al género Rubus.

2.¿En que formato estan tus datos?

Todos los datos se encuentran en formato FASTA. El dataset fue descargado en formato de secuencias proteicas (FASTA), alineados con MUSCLE, procesados por IQ-TREE y visualizados en FigTree al estar en formato treefile.

3 ¿Que quisieras hacer con estos datos?

Con una filogenia de Prunus basada en el gen ortólogo rbcL, se pueden determinar relaciones evolutivas entre las especies, estudiar patrones de diversificación, reconstruir ancestros comunes y comparar con otros géneros de la familia Rosaceae. Además, se pueden identificar eventos de hibridación, realizar estudios de conservación, análisis biogeográficos y explorar adaptaciones específicas de las especies.

### Prerequisites

What things you need to install the software and how to install them

GIT BASH
FigTree
IQTREE
```
GITHUB
```

### Installing

A step by step series of examples that tell you how to get a development env running
NCBI
Sublime Text
MUSCLE
IQTREE
FigTree

##Tutorial para descargar GitHub

<iframe src="https://https://www.youtube.com/embed/MAHkItbZD5c?si=bxfTncEMNgxAsDdh"data-external= "1" width="560" height="315"> </iframe> 
<iframe src="<iframe src="https://www.youtube.com/embed/DAflT-GTMk4?si=0hDi9yTkFx-Pgq20&amp"data-external= "1" width="560" height="315"> </iframe> i" data-external= "1" > </iframe>


Say what the step will be

```
Give the example
```

And repeat

```
until finished
```

End with an example of getting some data out of the system or using it for a little demo


### And coding style tests

Explain what these tests test and why
mkdir
git ..

```
Give an example
```
# INSTALLING IQ-TREE
####################

export TOOLS_DIR=/home/userid/tools
cd $TOOLS_DIR
wget https://github.com/iqtree/iqtree2/releases/download/v2.2.0/iqtree-2.2.0-Linux.tar.gz
tar -xzvf iqtree-2.2.0-Linux.tar.gz && rm iqtree-2.2.0-Linux.tar.gz
export PATH=$PATH:$TOOLS_DIR/iqtree-2.2.0-Linux/bin/

##########################
# SET UP PROJECT DIRECTORY
##########################

export PROJ_DIR=/scratch/mt2245/CompGenomicsCourse/fall22/phylo/
mkdir $PROJ_DIR && cd $PROJ_DIR && mkdir ml && cd ml

# Let's move the example data into workdir using symbolic links
ln -s $TOOLS_DIR/iqtree-2.2.0-Linux/example.phy
## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Natasha Albán** - *Initial work* - [KNVAx]( https://github.com/KNVAx)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.


## Acknowledgments

* swcarpentry
* Inspiration
* etc

