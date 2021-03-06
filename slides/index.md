 - title : Detecting similar areas of knowledge using Semantic and Data Mining technologies
- description : Thesis presentation in order to obtain the degree of Computer Scientist from the University of Cuenca.
- author : Xavier Sumba
- theme : white
- transition : none

***

### Detecting similar areas of knowledge using Semantic and Data Mining technologies
<div style="font-size:11pt;"><i>Detección de areas similares de conocimiento usando tecnologías semánticas y minería de datos.</i></div>
<br><hr><br>
##### <div style="font-size:18pt;"><a style="color: black;" href="http://cuent.tk">Xavier Sumba</a> / <a style="color: black;" href="https://www.facebook.com/FERNANDO2654?fref=ts">Freddy Sumba</a></div>


<div style="font-size:15pt;"><i>Universidad de Cuenca, Departamento de Ciencias de la Computación, Cuenca, Ecuador.</i></div>


![](images/uc.png)

***

### Introducción

- ¿Quién trabaja en líneas de investigación parecidas?
- ¿Cómo se puede crear una red de investigadores de un área en común, cuando no conocemos si estas existen?
- Obtener sus artículos, conocer revistas en las que fueron aceptados, entre otros.

***

### Problemas comunes

![an alternative text](images/problema.png)

***

### Arquitectura General

![an alternative text](images/platformDiagram.png)

---

### Data Sources

![an alternative text](images/sources.png)

#### Fuentes de datos bibliográficas

<div style="text-align: justify;">Las fuentes utilizadas, contienen información de investigadores y publicaciones científicas. Abarcan diferentes dominios de estudio, por lo que la estructura de los datos varían por cada fuente. Algunas fuentes proveen APIs que permiten la extracción de datos, sin embargo se tienen limitaciones de cuota.</div>

---

### Data Extraction


<p><img src="images/providerImage.png" alt="" style="width:750px;height:460px"></p>
<div style="text-align: justify;">El modelo de datos de la fuente es mapeado a un modelo común basado en la ontología BIBO.</div>

---

### Data Extraction
#### Análisis del modelo.
<div style="text-align: justify;">Ejemplo de diferencia entre atributos de DBLP y el modelo de datos común.</div>

<table style="font-size: large;">
<thead>
<tr class="header">
<th><p>DBLP fields</p></th>
<th><p>Common model fields</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>dblp:primaryElectronicEdition</p></td>
<td><p>bibo:uri</p></td>
</tr>
<tr class="even">
<td><p>dblp:publishedAsPartOf</p></td>
<td><p>dc:isPartOf</p></td>
</tr>
<tr class="odd">
<td><p>dblp:publishedInBook</p></td>
<td><p>dc:publisher</p></td>
</tr>
<tr class="even">
<td><p>dblp:authoredBy</p></td>
<td><p>dc:contributor</p></td>
</tr>
<tr class="odd">
<td><p>dblp:title</p></td>
<td><p>dc:title</p></td>
</tr>
<tr class="even">
<td><p>dblp:pageNumbers</p></td>
<td><p>bibo:numPages</p></td>
</tr>
</tbody>
</table>

' | DBLP fields                   | Common model fields |
' |-------------------------------|---------------------|
' | dblp:primaryElectronicEdition | bibo:uri            |
' | dblp:publishedAsPartOf        | dc:isPartOf         |
' | dblp:publishedInBook          | dc:publisher        |
' | dblp:authoredBy               | dc:contributor      |
' | dblp:title                    | dc:title            |
' | dblp:pageNumbers              | bibo:numPages       |


---

### Data Extraction
<div style="text-align: justify; text-align: center;">Datos extraidos</div>
<p><img src="images/correctPublicationsSource.png" alt="" style="width:900px;height:500px"></p>



---

### Data Enrichment
#### Modelo de datos

<div style="font-size: 80%;">El modelo de datos basado en la ontología BIBO.</div>

<p><img src="images/dataModelCommon.png" alt="" style="width:750px;height:460px"></p>

---

### Data Enrichment
#### Mapeo del modelo de datos

<div style="font-size: 80%;">Integración de grafos.</div>
<p><img src="images/grafos.png" alt="" style="width:900px;height:500px"></p>

---

