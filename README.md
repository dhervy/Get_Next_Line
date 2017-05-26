# Get_Next_Line

Le but est de créer une fonction qui lit une seule ligne à partir d'un descripteur de fichier, en supposant qu'il ne soit pas manipulé entre les appels à la fonction.

Il doit correspondre à un seul fichier source et à un seul header. Il doit pouvoir fonctionner avec plusieurs descripteurs de fichiers a la fois.

## Usage

```c
char *line;

// pour récupérer une seule ligne.
get_next_line(fd, &line);
  ft_putstr(line); // Line contient la premiere ligne du fichier.

// pour lire la totalité du fichier
while (get_next_line(fd, &line)) // Get_Next_Line retourne 1 tant que le fichier n'est pas fini.
{
	// Line contiendra une nouvelle ligne a chaque tour de boucle.
	ft_putstr(line);
}

// Lorsque Get_Next_Line attaindra le END OF FILE il retournera 0.
```

Vous trouverez dans le Header un define permettent de definire le delimitateur.

Exemple:

```c
# define DELIMITE '\n' // retourne une ligne.

# define DELIMITE '.' // retourne une phrase.
...
```

