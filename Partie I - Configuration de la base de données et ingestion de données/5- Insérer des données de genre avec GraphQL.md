## 5. Insérer des données de genre avec GraphQL

1.Allez à la fenetre `graphql`,Remplacez `system` par `netflix`

![image](https://user-images.githubusercontent.com/123748165/227166707-0d6700c3-8bee-476c-80f2-d3444833f45d.png)

2- Modifiez `HTTP HEADER`,Integrez votre `TOKEN` dans `x-cassandra-token`.

![image](https://user-images.githubusercontent.com/123748165/227175185-d60e2ed6-3cfb-4fd1-a66b-9f10231fcf84.png)

3- Dans le GraphQL Playground, exécutez la mutation qui écrit les données de genre :

✅Copiez la mutation suivante dans le panneau de gauche :

``` yaml
mutation insertGenres {
  action : insertreference_list(valeur : {étiquette :"genre", valeur :"Action"}) {
    valeur{valeur}
  }
  anime: insertreference_list(value: {label:"genre", value:"Anime"}) {
     valeur{valeur}
  }
  prix : insertreference_list(value : {label:"genre", value:"Award-Winning"}) {
     valeur{valeur}
  }
  enfants : insertreference_list(value : {label :"genre", value:"Enfants et famille"}) {
     valeur{valeur}
  }
  classique : insertreference_list(value : {label :"genre", value:"Classic"}) {
     valeur{valeur}
  }
  comédies : insertreference_list(value : {label :"genre", value:"Comédies"}) {
     valeur{valeur}
  }
  crime : insertreference_list(value : {label:"genre", value:"Crime"}) {
     valeur{valeur}
  }
  culte : insertreference_list(value : {label :"genre", value:"Cult"}) {
     valeur{valeur}
  }  
  documentaires : insertreference_list(value : {label :"genre", value:"Documentaries"}) {
     valeur{valeur}
  }
  drame : insertreference_list(value : {label:"genre", value:"Dramas"}) {
     valeur{valeur}
  }
  fantaisie : insertreference_list(value : {label :"genre", value:"Fantasy"}) {
     valeur{valeur}
  }
  français : insertreference_list(valeur : {étiquette :"genre", valeur :"français"}) {
     valeur{valeur}
  }
  horreur : insertreference_list(value : {label :"genre", value:"Horror"}) {
     valeur{valeur}
  }
  indépendant : insertreference_list(valeur : {étiquette :"genre", valeur :"Indépendant"}) {
     valeur{valeur}
  }
  international : insertreference_list(valeur : {étiquette :"genre", valeur :"International"}) {
     valeur{valeur}
  }
  italien : insertreference_list(valeur : {étiquette :"genre", valeur :"italien"}) {
     valeur{valeur}
  }
  musicmusicals : insertreference_list(value : {label :"genre", value:"Musique et comédies musicales"}) {
     valeur{valeur}
  }
  téléréalité : insertreference_list(value : {label :"genre", value:"Reality TV"}) {
     valeur{valeur}
  }
  romance : insertreference_list(value : {label :"genre", value:"Romance"}) {
     valeur{valeur}
  }
  scifi : insertreference_list(value : {label :"genre", value:"Sci-Fi"}) {
     valeur{valeur}
  }
  thriller : insertreference_list(value : {label :"genre", value:"Thriller"}) {
     valeur{valeur}
  }
  émission de télévision : insertreference_list(value : {label :"genre", value:"TV Show"}) {
     valeur{valeur}
  }
}
```

4-Puis cliquez sur la grosse flèche "play button" au centre pour exécuter la mutation

![image](https://user-images.githubusercontent.com/123748165/227215390-7c0ef514-c98b-4d35-9d2c-1a4671ba58c7.png)