### Data Enrichment
<div style="font-size: 20px;">Recurso bibliográfico descrito usando la ontología BIBO.</div>
<!-- HTML generated using hilite.me -->
<blockquote style="font-size: 16px !important; text-align: left; border:none !important;width:80% !important" ><font color="#009900"><font color="#000000">&lt;?xml</font>&nbsp;<font color="#000066">version</font>=<font color="#65b249">&quot;1.0&quot;</font>&nbsp;<font color="#000066">encoding</font>=<font color="#65b249">&quot;UTF-8&quot;</font><font color="#000000">?&gt;</font></font><br/>
<font color="#009900"><font color="#000000">&lt;rdf:RDF</font>&nbsp;<font color="#000066">xmlns:rdf</font>=<font color="#65b249">&quot;http://www.w3.org/1999/02/22-rdf-syntax-ns#&quot;</font>&nbsp;</font><br/>
<font color="#009900">&nbsp;&nbsp;&nbsp;&nbsp;<font color="#000066">xmlns:bibo</font>=<font color="#65b249">&quot;http://purl.org/ontology/bibo/&quot;</font>&nbsp;</font><br/>
<font color="#009900">&nbsp;&nbsp;&nbsp;&nbsp;<font color="#000066">xmlns:dc</font>=<font color="#65b249">&quot;http://purl.org/dc/terms/&quot;</font></font><br/>
<font color="#009900">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font color="#000066">xmlns:foaf</font>=<font color="#65b249">&quot;http://xmlns.com/foaf/0.1/&quot;</font></font><br/>
<font color="#009900">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font color="#000066">xmln border:none !important;width:80% !importants:owl</font>=<font color="#65b249">&quot;http://www.w3.org/2002/07/owl#&quot;</font><font color="#000000">&gt;</font></font><br/>
&nbsp;&nbsp;&nbsp;<font color="#009900"><font color="#000000">&lt;bibo:Document</font>&nbsp;<font color="#000066">rdf:about</font>=<font color="#65b249">&quot;http://ucuenca.edu.ec/wkhuska/publication/semantic-annotation-of-restful-&nbsp;services-using-external&quot;</font><font color="#000000">&gt;</font></font><br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font color="#009900"><font color="#000000">&lt;dc:title<font color="#000000">&gt;</font></font></font>Semantic&nbsp;Annonation&nbsp;of&nbsp;RESTful&nbsp;Services&nbsp;Using&nbsp;External&nbsp;Resources.<font color="#009900"><font color="#000000">&lt;/dc:title<font color="#000000">&gt;</font></font></font><br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font color="#009900"><font color="#000000">&lt;foaf:Organization</font>&nbsp;<font color="#000066">rdf:resource</font>=<font color="#65b249">&quot;http://dblp.uni-trier.de/&quot;</font>&nbsp;<font color="#000000">/&gt;</font></font><br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font color="#009900"><font color="#000000">&lt;dc:contributor</font>&nbsp;<font color="#000066">rdf:resource</font>=<font color="#65b249">&quot;http://dblp.dagstuhl.de/peers/s/Saquicela:Victor&quot;</font>&nbsp;<font color="#000000">/&gt;</font></font><br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font color="#009900"><font color="#000000">&lt;dc:contributor</font>&nbsp;<font color="#000066">rdf:resource</font>=<font color="#65b249">&quot;http://dblp.dagstuhl.de/peers/c/Corcho:=Oacute=scar&quot;</font>&nbsp;<font color="#000000">/&gt;</font></font><br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font color="#009900"><font color="#000000">&lt;dc:contributor</font>&nbsp;<font color="#000066">rdf:resource</font>=<font color="#65b249">&quot;http://dblp.dagstuhl.de/peers/b/BL=aacute=zquez:Luis_Manuel_Vilches&quot;</font>&nbsp;<font color="#000000">/&gt;</font></font><br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font color="#009900"><font color="#000000">&lt;owl:sameAs</font>&nbsp;<font color="#000066">rdf:resource</font>=<font color="#65b249">&quot;http://dblp.dagstuhl.de/rec/conf/icwe/SaquicelaVC10&quot;</font>&nbsp;<font color="#000000">/&gt;</font></font><br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font color="#009900"><font color="#000000">&lt;bibo:uri</font>&nbsp;<font color="#000066">rdf:resource</font>=<font color="#65b249">&quot;http://dx.doi.org/10.1007/978-3-642-16985-4_24&quot;</font>&nbsp;<font color="#000000">/&gt;</font></font><br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font color="#009900"><font color="#000000">&lt;bibo:numPages<font color="#000000">&gt;</font></font></font>266-276<font color="#009900"><font color="#000000">&lt;/bibo:numPages<font color="#000000">&gt;</font></font></font><br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font color="#009900"><font color="#000000">&lt;dc:license</font>&nbsp;<font color="#000066">rdf:resource</font>=<font color="#65b249">&quot;http://www.opendatacommons.org/licenses/by/&quot;</font>&nbsp;<font color="#000000">/&gt;</font></font><br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font color="#009900"><font color="#000000">&lt;dc:publisher<font color="#000000">&gt;</font></font></font>ICWE&nbsp;Workshops<font color="#009900"><font color="#000000">&lt;/dc:publisher<font color="#000000">&gt;</font></font></font><br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<font color="#009900"><font color="#000000">&lt;dc:isPartOf</font>&nbsp;<font color="#000066">rdf:resource</font>=<font color="#65b249">&quot;http://dblp.dagstuhl.de/rec/rdf/conf/agile/conf/agile/config/iwce/2010w&quot;</font><font color="#000000">/&gt;</font></font><br/>
&nbsp;&nbsp;&nbsp;<font color="#009900"><font color="#000000">&lt;/bibo:Document<font color="#000000">&gt;</font></font></font><br/>
<font color="#009900"><font color="#000000">&lt;/rdf:RDF<font color="#000000">&gt;</font></font></font></blockquote>

