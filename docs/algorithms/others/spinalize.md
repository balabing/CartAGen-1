# Description of the Spinalize Algorithm

> - Date 20/07/2017.
> - Author: [Guillaume Touya][1]
> - Contact {firstname.lastname}@ign.fr.



Description of the algorithm
-------------
The spinalize algorithm collapses a polygon into a line based on a voronoï diagram of the polygon, keeping only the "spine" of the skeleton (the algorithm gets rid of the small edges of the skeleton). 
If several polygons are initially connected (i.e. they touch each other) their spine is also connected by the algorithm.

![A river area spinalized](/images/proc_spinalize.png)

The algorithm is briefly described in two papers that can be found [here][5] and [here][6].

| Parameter name        | Description         				| Type 							| Default value			|
|:----------------------|:----------------------------------|:------------------------------|:--------------------------------------------------|
| lengthMin    | minimum length to keep a segment in the spine of the skeleton 	| double (meters) 			| 								|
| overSample    | a step for the vertex oversampling performed before computing the Voronoï diagram 	| double (meters) 			| 								|
| removeHoles    | true if you want to remove holes prior to collapse 	| boolean 			| 	true							|


Examples of generalization
-------------


When to use the algorithm?
-------------
The algorithm can be used to collapse thin areas into lines (e.g. rivers, hedges, taxiways). When the shapes of the areas are not very thin, or are very complex, the algorithm provides not very smooth lines, and a straight skeleton based collapse should be preferred.


Available variations
-------------



See Also
-------------


[1]: http://recherche.ign.fr/labos/cogit/english/cv.php?prenom=&nom=Touya
[2]: /algorithms/line/visvalingam.md
[3]: /algorithms/line/raposo.md
[4]: /algorithms/line/li_openshaw.md
[5]: http://www.tandfonline.com/doi/abs/10.1080/15230406.2013.809233
[6]: https://kartographie.geo.tu-dresden.de/downloads/ica-gen/workshop2014/genemr2014_submission_6.pdf