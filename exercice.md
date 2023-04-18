On souhaite manipuler une playlist avec un programme en C.

Chaque musique aura la forme suivante

```c
typedef struct _Track Track;
struct Track {
	int id;
	char name[21];
	int like; //boolean donc soit 1 soit 0
	int duration;
	Track* next; //suivant
};
```

## Q1

Écrire une fonction ```new_playlist``` qui a pour paramètres un id, un nom, une durée, et qui créer une nouvelle playlist contenant une seule musique initialisée avec les paramètres (c'est le nom de la musique et non celle de la playlist). Les autres champs de la musique seront initialisés à 0

## Q2

- a) Écrire une fonction ```add_track``` qui ajoute une musique à la playlist, en tête
- b) Écrire une fonction ```add_track_bis``` qui fait pareil mais cette fois ça l'ajoute à la fin
- c) Pareil mais cette fois on l'ajoute à la position pos passé en paramètre

## Q3

Écrire une fonction ```delete_track``` qui supprime la musique ayant un certains id de la playlist

## Q4

Écrire une fonction ```like_track``` qui like ou delike la musique associé à un id de playlist

## Q5

Écrire une fonction ```favorite_track``` qui créer une nouvelle playlist contenant toutes les musiques ayant été like, sans modifier la playlist originelle

## Q6

Écrire une fonction ```find_track_by_name``` qui cherche la musique ayant le nom en paramètre, renvoi l'adresse de cette musique

## Question bonus

Fait un décalage vers la droite de toute les musiques dans la playlist (permutation circulaire avec un pas de 1)