---

### Data Enrichment
#### Desambiguación de autores.

<example style="width:900px;height:600px"></example>
<script type="text/javascript" src="https://d3js.org/d3.v3.min.js"></script>
<script type="text/javascript">
var width = 900,
    height = 600
var svg = d3.select("example").append("svg")
    .attr("width", width)
    .attr("height", height);
var force = d3.layout.force()
    .gravity(.04)
    .charge(-350)
    .linkDistance(200)
    .size([width, height]);
d3.json("images/readme.json", function(error, json) {
  if (error) throw error;
  force
      .nodes(json.nodes)
      .links(json.links)
      .start();
  var link = svg.selectAll(".link")
      .data(json.links)
    .enter().append("line")
      .style("stroke", "#777")
      .style("stroke-width", "3px");
  var node = svg.selectAll(".node")
      .data(json.nodes)
    .enter().append("g")
      .attr("class", "node")
      .call(force.drag);
  node.append("image")
      .attr("class", "circle")
      .attr("xlink:href", function(d) { return "images/"+d.icon; })
      .attr("x", function(d) { if(d.node) {return "-35px";} else {return "-10px";}})
      .attr("y", function(d) { if(d.node) {return "-35px";} else {return "0px";}})
      .attr("width", function(d) { if(d.node) {return "75px";} else {return "35px";}})
      .attr("height", function(d) { if(d.node) {return "75px";} else {return "35px";}});
  node.append("title")
      .text(function(d) { return d.subject; });
  node.append("text")
          .text(function(d) { return d.name; })
          .style("fill", color)
          .style("font-size", function(d) { if(d.node) {return "16px";} else {return "12px";}})
          .attr("x", function(d) { if(d.node) {return "0";} else {return "0";}})
          .attr("y", function(d) { if(d.node) {return "-35";} else {return "-5";}});
    function color(d) {
            return d.node ? "#3182bd" : "#020507";
          }
  force.on("tick", function() {
    link.attr("x1", function(d) { return d.source.x; })
        .attr("y1", function(d) { return d.source.y; })
        .attr("x2", function(d) { return d.target.x; })
        .attr("y2", function(d) { return d.target.y; });
    node.attr("transform", function(d) { return "translate(" + d.x + "," + d.y + ")"; });
  });
});
</script>

---

### Data Enrichment
#### Desambiguación de información.

<div style="font-size: 80%;">Debido a que se obtiene datos de diferentes fuentes bibliogríficas se tiene datos incoherentes o duplicados. Por lo que es necesario utilizar técnicas de desambiguación, en autores y publicaciones.</div>



<p><img src="images/desamibiguacion_a.png" alt=""></p>

---

### Data Enrichment
#### Desambiguación de información.

<p><img src="images/desamibiguacion_b.png" alt=""></p>

---


### Data Enrichment
#### Desambiguación de información.
<div style="font-size: 80%;">Índice de similaridad entre recursos bibliográfico.</div>
<p><img src="images/similaridad.png" alt="" style="width:500px;height:300px"></p>

---

### Pattern Detection
#### Proceso para detección de areas y redes de colaboración

![](images/pdetection.png)


<div style="font-size: 80%; text-align: justify;">
<span style="color: red;">Find groups</span> detectar patrones de los datos almacenados en el repositorio central.

<div class="fragment">
<span style="color: red;">Knowledge Discovery</span> asociar patrones a un formato legible por un humano. Se descubre redes de colaboración y áreas de
conocimiento.
</div>

<div class="fragment">
<span style="color: red;">Label Groups</span> Se encuentra una etiqueta a cada cluster, ayuda a acelerar consultar y mantener la información
organizada en el repositorio.
</div>
<div>

---

### Find Groups

![](images/findgroups.png)

---

### Knowledge Discovery

