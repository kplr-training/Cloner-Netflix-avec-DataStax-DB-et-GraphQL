1-Dans `GraphQL Playground`, ne changez pas l'onglet du terrain de jeu (restez sur le deuxième onglet, `graphql`, ouais) répertoriez les valeurs du tableau avec la commande suivante :

```yaml
query getMovieAction {
  movies_by_genre (
      value: {genre:"Sci-Fi"},
      orderBy: [year_DESC]
  ) {
    values {
      year,
      title,
      duration,
      synopsis,
      thumbnail
    }
  }
}
```

![image](https://user-images.githubusercontent.com/123748165/227240709-4e6c7637-8d6b-49b1-a865-8b550577d55d.png)

2-Activer la pagination :** Sur un petit jeu de données, vous pouvez récupérer toutes les valeurs du tableau en une seule fois ;
>mais en général, pour des raisons de performances ou de réseau, vous aurez besoin d'une pagination. Exécutez une requête similaire à la précédente, 
>mais cette fois en demandant une _taille de page de 2_ :

```yaml
query getMovieActionPag1 {
    movies_by_genre (
        value: {genre:"Sci-Fi"},
        options: {pageSize: 2},
        orderBy: [year_DESC]
    ) {
      values {
        year,
        title,
        duration,
        synopsis,
        thumbnail
      }
    pageState
    }
}
```

![image](https://user-images.githubusercontent.com/123748165/227241094-12300218-fe37-4c9b-90c6-b64faeecbd4c.png)

3-**Récupérez la page suivante :**

>Notez que `pageState` est maintenant également renvoyé. Utilisez-le pour récupérer les 2 éléments suivants (page suivante) :
>modifiez la requête suivante pour remplacer `YOUR_PAGE_STATE` par votre propre valeur de chaîne :

```yaml
query getMovieActionNextPage {
    movies_by_genre (
        value: {genre:"Sci-Fi"},
        options: {pageSize: 2, pageState: "YOUR_PAGE_STATE"},
        orderBy: [year_DESC]
    ) {
      values {
        year,
        title,
        duration,
        synopsis,
        thumbnail
      }
    pageState
    }
}
```

![image](https://user-images.githubusercontent.com/123748165/227242214-0bfc1fd3-9ea6-4d58-b4d5-2551bc0bd632.png)

Si vous essayez de coller la valeur _nouvellement obtenue_ pour `pageState` et relancez la requête, vous obtenez une liste vide et un `pageState` nul en retour. Oh ! Vous aviez déjà fait défiler toutes les lignes :
_c'est ainsi que la pagination signale la fin de la liste complète des résultats._
