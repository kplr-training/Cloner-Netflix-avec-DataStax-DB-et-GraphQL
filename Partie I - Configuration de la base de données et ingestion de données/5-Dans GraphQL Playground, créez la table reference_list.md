✅ **Étape 5 :** Dans GraphQL Playground, créez la table `reference_list` :

1-Ouvrir `GraphQL`, puis partir dans la fenétre `graphql-shema`.


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
