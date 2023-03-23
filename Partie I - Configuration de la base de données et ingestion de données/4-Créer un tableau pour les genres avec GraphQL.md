# 3. Créer un tableau pour les genres avec GraphQL

✅ **Étape 3 :** Ouvrez **GraphQL Playground** :

0. Assurez-vous d'être connecté à votre compte [DataStax](https://astra.datastax.com)
1. Cliquez sur la base de données **`workshops`** à gauche (développez la liste si nécessaire).

![image](https://user-images.githubusercontent.com/123748165/226287438-c3bb0d6e-b1ec-43db-99cc-22cb360224d0.png)

2.Cliquez sur l'onglet **`Connecter`**.

![image](https://user-images.githubusercontent.com/123748165/226287946-ddb07064-8174-4ef3-9e86-5f8317566203.png)

3.Descendre vers le bas de la page, puis cliquez sur la méthode de connexion `APIs`.

4.Assurez-vous que `GraphQL API` est sélectionné.

![image](https://user-images.githubusercontent.com/123748165/226293938-dadc4b28-5231-4059-8065-b9fce5d37bbf.png)

5.Cliquez sur l'onglet **`GraphQL Playground`** ,

![image](https://user-images.githubusercontent.com/123748165/226340102-9a1a9279-d84f-4e72-bb6a-48f290216fc6.png)

✅ **Étape 5 :** Dans GraphQL Playground, créez la table `reference_list` :

6.Allez dans `HTTP HEADER`,Integrez votre `TOKEN` dans `x-cassandra-token`.

![image](https://user-images.githubusercontent.com/123748165/227164820-20813aa8-5662-469c-a7b6-c88d490769a0.png)


2-Copiez la **mutation** suivante dans le panneau de gauche

``` yaml
mutation createReferenceList {
  reference_list : createTable(
    keyspaceName:"netflix",
    tableName:"liste_de_références",
    ifNotExists : vrai
    partitionKeys : [
      { nom : "étiquette", type : {de base : TEXT} }
    ]
    clusteringKeys : [
      { nom : "valeur", type : {basic : TEXT}, ordre : "ASC" }
    ]
  )
}
```

![image](https://user-images.githubusercontent.com/123748165/227172847-635c245d-a9b3-44dd-8040-49d9fdd04038.png)

