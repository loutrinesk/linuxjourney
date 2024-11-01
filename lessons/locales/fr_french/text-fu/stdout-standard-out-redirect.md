# stdout (Standard Out)

## Contenu de la leçon

À présent, nous nous sommes familiarisés avec des nomreuses commandes ainsi que ce qu'elles renvoient, ce qui nous amène à notre prochain sujet : les flux I/O (entrée/sortie, ou en anglais input/output). Exécutons la commande suivante et nous verrons comment cela fonctionne. 

<pre>$ echo Hello World > peanuts.txt</pre>

Que vient-il de se passer ? Eh bien, vérifiez le répertoire dans lequel vous avez exécuté cette commande et voilà, vous devriez voir un fichier appelé peanuts.txt, regardez à l'intérieur de ce fichier et vous devriez voir le texte Hello World. Beaucoup de choses se sont produites en une seule commande, alors décomposons-les.

Analysons d'abord la première partie : 

<pre>$ echo Hello World</pre>

Nous savons que cela affiche Hello World à l'écran, mais comment ? Les processus utilisent des flux d’I/O pour recevoir des entrées et renvoyer des sorties. Par défaut, la commande echo prend l'entrée (entrée standard ou stdin) du clavier et renvoie la sortie (sortie standard ou stdout) à l'écran. C'est pourquoi lorsque vous tapez echo Hello World dans votre shell, vous obtenez Hello World à l'écran. Cependant, la redirection d'entrée/sortie nous permet de modifier ce comportement par défaut, nous offrant ainsi une plus grande flexibilité avec les fichiers.

Passons maintenant à la deuxième partie de la commande : 

<pre> > </pre>

Le symbole > est un opérateur de redirection qui nous permet de changer l'emplacement de la sortie standard. Il nous permet d'envoyer la sortie de echo Hello World vers un fichier au lieu de l'écran. Si le fichier n'existe pas déjà, il sera créé pour nous. Cependant, s'il existe, il sera écrasé (vous pouvez ajouter un paramètre de shell pour éviter cela, selon le shell que vous utilisez).

Et c'est essentiellement ainsi que fonctionne la redirection de stdout !

Eh bien, disons que je ne voulais pas écraser mon fichier peanuts.txt. Heureusement, il existe aussi un opérateur de redirection pour cela, >>.

<pre>$ echo Hello World >> peanuts.txt</pre>

Cela ajoutera "Hello World" à la fin du fichier peanuts.txt. Si le fichier n'existe pas déjà, il sera créé pour nous, tout comme avec l'opérateur de redirection >.


## Exercice

Essayez ces quelques commandes : 

<pre>
$ ls -l /var/log > myoutput.txt
$ echo Hello World > rm
$ > somefile.txt 
</pre>

## Question du Quiz 

Quel opérateur de redirection utilisez-vous pour ajouter une sortie à un fichier ?

## Réponse du Quiz

>>