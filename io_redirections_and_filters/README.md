exercice 6 : 
- head -n 3 gets the first three lines of the file.
- tail -n 1 retrieves the last line from that output, which is the third line of the file.

exercice 9 :
 > 
means redirect the output from the ls command to create a new file called list. If the file already exists, replace it.

Whereas

 >> 
means redirect the output from the ls command and append it to the file called list If the file doesn't exist then create it.

exercice 10 :
find . -name \*.swp -type f -delete

The -delete option means find will directly delete the matching files. This is the best match to OP's actual question.

Using -type f means find will only process files.

exercice 11

In terms of depths, we can say that you should start at a minimum depth of 1 (that's referring to any directory present in the current directory) but we won't set a maximum since we want it to go as deep as it can.

The option to use is -mindepth and give the number as the attribute. In this case, the attribute will be 1. The command will then look like

wc as a command can be used to count a lot of things include:

Number of lines
Number of words
Number of characters
With this task, we want it to print the total number of lines that were printed out by the find command.

To get the wc command to count number of lines, we need to provide the option -l.

solution: find -mindepth 1 -type d | wc -l

exercice 12 :

ls -t | head
option -t to see the most recently modified/created files
head to display 10

exercice 13 :

sort | uniq
sort without argument prompts input sorts its and pipe it to unique which print unique words

exercice 14 :

grep 'root' /etc/passwd | xargs

Cette partie de la commande recherche toutes les lignes du fichier /etc/passwd qui contiennent le mot "root". grep est un outil très utilisé pour la recherche de motifs dans des fichiers texte.
| (pipe) :

Le pipe prend la sortie de la commande précédente (ici, les lignes trouvées par grep) et l'utilise comme entrée pour la commande suivante.
xargs :

xargs prend les lignes en entrée et les concatène en une seule ligne. Par défaut, il sépare les éléments par des espaces. Cela signifie que toutes les lignes qui contiennent "root" seront affichées en une seule ligne, sans sauts de ligne.

exercice 16 :

--after-context=3 :

Ce paramètre indique à grep d'afficher également 3 lignes qui suivent chaque ligne contenant le motif "root". Cela peut être utile si vous souhaitez voir des informations supplémentaires qui se trouvent juste après l'occurrence du motif.

exercice 17 : 

grep ' ' -v = inverse, exclue les lignes cotenant les caracteres entre ' '

exercice 19 :

tr = remplacer ou supprimer des caracteres
option -d = supprimer

exercice 21 :

rev = inverser input
