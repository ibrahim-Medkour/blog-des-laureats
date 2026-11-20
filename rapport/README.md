# Dossier du Rapport de Projet (`rapport/`)

Ce dossier héberge le rapport technique et académique du projet Blog des Lauréats (Solicode Tanger).

## 1. Organisation modulaire

<<<<<<< HEAD
Le rapport est découpé en chapitres indépendants dans le sous-dossier `chapitres/` pour faciliter la rédaction progressive. Les fichiers portent le numéro de leur position (`1.md`, `2.md`, ..., `25.md`), ce qui fixe l'ordre du rapport sans configuration :

- `1.md` : remerciement.
- `2.md` : table des matières, remplie automatiquement par le script.
- `3.md` : introduction.
- `4.md` et `5.md` : cadrage du besoin (contexte, cahier des charges).
- `6.md` à `9.md` : démarche méthodologique (méthodologie de travail, Scrum, 2TUP, Design Thinking).
- `10.md` : organisation des sprints.
- `11.md` à `15.md` : branche fonctionnelle et analyse fonctionnelle.
- `16.md` à `18.md` : branche technique, stack et architecture.
- `19.md` à `22.md` : prototype, conception, diagramme de classes et maquettes.
- `23.md` et `24.md` : réalisation et interfaces.
- `25.md` : conclusion et perspectives.
=======
Le rapport est découpé en chapitres indépendants dans le sous-dossier `chapitres/` pour faciliter la rédaction progressive. Les fichiers portent le numéro de leur position suivi du titre (`1 - Remerciement.md`, `2 - Table des matières.md`, ..., `19 - Conclusion.md`), ce qui fixe l'ordre du rapport sans configuration :

- `1 - Remerciement.md` : remerciement.
- `2 - Table des matières.md` : table des matières, remplie automatiquement par le script.
- `3 - Introduction.md` : introduction.
- `4 - Contexte du projet.md` et `5 - Cahier des charges.md` : cadrage du besoin.
- `6 - Méthodologie de travail.md` à `8 - Design thinking.md` : démarche méthodologique (méthodologie de travail, Scrum, Design Thinking).
- `9 - Planification.md` : planification du projet.
- `10 - Persona.md` à `13 - Diagramme de cas d’utilisation.md` : analyse fonctionnelle.
- `14 - Conception.md` à `16 - Maquettes.md` : conception, diagramme de classes et maquettes.
- `17 - Réalisation.md` : réalisation, stack technologique et architecture du système.
- `18 - Interfaces.md` : interfaces.
- `19 - Conclusion.md` : conclusion et perspectives.
>>>>>>> 7599b76b0ad3122e442706244587ef70219006e4

Les chapitres encore vides contiennent seulement leur titre de niveau 1 : le script le reprend tel quel.

## 2. Compilation automatique

Le fichier unique consolidé `rapport.md` est généré automatiquement à partir des chapitres à l'aide d'un script Node.js réutilisable sur n'importe quel projet :

- Script : `concat-chapitres.js`
- Commande directe : `node concat-chapitres.js`
- Ou via npm : `npm run build`

Le script ne contient aucune liste de chapitres : il détecte tous les fichiers `.md` du dossier, les trie par ordre naturel du nom (préfixe numérique puis alphabet) et les numérote de 1 à N dans le rapport généré. Les titres sont repris du titre de niveau 1 présent dans le fichier, sinon déduits du nom du fichier.

<<<<<<< HEAD
Les titres sont insérés tels quels, sans numérotation : le fichier `23.md` produit `# Réalisation`, et non `# Chapitre 23 : Réalisation`.
=======
Les titres sont repris du titre de niveau 1 présent dans chaque fichier ; sans titre de niveau 1, le script retire le numéro du nom (`17 - Réalisation.md` devient « Réalisation »).
>>>>>>> 7599b76b0ad3122e442706244587ef70219006e4

La table des matières est elle aussi générée : le chapitre qui contient le marqueur `<!-- SOMMAIRE -->` reçoit à cet endroit la liste des titres de tous les autres chapitres.

Options disponibles :

- `--chapters <dossier>` : dossier des chapitres (`chapitres/` par défaut).
- `--output <fichier>` : fichier généré (`rapport.md` par défaut).
- `--title <texte>` : titre du rapport (`Rapport de Projet` par défaut).
- `--marp` : ajoute l'en-tête Marp au fichier généré.

## 3. Guide de rédaction

- Rédiger ou modifier les chapitres dans le sous-dossier `chapitres/`.
<<<<<<< HEAD
- Pour placer un chapitre à un endroit précis, nommer son fichier avec le numéro d'ordre voulu (`12.md`).
- Chaque fichier commence par son titre de niveau 1 (`# Titre du chapitre`) : ce titre est repris tel quel dans le rapport.
- Le fichier `2.md` ne contient que son titre et le marqueur `<!-- SOMMAIRE -->` : ne pas écrire la liste à la main.
- Lancer le script de compilation après chaque modification pour mettre à jour `rapport.md`.
- Respecter les règles générales : zéro tableau Markdown, liens relatifs et français professionnel.
=======
- Pour placer un chapitre à un endroit précis, nommer son fichier avec le numéro d'ordre et son titre, séparés par un tiret (`10 - Persona.md`).
- Chaque fichier commence par son titre de niveau 1 (`# Titre du chapitre`) : ce titre est repris tel quel dans le rapport.
- Le fichier `2 - Table des matières.md` contient son titre et le marqueur `<!-- SOMMAIRE -->` : ne pas écrire la liste à la main.
- Lancer le script de compilation après chaque modification pour mettre à jour `rapport.md`.
- Respecter les règles générales : zéro tableau Markdown, liens relatifs et français professionnel.
>>>>>>> 7599b76b0ad3122e442706244587ef70219006e4
