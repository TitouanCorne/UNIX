# Cours système Unix/Linux : les commandes utiles

Le cours est disponible ici :  [Système et réseau](https://francoisbrucker.github.io/cours_informatique/cours/syst%C3%A8me-et-r%C3%A9seau/)

## Table des matières

1. [Pêle-mêle de commandes utiles](#section1)
2. [Se connecter à une machine distante](#section2)

## 1. Pêle-mêle de commandes utiles <a id="section1"></a>

```cd path``` pour naviguer d'un emplacement à un autre.

```cd ..``` pour aller dans le répertoire racine.

`echo $HOME` ou `echo ~` pour afficher le répertoire personnel.

`ls` liste les différents fichiers.

`mkdir` crée un répertoire.

`touch` met à jour la date et l'heure de dernière modification et d'accès du fichier à l'heure actuelle, sans modifier son contenu.

`ls -lt | head -n 3` un **pipe** (`|`) redirige la sortie d'une commande vers l'entrée d'une autre commande.

`cp /etc/passwd ${HOME}/temporaire/mot-de-passe` permet de copier le fichier passwd dans le dossier 'temporaire' et de le renommer 'mot-de-passe'.

`rm -r ${HOME}/temporaire` supprime de manière récursive (`-r`) tous les fichiers et sous-répertoires à l'intérieur du répertoire spécifié.

`chmod u=rwx,go= ${HOME}/private` change les permissions d'un dossier.

`echo "monde !" >> ~/hello.txt` : `echo "monde !"` génère le texte "monde !" et `>>` permet d'ajouter le texte en fin du fichier spécifié (*hello.txt* en l'occurence).

`mv [fichier] [destination]` déplace un fichier.

`ln -s [chemin du fichier source] [chemin et nom du lien symbolique]` crée un lien symbolique.

`tr '\n' ' ' < ~/hello.txt > ~/temp.txt && mv ~/temp.txt ~/hello.txt` : cette ligne de commande remplace les sauts de ligne ('\n') par un espace (' ') du fichier hello.txt. Le fichier résultant est appelé *temp.txt*, il vient ensuite écraser le fichier orignal *hello.txt*.

`cat fichier.txt` pour afficher le contenu du fichier texte.

`cat fichier1.txt fichier2.txt > fichier3.txt` pour concaténer deux fichiers.

`cat > nouveau_fichier.txt` permet de taper du texte dans le terminal et de le copier directement dans le fichier texte.

`ps` affiche les informations des processus en cours d'exécution.

`ps aux` (`a` pour montrer les processus lancés par tous les utilisateurs ; `u` pour afficher les infos détaillées comme l'utilisateur, l'utilisation de la mémoire et du CPU ; `x` pour afficher les processus qui n'ont pas de terminal comme les processus de fond).

`ps -ejH` (`e` affiche tous les processus, `j` utilise le format 'jobs' pour lister les informations, `H` affiche la hiérarchie des processus permettant de voir les relations parent-enfant entre eux).

## 2. Se connecter à une machine distante via ssh <a id="section2"></a>

`ssh` : protocole *Secure Shell* qui permet de se connecter à distance à un autre ordinateur (souvent un serveur) et d'y exécuter des commandes en ligne de commande.
