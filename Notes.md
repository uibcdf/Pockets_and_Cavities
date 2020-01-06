# Pockets

## Whats a pocket and whats not.

- Convex parts of a protein (sometimes removed, not pockets)
- Clefts and cavities
- Surface pockets (opened)?
- Occluded cavities
- pocket and cavity is the same?
- pocket mouth opening

Medium size proteins have 10 to 20 pockets or cavities (será verdad? podemos hacer un barrido del protein data bank? Podemos hacer una gráfica del número de pockets por tamaño? sólo para globulares -sin canales-?) Se pueden clasificar las proteinas por el pocketoma? podemos hacer grupos de proteinas según el número y tamaño de pockets o cavidades?

### Whats a binding site?
binding sites are pockets with 1 or 2 mouth openings, menos frecuentemente son las cavidades.
Suelen tener un tamaño de entre 100-1000 A2 (hay paper de esto?). Hay correlación entre el número de cavidades y pockets y el tamaño, pero no entre el número de binding sites. Ligand volume and binding site volume are correlated when binding site volume is less than 700 A3, but the lignad sheldom occupies the entire site (todo esto donde está reportado?). Auxiliary pockets near the binding site can be used as binding surfaces ([ver](https://www.nature.com/articles/nsb0194-55)).

- Cual será el efecto de los binding pockets proximos a un binding site. Y su topología? la topología de los poquets.. la relación entre sus ubicaciones y sus tamaños. Se puede decir algo a traves de los modos normales de sus deformaciones?

- Otra discusión interesante puede ser la diferencia entre sustratos e inhibidores (ok, su función es cláramente diferente, pero se puede predecir estructuralmente?).

Qué pedimos:
- tight binding (depende de la situación... si son inhibidores puede que si. Pero puede haber contextos en los que queramos liberar el hueco despues de cierto tiempo)
- espcificidad
- balance entalpia y entropia entre el hueco solvatado y ocupado por el ligando

Hay inhibidores lejos del sitio del sustrato, podría hacerse un estudio del pdb sobre esto? ([ver](https://www.sciencedirect.com/science/article/pii/0022283691800745)).

General correlations between binding pockets, flexibility of the aminoacid residues and water molecules could be essential to unravel the essential constituents of a binding site. (hay algo hecho a este respecto?)

### Properties

- Burial Count
- Size
- Volume
- Area
- Depth
- Shape (how?)
- Shallowness (see: Kawabata2007)
- Pocket mouth opening: area and circumference (y si es un canal? detectamos las dos bocas?)
- Atoms lining the pocket


## Types of pockets

## What for?

- initial step in protein structure-based ligand design
- Allosteric pockets
- Protein-protein inhibition or reinforcement
- Ligand pockets
- Pocketome?

## Tasks working with pockets

- Pocket detection and identification
- Pocket classification in order to identify drugable pockets
- Pocket analysis (change of shape)
- Pocket encryption
- Pocket visualization

## Pocket identification

- Pure geometric analysis
- Energy calculations
    - Chemical Probes

### According to the detection algorithm

- Grid-based
- Grid-free
    - Probe spheres
    - Voronoi 

#### Grid-based

- [POCKET](https://www.sciencedirect.com/science/article/abs/pii/026378559280074N) (1992)
- [LigSite](https://www.sciencedirect.com/science/article/abs/pii/S1093326398000023) (1997)
- [Pocket-Picker](https://link.springer.com/article/10.1186%2F1752-153X-1-7) (2007)
- [Q-SiteFinder](https://academic.oup.com/bioinformatics/article/21/9/1908/409213) (2005) -chemical probes-
- [PocketFinder](https://www.mcponline.org/content/4/6/752.long) (2005) -chemical probes-

#### Grid-free

- [SURFNET](https://www.sciencedirect.com/science/article/abs/pii/0263785595000739)(1995) and [SURFNET-ConSurf](https://onlinelibrary.wiley.com/doi/abs/10.1002/prot.20769) (2005)
- [PASS](https://link.springer.com/article/10.1023%2FA%3A1008124202956) (2000)
- [SCREEN](https://onlinelibrary.wiley.com/doi/abs/10.1002/prot.20897) (2006)
- [PHECOM](https://onlinelibrary.wiley.com/doi/abs/10.1002/prot.21283) (2007)
- [CAST](https://onlinelibrary.wiley.com/doi/abs/10.1002/pro.5560070905) (1998) y [CASTp](https://academic.oup.com/nar/article/46/W1/W363/5026264) (2018)
- [APROPOS](https://www.sciencedirect.com/science/article/pii/S0022283696900777) (1996)
- [SiteFinder](https://www.chemcomp.com) (-)
- [Fpocket](https://bmcbioinformatics.biomedcentral.com/articles/10.1186/1471-2105-10-168) (2009)
- []() ()

### Voronoi diagrams and Alpha Spheres

Ver notebook voronoi diagramas and alpha spheres...

Ver Kim2008, Site Finder (Hay literatura?)

#### Alpha Spheres

A sphere that contacts four atoms and contains no atoms inside. By definition, the center of the sphere is at the same distance of every contacted atom (sphere radius).

Four atoms in a plane ---> infinite radius

Large radii spheres ---> exterior surface of the protein

Small radii spheres ---> inter-atoms space (radii comparable to VDW radii)

Relationship alpha sphare -- Voronoi decomposition: the center of alpha spheres are voronoi vertices.

Los pockets de ligandos probablemente son clusters de esferas con una distribución caracteristica de radios de esferas, lo mismo debe pasar seguramente con los grooves, clefts, etc. **Mirar si no está hecho esto... la caracterización de los clusters de esferas según la distribución de los radios**

### Ranking cavities and Scoring functions and Descriptors

### Testing Data Sets and Benchmarking

- [CAST](https://onlinelibrary.wiley.com/doi/abs/10.1002/pro.5560070905) (1998), 100 proteins.

### Web servers and available software

| Algorithm | Web Server | Free Academic Use | Open Source | Commercial | Yet Available | Yet Mantained |
| --------- | :--------: | :---------------: | :---------: | :--------: | :-----------: | :-----------: |
| Q-SiteFinder | Y |  | | | N | N |
| Pocket-Finder | Y | Y | N | | Y | |
| CASTp | Y | Y* | N | | Y | |
| CAST | N | 
| Pocket Picker | N | Y* | Y | | | |
| Fpocket | N | Y* | Y | | | |
| LigSite csc | N | Y* | Y | | N (creo) | N |
| MetaPocket | Y | | | | | |


*: With out restrictions

Python: Pocket Picker (PyMOL, not available yet), alphaspace (not available), KVFinder

## Why this problem has not been solved once and for all?

## Why OpenPocket?

- Available free tool for any one.
- Faster development and inclusion of new features: methods, scoring functions, attributes, descriptors...
- Development of protocols and approaches more complex (easy to use it as module in other working flows).
- Flexibility and adaptability.
- Probably not every algorithm works for every scenario: the search for catalytic site pockets might differ from the search for protein-protein interaction effectors or carbohydrate-protein binding sites.
- Easy to use on molecular dynamics trajectories
- Easy to couple with pocket analysis software (open source)
- Use of collective manpower and intelligence to improve the tool


## Other sources

### Software and servers lists

https://www.researchgate.net/post/How_to_find_out_the_binding_sites_in_a_given_protein   
https://opensourcemolecularmodeling.github.io/#pocket-detection    



```python

```
