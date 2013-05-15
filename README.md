Sty Tex pacquage pour la page de garde du rapport de PFE de l'ISI.
---

Description
----
Un pacquage Tex pour générer la page de garde pour les rapport de PFE de l'ISI, Institut Supérieur d'Informatique (Ariana, TUNISIE). Testé avec LaTeX et PDFLaTeX.

Un grand merci pour M. Sabri BAHRINI pour l'adaptation de la mise en page original (.doc) en Tex.

Installation
----
1. Créez un fichier .tex et l'enregistrer.
2. Copiez/collez le fichier pagedegardeisi.sty à coté du fichier crée précedemment.
3. Ajouter `\usepackage{pagedegardeisi}` en haut de votre document, a coté des autres `\usepackage`.

Utilisation
----
1. Avant `\begin{document}`, ajouter ces lignes:
 - `\option{}`: pour l'option suivis
 - `\prenomnom{}`: pour le prénom suivis du nom, de forme `prenom NOM`
 - `\sujet{}`: pour définir le sujet de votre projet.
 - `\organismedaccueil{}{}`: La première variable est le nom de l'organisme d'accueil et la deuxième est un logo/une image de l'organisme.
 - `\encadrants{}{}`: La première variable est le nom de l'encadrant de l'entreprise et la deuxième est le nom de l'encadrant de l'ISI.
 - `\anneeuniversitaire{}`: L'année universitaire, de forme `AAAA-AAAA`.
2. Ensuite, ajouter `\makepagedegarde` juste après `\begin{document}`.

Exemple
----
```
\documentclass[a4paper,10pt]{report}
\usepackage[utf8]{inputenc}
\usepackage{pagedegardeisi}
% Title Page
% L'option suivis, tel que Systèmes Informatiques et Logiciels:
\option{Systèmes Informatiques et Logiciels}

% Votre prenom suivis du nom en MAJUSCULES de préférences:
\prenomnom{Foulen BEN FOULEN}

% Le sujet de votre projet:
\sujet{Création d'un générateur de pages de garde}

% Le nom ainsi que la photo de l'organisme d'accueil:
\organismedaccueil{ISI}{logoisi.png}

% Le nom de chacun de l'encadrant de l'entreprise et celui de l'ISI:
\encadrants{Someone}{Someone two}

% L'année universitaire, de forme AAAA-AAAA:
\anneeuniversitaire{2012-2013}

\begin{document}
\makepagedegarde
\end{document}```
