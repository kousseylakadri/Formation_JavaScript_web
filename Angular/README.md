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
- 