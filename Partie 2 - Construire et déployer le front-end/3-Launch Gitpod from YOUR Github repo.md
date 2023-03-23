[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/)

✅ -Configurer et utiliser `astra-cli`

1- Configurer la CLI

Exécutez ce qui suit dans le terminal Gitpod et,
lorsque vous y êtes invité, entrez le `AstraCS:...` que vous avez obtenu au début.

``` bash
astra setup
```
![image](https://user-images.githubusercontent.com/123748165/227347551-6af53722-c505-46d5-a7a3-19231d0b5f82.png)


2- Chargement de données en masse/
>hargez un grand ensemble de données vidéo dans la base de données.
>Cette commande installe et lance correctement l'outil `DSBulk` ([docs](https://docs.datastax.com/en/dsbulk/docs/dsbulkAbout.html)) :

``` bash
astra db load workshops \
  -url data/movies_by_genre.csv \
  -k netflix \
  -t movies_by_genre
```
![image](https://user-images.githubusercontent.com/123748165/227348141-cc6389a1-5c94-437e-927d-2d64958ae973.png)


> *Remarque* : nous nous moquons des bandes-annonces de ces milliers de films en utilisant une poignée
> d'eux encore et encore. Ne soyez pas surpris si vous voyez les mauvaises bandes-annonces
> pour votre film préféré !

