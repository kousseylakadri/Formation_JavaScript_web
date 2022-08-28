# Formation Open Class Rooms

## Formation Angular
📁 [Premier projet snapface](snapface)
### Créez une nouvelle application

`ng new snapface --style=scss --skip-tests=true`
- nom de notre projet : `snapface`
- Deux flags : `--style=scss --skip-tests=true`
- l'ajout du routing : `non` il sera fait a la main 

### Lancez le serveur de développement

`ng serve`

### Explorez le dossier du projet
#### * La stricture 

- 📁 [src](snapface/src) 
  - 🔖 [index.html](snapface/src/index.html) (le fichier principal de votre projet)
  - 📁 `App`
    - 🔖 [app.component.html](snapface/src/app/app.component.html) supprimer tout pour un new projet
    - 🔖 [app.component.ts](snapface/src/app/app.component.ts) supprimer tout pour un new projet

La balise  `<app-root>`  correspond à AppComponent
#### * La communication entre fichier 
`index.html` ( <app-root></app-root>) -call-> `app.component.ts` - qui call -> `app.component.html`

### Créez un component
`ng generate component face-snap`
- nom du componet : `face-snap` le `-` pour ajouter des majiscules
- pour affichier le contenu de notre componet il faut : 
  - dans le fichier `face-snap.component.ts` capter le nom de `selector` et l'ajouter dans le fichier `app.component.html`

### Ajoutez des données
- initialisation d'une variable sans que `ts` comprenne on lui ajoute un `!` comme suite `titre!: string` dans le fichier `face-snap.component.ts`
- initialisation des variables dans  `ngOnInit()`

### Affichez du contenu avec la string interpolation

- l'affichage est dans le fichier `face-snap.component.html` avec `{{}}` comme `<h1>{{titre}}</h1>`

### Dynamisez des données avec l'attribute binding
- dans le cas ou le type de la valeur dynamique a chaque fois on doit faire l'usage de `[]` pour les atribus comme suite `<img [src]="" [title]="">`

### Ajoutez un peu de style

- Dans le  `<head>`  de  `index.html` pour importer la police Roboto depuis Google Fonts.

### Écoutez le template
- pour ajouter une methode de bouton il faut cree le bouton dans `face-snap.component.html` et ecrire une fonction dans `face-snap.component.ts` avec l'option `On` comme le nom de cette methode `OnAjout`
- Finalement, on appel la methode dans le fichier `face-snap.component.html` comme suite `<button (click) = "OnAjout" >`
  
### Créez une classe FaceSnap (model)
- la creation de la classe `FaceSnap` dans le `face-snap.model.ts ` dans le dossier `models`
- avec un consctructeur et public pour elimiter la redandance 

### Ajoutez des propriétés personnalisées
- pour faire appel ou injecter une propriete de l'exterieur il faut faire appel avec l'object avec `@Input() nomVariable: nomClass`
- l'injection est faite depuis le parent `app.component.ts` comme 

### Ajoutez une propriété optionnelle
- propriété optionnelle il suffi d'ajouter un `?` comme suite : `titre?: string`
- pour afficher ou pas la propriété on etulise `ngIf` 

### Affichez des listes ou tableau
- avec `*ngfor`

### Ajoutez du style dynamique
- avec `ngstyl`
- chaque componet a son propre style