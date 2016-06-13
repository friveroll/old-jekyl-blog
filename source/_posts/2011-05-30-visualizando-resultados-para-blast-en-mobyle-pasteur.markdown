---
layout: post
title: "Visualizando resultados para Blast en Mobyle@Pasteur"
date: 2011-05-30 00:00
comments: true
categories: [blast, proteínas, bioinformática, bioquímica]
---

Brevemente, BLAST (**B**asic **L**ocal **A**lignment **S**earch **T**ool) es un método de búsqueda por homología, en el cuál se reta a la base de datos con una secuencia problema (query), para que encuentre secuencias relacionadas a nuestra secuencia problema.

Los resultados que BLAST arroja, son alineamientos pareados junto con los datos de la posición de la secuencia problema (*query*) con la secuencia que el programa encontró de la base de datos.

Uno de los problemas para hacer un alineamiento múltiple de las secuencias que encontramos en BLAST, es que los resultados solo arrojan links a las secuencias que nos interesan, de modo que hay que recuperar las secuencias una por una y además al hacer esto obtenemos la secuencia completa con residuos adicionales que no corresponden a la región que nos interesa (*match*) y por tanto obtenemos secuencias con una longitud distinta, lo cuál no es muy deseable para un alineamiento múltiple.

Así que si queremos visualizar los datos en forma de un alineamiento múltiple o generar archivos fasta con las secuencias alineadas, podemos utilizar MView el cual podemos descargar e instalar localmente en una maquina con linux, o también lo podemos utilizar en el portal [Mobyle@pasteur](http://mobyle.pasteur.fr).

Para hacer este análisis pueden seguirse los siguientes pasos:

- Ir a [Mobyle@pasteur](http://mobyle.pasteur.fr).
- En la pestaña program seleccionamos, database>homology>blast2
<img src="{{ root_url }}/images/blast_1.png" />
- Ahora en la interfase web de blast2, seleccionamos como en la imagen: 
<img src="{{ root_url }}/images/blast_2.png" />- Blast program: __blastp__
- Proteín db: __uniprot_sb__
- En la sección _query sequence/query_, para cargar la secuencia de ejemplo en la base de datos seleccionamos DB, después en la lista desplegable de abajo seleccionamos la base de datos uniprot y en el cuadro diálogo escribimos P25044 y damos click en _Select_.
<img src="{{ root_url }}/images/blast_3.png" />
- Ahora el portal nos mostrará esta secuencia en el cuadro de diálogo más grande.
<img src="{{ root_url }}/images/blast_4.png" />
- Ahora, vamos hacia la parte de arriba de la ventana y damos click en _Run_.
<img src="{{ root_url }}/images/blast_5.png" />
- Y ahora el portal nos muestra los resultados.
<img src="{{ root_url }}/images/blast_6.png" />
- Podemos ver que existen tres opciones para visualizar los resultados, como texto, html y de manera visual.
- Seguido de donde están los resultados en texto, hay una lista desplegable seguida del botón _further analysis_.
- Ahora seleccionamos de la lista mview(blast)>Further analysis.
<img src="{{ root_url }}/images/blast_7.png" />
- Enseguida nos aparecerá la interfase web para mview con los resultados de blast, obtenidos anteriormente
<img src="{{ root_url }}/images/blast_8.png" />
- Hay dos opciones que me parecen útiles para dar formato a los resultados de blast, por defecto está seleccionado html, lo que nos mostrará un alineamiento coloreado de la secuencias alineadas en blast. Pero si deseamos seguir trabajando con la secuencia, tenemos que obtener un archivo fasta, con todas las secuencias alineadas. Claro que también como podrán darse cuenta, hay muchas opciones, para poder filtrar las secuancias que queremos obtener, de momento solo vamos a usar otro programa para ver los resultados.
- Seleccionamos _Pearson/FASTA_ en el menú desplegable de la sección _Output format (-out)_ 
<img src="{{ root_url }}/images/blast_9.png" />
- Y damos click en _Run_.
- Ahora podemos ver como resultado un archivo con formato fasta de las secuencias.
<img src="{{ root_url }}/images/blast_10.png" />
- De aqui, podemos seguir haciendo análisis filogenéticos u obtener estadísticas sobre el alineamiento, pero en este ejemplo, vamos a reformatear estos resultados con un programa de la suite __EMBOSS__, llamado __showalign__.
- Similar a lo que hicimos para mandar los resultados de blast a mview, ahora vamos a seleccionar showalign(sequence).
<img src="{{ root_url }}/images/blast_11.png" />
<img src="{{ root_url }}/images/blast_12.png" />
- Utilizando __advanced options__ podemos seleccionar varias opciones para como queremos visualizar el alineamiento, como por ejemplo la scoring matrix y como queremos ver los residuos que no son idénticos
<img src="{{ root_url }}/images/blast_13.png" />
<img src="{{ root_url }}/images/blast_14.png" />
- Por ejemplo podemos mostrar en los resultados los residuos similares y también ordenarlos de acuerdo a su similaridad con estas opciones
<img src="{{ root_url }}/images/blast_15.png" />
- Para obtener el siguiente resultado:
<img src="{{ root_url }}/images/blast_16.png" />

{% bibliography --file 20110530 %}