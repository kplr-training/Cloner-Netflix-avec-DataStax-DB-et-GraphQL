## 5. Insérer des données de genre avec GraphQL

1.Allez à la fenetre `graphql`,Remplacez `system` par `netflix`

![image](https://user-images.githubusercontent.com/123748165/227166707-0d6700c3-8bee-476c-80f2-d3444833f45d.png)

2- Modifiez `HTTP HEADER`,Integrez votre `TOKEN` dans `x-cassandra-token`.

![image](https://user-images.githubusercontent.com/123748165/227175185-d60e2ed6-3cfb-4fd1-a66b-9f10231fcf84.png)

3- Dans le GraphQL Playground, exécutez la mutation qui écrit les données de genre :

✅Copiez la mutation suivante dans le panneau de gauche :

```yaml
mutation insertGenres {
  action: insertreference_list(value: {label:"genre", value:"Action"}) {
    value{value}
  }
  anime: insertreference_list(value: {label:"genre", value:"Anime"}) {
     value{value}
  }
  award: insertreference_list(value: {label:"genre", value:"Award-Winning"}) {
     value{value}
  }
  children: insertreference_list(value: {label:"genre", value:"Children & Family"}) {
     value{value}
  }
  classic: insertreference_list(value: {label:"genre", value:"Classic"}) {
     value{value}
  } 
  comedies: insertreference_list(value: {label:"genre", value:"Comedies"}) {
     value{value}
  }
  crime: insertreference_list(value: {label:"genre", value:"Crime"}) {
     value{value}
  } 
  cult: insertreference_list(value: {label:"genre", value:"Cult"}) {
     value{value}
  }  
  documentaries: insertreference_list(value: {label:"genre", value:"Documentaries"}) {
     value{value}
  }
  drama: insertreference_list(value: {label:"genre", value:"Dramas"}) {
     value{value}
  }
  fantasy: insertreference_list(value: {label:"genre", value:"Fantasy"}) {
     value{value}
  }
  french: insertreference_list(value: {label:"genre", value:"French"}) {
     value{value}
  }
  horror: insertreference_list(value: {label:"genre", value:"Horror"}) {
     value{value}
  }
  independent: insertreference_list(value: {label:"genre", value:"Independent"}) {
     value{value}
  }
  international: insertreference_list(value: {label:"genre", value:"International"}) {
     value{value}
  } 
  italian: insertreference_list(value: {label:"genre", value:"Italian"}) {
     value{value}
  } 
  musicmusicals: insertreference_list(value: {label:"genre", value:"Music & Musicals"}) {
     value{value}
  } 
  realitytv: insertreference_list(value: {label:"genre", value:"Reality TV"}) {
     value{value}
  } 
  romance: insertreference_list(value: {label:"genre", value:"Romance"}) {
     value{value}
  }
  scifi: insertreference_list(value: {label:"genre", value:"Sci-Fi"}) {
     value{value}
  }
  thriller: insertreference_list(value: {label:"genre", value:"Thriller"}) {
     value{value}
  } 
  tvshow: insertreference_list(value: {label:"genre", value:"TV Show"}) {
     value{value}
  } 
}
```


4-Puis cliquez sur la grosse flèche "play button" au centre pour exécuter la mutation

![image](https://user-images.githubusercontent.com/123748165/227216035-68648861-140d-4641-a424-1ba306828e43.png)

5-Dans GraphQL Playground, ne changez pas l'onglet du terrain de jeu (restez sur le second : `graphql`, ouais) exécutez la requête suivante pour lire la colonne "valeur" de toutes les lignes du tableau :

```yaml
query getAllGenres {
    reference_list (value: {label:"genre"}) {
      values {
      	value
      }
    }
}

```

![image](https://user-images.githubusercontent.com/123748165/227217240-ce7bdf5e-c4d2-4ff9-9b5f-fef70fb98af3.png)