<table style="width:100%">
  <tr>
    <th style="width: 30%; vertical-align: middle;"><img src="images/fgroups_files.png" alt=""></th>
    <th class="fragment" style="width: 70%"><img src="images/find_groups_process.png" alt=""></th>
  </tr>
</table>

---

# Topic Model + WordNet

<div class="fragment">
# =
# Label
</div>

---
### Topic Model
![](images/lda.png)

[Imagen de *David M. Blei* - Probabilistic Topic Models ](http://www.cs.princeton.edu/~blei/kdd-tutorial.pdf)

' Frecuencia Distribución de palabras/topicos
' Numero de topicos
' Varios documentos a varios topicos

---

### Label Groups

![](images/etiqueta.png)

---

### Datos listos para ser explotados

![](images/export.png)

---

### Resultados

![](images/redes.png)

---

<script type="text/javascript" src="https://www.google.com/jsapi"></script>
<script type="text/javascript">
    google.load("visualization", "1", {packages:["corechart"]})
    google.setOnLoadCallback(drawChart);
function drawChart() {
    var data = new google.visualization.DataTable({"cols": [{"type": "string" ,"id": "Column 1" ,"label": "Column 1" }, {"type": "number" ,"id": "Column 2" ,"label": "Publicaciones" }], "rows" : [{"c" : [{"v": "Carvallo Vega, Juan Pablo"}, {"v": 75}]}, {"c" : [{"v": "Conci, Aura"}, {"v": 72}]}, {"c" : [{"v": "Díaz Contreras, Jessica"}, {"v": 46}]}, {"c" : [{"v": "Vanegas, Pablo"}, {"v": 42}]}, {"c" : [{"v": "Espinoza, Mauricio"}, {"v": 42}]}, {"c" : [{"v": "Saquicela, Víctor"}, {"v": 35}]}, {"c" : [{"v": "Goethals, Peter L. M"}, {"v": 34}]}, {"c" : [{"v": "Castro Riera, Carlos "}, {"v": 31}]}, {"c" : [{"v": "Torres, Maria Eugenia"}, {"v": 30}]}, {"c" : [{"v": "Veronica Mora"}, {"v": 28}]}]});
    var options = {"hAxis":{"title":"Número de publicaciones","viewWindowMode":"explicit","viewWindow":{"min":0}},"legend":{"position":"none"},"title":"Investigadores Relevantes","width":1000,"height":600}
    var chart = new google.visualization.BarChart(document.getElementById('d58646cc-a055-47d1-8d4f-d9a17025c2d1'));
    chart.draw(data, options);
}
</script>
<div id="d58646cc-a055-47d1-8d4f-d9a17025c2d1" style="width: 800px; height: 600px;"></div>

---

<table style="width:100%">
  <tr>
    <th style="width: 35%; vertical-align: middle;">
      <h4 style="text-align: center">Areas Relevantes</h4>
      <img src="images/wordcloud.png" alt="">
    </th>
    <th class="fragment" style="width: 65%">
      <h4>Redes de colaboración</h4>
      <img src="images/colaboracion.png" alt="">
    </th>
  </tr>
</table>

---


# __¿Más?__


[![](images/redi.png)](http://redi.cedia.org.ec/)

***

### Conclusiones

- Procesos como el de desambiguación y etiquetado necesitan un trabajo mas exhaustivo, debido a que aun se tienen ciertas inconsistencias en los resultados.
- Considerar que incluso para una persona es complicado determinar cierta información sobre un investigador o varios investigadores que pueden trabajar en conjunto. Por lo que aun es un reto a nivel computacional.
- Además como resultado se cuenta con un repositorio centralizado y se provee el uso de estos datos a cualquier persona.


***

### Trabajos Futuros

- Incluir el abstract para analizar redes de colaboración.
- Mejorar el proceso de etiquetado.
- Analizar nuevos algoritmos de clustering o otras técnicas para encontrar agrupaciones.

***

<table style="width:100%;">
  <tr>
    <th><h2 style="text-align: center">CLEI 2016</h2></th>
    <th><h2 style="text-align: center">ENTCS</h2></th>
    <th><h2 style="text-align: center">TICAL</h2></th>
  </tr>
  <tr>
    <th style="width: 33%; vertical-align: middle;">
      <img src="images/clei.png" alt="">
    </th>
    <th style="width: 33%; text-align:center; vertical-align: middle;">
      <img src="images/entcs.gif" alt="">
    </th>
    <th style="width: 33%; text-align:center; vertical-align: middle;">
      <img src="images/tical.png" alt="">
    </th>
  </tr>
</table>

***

![](images/cedia.png)

Agradecemos a **CEDIA** por el apoyo brindado durante el transcurso de está investigación.

***

# ¿PREGUNTAS?
