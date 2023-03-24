1-Installer les dépendances :

```bash
npm install
```
![image](https://user-images.githubusercontent.com/123748165/227352510-061fbdbe-8884-4e94-8425-713309def379.png)


2- Démarrez l'application 

```
netlify dev
```

l'application devrait s'afficher automatiquement dans le "navigateur simple" de GitPod.
Notez que dans cette **exécution en mode dev**, tout est local pour votre instance Gitpod :
_les "fonctions sans serveur", notamment, y tournent réellement,
à côté du reste de l'application !_

![image](https://user-images.githubusercontent.com/123748165/227353141-89009ba3-f6a4-46f9-b4a5-6e5855d04818.png)

Vous pouvez copier l'URL trouvée dans le navigateur simple de Gitpod et l'ouvrir dans un nouvel onglet
(de votre vrai navigateur, c'est-à-dire) pour un
meilleure expérience. Mais il est maintenant temps de passer à la phase de déploiement proprement dite.

3-Arrêtez l'exécution du développement avec `Ctrl-C`.

4-Authentification avec Netlify : exécutez

```
netlify login
```
>Ouvurir le lien dans une nouvelle fenetre puis authoriser l'accés.

![image](https://user-images.githubusercontent.com/123748165/227366364-f7825830-4ba9-4f5d-af8c-7d35351ae066.png)

![image](https://user-images.githubusercontent.com/123748165/227355763-f9c049ac-8b7d-4ab0-9813-9d8971a20a6b.png)

5-Associez à votre site Netlify : exécutez

```
netlify link
```

![image](https://user-images.githubusercontent.com/123748165/227360565-15d60107-e17e-483a-ae1e-bb80d7fd835c.png)

4-Déployez en production !
>Injecter des secrets sur le site Netlify

```
netlify env:import .env
```

Maintenant, les fonctionsserveur de Netlify ont la connexion et les paramètres dont ils ont besoin.

5- Sauvegardez vos pmodification dans `Github`.


![image](https://user-images.githubusercontent.com/123748165/227354568-375f1bdb-3ce9-4b8f-bc4a-70547a2bab04.png)

![image](https://user-images.githubusercontent.com/123748165/227354694-923394ab-5686-48a3-afbc-f4234bdc0ddf.png)

![image](https://user-images.githubusercontent.com/123748165/227354854-47c5e3f6-5487-498c-ba0b-ace691b18693.png)


6-Créer l'application

```
netlify build
```

7- Déployez !
```
netlify deploy --prod
```

![image](https://user-images.githubusercontent.com/123748165/227455433-02941926-4d7d-441d-98ed-ea5ad078acc6.png)

8-Visitez votre site.

```
netlify open:site
```



```
       ██╗    ██╗███████╗██╗     ██╗          
       ██║    ██║██╔════╝██║     ██║          
       ██║ █╗ ██║█████╗  ██║     ██║          
       ██║███╗██║██╔══╝  ██║     ██║          
       ╚███╔███╔╝███████╗███████╗███████╗     
        ╚══╝╚══╝ ╚══════╝╚══════╝╚══════╝     
                                              
       ██████╗  ██████╗ ███╗   ██╗███████╗██╗ 
       ██╔══██╗██╔═══██╗████╗  ██║██╔════╝██║ 
       ██║  ██║██║   ██║██╔██╗ ██║█████╗  ██║ 
       ██║  ██║██║   ██║██║╚██╗██║██╔══╝  ╚═╝ 
       ██████╔╝╚██████╔╝██║ ╚████║███████╗██╗ 
       ╚═════╝  ╚═════╝ ╚═╝  ╚═══╝╚══════╝╚═╝ 
```
