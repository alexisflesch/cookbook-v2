# A fancy cookbook class for LaTeX


Below is a screeshot of what you can do with this style file:

![screenshot](/files/shortbreads.png)

## Introduction

You can find here a style file to write a cook book in LATEX. It's a simple modification of [cookybooky](https://ctan.org/tex-archive/macros/latex/contrib/cookybooky) that works with **TikZ** instead of pstricks.

The cookybooky class is distributed under the [LPPL](https://www.latex-project.org/lppl/), as is this modification.

## An example

The LaTeX class will deal with odd and even pages in a different manner. Fat, protein and carbs are calculated automatically. Take a look at **calories.sty** if you need to add ingredients.

**For some reason I can't put my hand on the modified version of livrerecettes.sty with the bargraphs, I'm leaving the visual here in case I find the time to re-implement it.**

Here is the code for the recipe above:

```latex
\index{nom}{Shortbread}
\index{cat}{Desserts!shortbread}
\recette{Shortbread}
\temps{15 minutes}{30 minutes}

\ingredients{
\item \sucre{100}
\item \beurredemisel{200}
\item \farine{300}
}

\preparation{
\init Mettre le beurre coupé en morceaux dans le bol du Kitchenaid. Ajouter la farine tamisée et
mettre le batteur plat à vitesse minimale.
\init Ajouter le sucre et pétrir à vitesse 2-4 jusqu'à ce que la pâte soit homogène.
\init Faire une boule à la main et l'étaler sur une épaisseur d'un peu moins de 1cm.
\init Découper au couteau et enfourner sur du papier cuisson à 150\degrees pendant 30 minutes.
}

\attention{Les biscuits sont mous à la sortie du four : c'est normal !}
```

This recipe in then added to the main file with the macro below where the arguments are:
* the recipe file (the one given above)
* the small image
* the big image
```latex
\ajoute{recettes/patisserie/ShortBread}{shortbread}{beurre}
```

## A (in)complete recipe book

If you want, you can find a sub-folder in the **files** folder with my cookbook. I had to remove all of the recipes (except the one shown here) for copyright reasons. Still, it should leave you with enough to start your own cookbook. Plus, the code is "calories"-compatible, meaning that if I ever update the style file, the bargraphes will show automatically.
