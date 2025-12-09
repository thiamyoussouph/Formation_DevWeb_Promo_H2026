# 🅰️ Module Angular Framework

Bienvenue dans le **Module 04 - Angular Framework** ! Ce guide complet vous accompagnera pas à pas dans la découverte d'Angular, depuis l'installation jusqu'à la création de votre première application interactive.

---

## 📋 Table des Matières

- [Qu'est-ce qu'Angular ?](#-quest-ce-quangular-)
- [Installation de l'Environnement](#-installation-de-lenvironnement)
- [Installation du CLI Angular](#-installation-du-cli-angular)
- [Créer Votre Premier Projet](#-créer-votre-premier-projet)
- [Comprendre la Structure du Projet](#-comprendre-la-structure-du-projet)
- [Les Composants Angular](#-les-composants-angular)
- [Le Data Binding](#-le-data-binding)
- [Les Directives](#-les-directives)
- [Le Routing](#-le-routing)
- [Les Services](#-les-services)
- [Commandes Essentielles](#-commandes-essentielles)

---

## 🤔 Qu'est-ce qu'Angular ?

Angular est un **framework JavaScript** créé par Google pour développer des applications web modernes. Contrairement au HTML/CSS/JS classique où vous manipulez directement le DOM, Angular vous permet de créer des applications **réactives** et **organisées** grâce à une architecture basée sur les composants.

### Pourquoi utiliser Angular ?

- ✅ **Structure claire** : Votre code est organisé en composants réutilisables
- ✅ **TypeScript** : Un JavaScript amélioré avec la détection d'erreurs avant l'exécution
- ✅ **Réactivité** : L'interface se met à jour automatiquement quand les données changent
- ✅ **Écosystème complet** : Routing, formulaires, HTTP, tout est inclus
- ✅ **Utilisé par de grandes entreprises** : Google, Microsoft, Forbes, etc.

---

## 🛠 Installation de l'Environnement

### Étape 1 : Installer Node.js et npm

Angular a besoin de **Node.js** pour fonctionner. Node.js est un environnement qui permet d'exécuter du JavaScript en dehors du navigateur.

#### 🪟 Windows

1. Allez sur [nodejs.org](https://nodejs.org/fr/download/)
2. Téléchargez la version **LTS** (Long Term Support) - format `.msi`
3. Lancez l'installeur et suivez les étapes (laissez les options par défaut)
4. **Important** : Cochez la case "Automatically install the necessary tools" si proposée

#### 🍎 macOS

**Option 1 : Installeur officiel**
1. Allez sur [nodejs.org](https://nodejs.org/fr/download/)
2. Téléchargez la version **LTS** - format `.pkg`
3. Lancez l'installeur et suivez les instructions

**Option 2 : Avec Homebrew (recommandé si vous l'avez)**
```bash
brew install node
```

#### 🐧 Linux (Ubuntu/Debian)

```bash
# Mise à jour des paquets
sudo apt update

# Installation de Node.js et npm
sudo apt install nodejs npm

# Ou avec la version LTS via NodeSource
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
sudo apt-get install -y nodejs
```

#### ✅ Vérification de l'Installation

Ouvrez votre terminal et tapez :

```bash
node -v
npm -v
```

Vous devriez voir quelque chose comme :
```
v18.17.0
9.8.1
```

> **💡 Ouvrir le Terminal :**
> - **Windows** : Recherchez "cmd" ou "PowerShell" dans le menu Démarrer
> - **macOS** : Appuyez sur `Cmd + Espace`, tapez "Terminal"
> - **Linux** : Appuyez sur `Ctrl + Alt + T`

---

## ⚙️ Installation du CLI Angular

Le **CLI** (Command Line Interface) est l'outil magique d'Angular. Il vous permet de créer des projets, générer des composants, et bien plus encore, avec de simples commandes.

### Installation Globale

#### 🪟 Windows (PowerShell ou CMD)

```bash
npm install -g @angular/cli
```

#### 🍎 macOS / 🐧 Linux

```bash
sudo npm install -g @angular/cli
```

> **📝 Note** : Le flag `-g` installe le CLI de manière **globale** sur votre machine, ce qui vous permet de l'utiliser dans n'importe quel dossier.

### ✅ Vérification

```bash
ng version
```

Vous devriez voir un affichage détaillé avec la version d'Angular CLI installée (ex: Angular CLI: 17.x.x).

### ⚠️ Problèmes Courants

**Windows : "ng n'est pas reconnu..."**
- Fermez et rouvrez votre terminal
- Si le problème persiste, ajoutez manuellement npm au PATH système

**macOS/Linux : "Permission denied"**
- Utilisez `sudo` devant la commande
- Ou configurez npm pour installer sans sudo : [Guide npm](https://docs.npmjs.com/resolving-eacces-permissions-errors-when-installing-packages-globally)

---

## 🚀 Créer Votre Premier Projet

### Étape 1 : Naviguer vers votre Dossier de Travail

Créez d'abord un dossier pour vos projets Angular :

```bash
# Windows
cd C:\Users\VotreNom\Documents
mkdir projets-angular
cd projets-angular

# macOS/Linux
cd ~/Documents
mkdir projets-angular
cd projets-angular
```

### Étape 2 : Créer le Projet

```bash
ng new mon-app-meteo
```

Le CLI vous posera **deux questions importantes** :

#### Question 1 : Would you like to add Angular routing?

```
? Would you like to add Angular routing? (y/N)
```

**Tapez `y` et appuyez sur Entrée**

Le **routing** permet de naviguer entre différentes pages dans votre application (comme aller de la page d'accueil à la page "À propos"). C'est essentiel pour toute application avec plusieurs vues.

#### Question 2 : Which stylesheet format would you like to use?

```
? Which stylesheet format would you like to use?
  CSS
❯ SCSS
  Sass
  Less
```

**Sélectionnez `CSS` et appuyez sur Entrée**

Pour ce module, nous utiliserons du CSS classique que vous connaissez déjà.

### Étape 3 : Attendre l'Installation

Le CLI va maintenant :
1. Créer tous les fichiers nécessaires
2. Installer toutes les dépendances (cela peut prendre 2-5 minutes)
3. Initialiser un repository Git

Vous verrez défiler plein de lignes dans le terminal. **C'est normal !**

```
CREATE mon-app-meteo/README.md (1024 bytes)
CREATE mon-app-meteo/.editorconfig (274 bytes)
CREATE mon-app-meteo/.gitignore (548 bytes)
...
✔ Packages installed successfully.
```

### Étape 4 : Lancer l'Application

```bash
# Entrez dans le dossier du projet
cd mon-app-meteo

# Lancez le serveur de développement
ng serve
```

Vous verrez :
```
** Angular Live Development Server is listening on localhost:4200 **
✔ Browser application bundle generation complete.
```

**Ouvrez votre navigateur** et allez à l'adresse : **http://localhost:4200**

🎉 **Félicitations !** Vous voyez votre première application Angular !

> **💡 Astuce** : Utilisez `ng serve --open` (ou `ng serve -o`) pour ouvrir automatiquement le navigateur.

### Étape 5 : Arrêter le Serveur

Pour arrêter le serveur de développement :
- Appuyez sur `Ctrl + C` dans le terminal
- Tapez `y` si on vous demande confirmation

---

## 📁 Comprendre la Structure du Projet

Voici à quoi ressemble votre nouveau projet :

```
mon-app-meteo/
│
├── src/                          # Code source de votre application
│   ├── app/                      # Dossier principal de l'application
│   │   ├── app.component.ts      # Composant racine (logique)
│   │   ├── app.component.html    # Template HTML du composant racine
│   │   ├── app.component.css     # Styles du composant racine
│   │   ├── app.config.ts         # Configuration de l'application
│   │   └── app.routes.ts         # Configuration des routes
│   │
│   ├── assets/                   # Fichiers statiques (images, fonts, etc.)
│   ├── index.html               # Page HTML principale
│   ├── main.ts                  # Point d'entrée de l'application
│   └── styles.css               # Styles globaux
│
├── node_modules/                # Toutes les dépendances (NE PAS MODIFIER)
├── angular.json                 # Configuration Angular CLI
├── package.json                 # Liste des dépendances npm
├── tsconfig.json                # Configuration TypeScript
└── README.md                    # Documentation du projet
```

### 🔍 Fichiers Importants à Connaître

| Fichier | Rôle |
|:--------|:-----|
| **src/main.ts** | Point de départ de l'application, charge le composant racine |
| **src/index.html** | La page HTML de base (ne touchez presque jamais à ce fichier) |
| **src/app/app.component.ts** | Le premier composant de votre app, le "conteneur principal" |
| **src/app/app.routes.ts** | Définit les URLs de votre application |
| **src/styles.css** | Styles CSS qui s'appliquent partout dans l'app |
| **angular.json** | Configuration générale (ports, chemins, etc.) |
| **package.json** | Liste des bibliothèques installées |

### ⚠️ Dossiers à NE JAMAIS MODIFIER

- **node_modules/** : Contient toutes les dépendances (peut contenir des milliers de fichiers)
- **dist/** : Dossier de compilation (créé quand vous faites `ng build`)

---

## 🧩 Les Composants Angular

Les **composants** sont les briques de base d'Angular. Chaque composant est une partie réutilisable de votre interface.

### Anatomie d'un Composant

Un composant Angular se compose toujours de **3 fichiers** :

```typescript
// mon-composant.component.ts - LA LOGIQUE
import { Component } from '@angular/core';

@Component({
  selector: 'app-mon-composant',        // Nom de la balise HTML
  templateUrl: './mon-composant.component.html',
  styleUrls: ['./mon-composant.component.css']
})
export class MonComposantComponent {
  // Variables (propriétés)
  titre = 'Bonjour Angular !';
  compteur = 0;

  // Méthodes (fonctions)
  incrementer() {
    this.compteur++;
  }
}
```

```html
<!-- mon-composant.component.html - LE TEMPLATE -->
<div class="container">
  <h1>{{ titre }}</h1>
  <p>Compteur : {{ compteur }}</p>
  <button (click)="incrementer()">Cliquez-moi</button>
</div>
```

```css
/* mon-composant.component.css - LES STYLES */
.container {
  padding: 20px;
  background-color: #f0f0f0;
}

button {
  background-color: #007bff;
  color: white;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

button:hover {
  background-color: #0056b3;
}
```

### Créer un Nouveau Composant

```bash
ng generate component meteo-widget

# Ou la version courte :
ng g c meteo-widget
```

Cette commande crée automatiquement :
```
CREATE src/app/meteo-widget/meteo-widget.component.css
CREATE src/app/meteo-widget/meteo-widget.component.html
CREATE src/app/meteo-widget/meteo-widget.component.ts
```

> **✨ Magie du CLI** : Le composant est automatiquement déclaré et prêt à être utilisé !

### Utiliser votre Composant

Dans un autre template, utilisez le selector :

```html
<!-- app.component.html -->
<h1>Mon Application Météo</h1>
<app-meteo-widget></app-meteo-widget>
```

---

## 🔗 Le Data Binding

Le **Data Binding** est la connexion entre votre code TypeScript et votre template HTML.

### 1. Interpolation `{{ }}`

Affiche une variable dans le HTML :

```typescript
// component.ts
export class AppComponent {
  ville = 'Dakar';
  temperature = 28;
}
```

```html
<!-- component.html -->
<p>Il fait {{ temperature }}°C à {{ ville }}</p>
<!-- Résultat : Il fait 28°C à Dakar -->
```

### 2. Property Binding `[propriété]`

Lie une propriété HTML à une variable :

```typescript
// component.ts
export class AppComponent {
  imageUrl = 'assets/soleil.png';
  estDesactive = false;
}
```

```html
<!-- component.html -->
<img [src]="imageUrl" alt="Météo">
<button [disabled]="estDesactive">Cliquez</button>
```

### 3. Event Binding `(événement)`

Réagit aux actions de l'utilisateur :

```typescript
// component.ts
export class AppComponent {
  message = '';

  afficherAlerte() {
    this.message = 'Bouton cliqué !';
  }
}
```

```html
<!-- component.html -->
<button (click)="afficherAlerte()">Cliquez-moi</button>
<p>{{ message }}</p>
```

### 4. Two-Way Binding `[(ngModel)]`

Synchronisation bidirectionnelle (nécessite FormsModule) :

```typescript
// component.ts
import { FormsModule } from '@angular/forms';

export class AppComponent {
  nomUtilisateur = '';
}
```

```html
<!-- component.html -->
<input [(ngModel)]="nomUtilisateur" type="text">
<p>Bonjour {{ nomUtilisateur }} !</p>
<!-- Le paragraphe se met à jour en temps réel ! -->
```

---

## 🎯 Les Directives

Les **directives** sont des instructions spéciales dans le HTML qui modifient le comportement des éléments.

### *ngIf - Affichage Conditionnel

```typescript
// component.ts
export class AppComponent {
  estConnecte = false;
  age = 17;
}
```

```html
<!-- component.html -->
<div *ngIf="estConnecte">
  <p>Bienvenue dans votre espace personnel</p>
</div>

<div *ngIf="!estConnecte">
  <p>Veuillez vous connecter</p>
</div>

<!-- Avec else -->
<div *ngIf="age >= 18; else mineur">
  <p>Vous êtes majeur</p>
</div>
<ng-template #mineur>
  <p>Vous êtes mineur</p>
</ng-template>
```

### *ngFor - Boucles

```typescript
// component.ts
export class AppComponent {
  villes = ['Dakar', 'Paris', 'New York', 'Tokyo'];
  
  produits = [
    { nom: 'Ordinateur', prix: 800 },
    { nom: 'Souris', prix: 20 },
    { nom: 'Clavier', prix: 50 }
  ];
}
```

```html
<!-- component.html -->
<!-- Liste simple -->
<ul>
  <li *ngFor="let ville of villes">{{ ville }}</li>
</ul>

<!-- Liste avec index -->
<ul>
  <li *ngFor="let ville of villes; let i = index">
    {{ i + 1 }}. {{ ville }}
  </li>
</ul>

<!-- Liste d'objets -->
<div *ngFor="let produit of produits">
  <h3>{{ produit.nom }}</h3>
  <p>Prix : {{ produit.prix }}€</p>
</div>
```

### [ngClass] et [ngStyle]

```typescript
// component.ts
export class AppComponent {
  estActif = true;
  temperature = 32;
}
```

```html
<!-- component.html -->
<!-- Ajouter des classes CSS dynamiquement -->
<div [ngClass]="{ 'actif': estActif, 'inactif': !estActif }">
  Status
</div>

<!-- Styles dynamiques -->
<div [ngStyle]="{ 
  'color': temperature > 30 ? 'red' : 'blue',
  'font-size': '20px' 
}">
  Température : {{ temperature }}°C
</div>
```

---

## 🗺️ Le Routing

Le **routing** permet de créer une application avec plusieurs pages sans recharger le navigateur.

### Configuration Basique

Quand vous créez un projet avec `ng new`, le routing est déjà configuré dans `app.routes.ts` :

```typescript
// app.routes.ts
import { Routes } from '@angular/router';
import { AccueilComponent } from './accueil/accueil.component';
import { MeteoComponent } from './meteo/meteo.component';
import { ContactComponent } from './contact/contact.component';

export const routes: Routes = [
  { path: '', component: AccueilComponent },           // Page d'accueil
  { path: 'meteo', component: MeteoComponent },        // /meteo
  { path: 'contact', component: ContactComponent },    // /contact
  { path: '**', redirectTo: '' }                       // Page non trouvée -> accueil
];
```

### Navigation dans le Template

```html
<!-- app.component.html -->
<nav>
  <a routerLink="/">Accueil</a>
  <a routerLink="/meteo">Météo</a>
  <a routerLink="/contact">Contact</a>
</nav>

<!-- Le composant de la route active s'affiche ici -->
<router-outlet></router-outlet>
```

### Navigation Programmée

```typescript
// component.ts
import { Router } from '@angular/router';

export class MonComponent {
  constructor(private router: Router) {}

  allerVersMeteo() {
    this.router.navigate(['/meteo']);
  }
}
```

### Paramètres de Route

```typescript
// app.routes.ts
{ path: 'ville/:nom', component: VilleDetailComponent }
```

```typescript
// ville-detail.component.ts
import { ActivatedRoute } from '@angular/router';

export class VilleDetailComponent {
  nomVille: string = '';

  constructor(private route: ActivatedRoute) {
    this.nomVille = this.route.snapshot.params['nom'];
    // URL: /ville/dakar -> nomVille = 'dakar'
  }
}
```

---

## 🔧 Les Services

Les **services** permettent de partager des données et de la logique entre plusieurs composants.

### Créer un Service

```bash
ng generate service services/meteo

# Ou :
ng g s services/meteo
```

### Exemple de Service

```typescript
// meteo.service.ts
import { Injectable } from '@angular/core';

@Injectable({
  providedIn: 'root'  // Le service est disponible partout
})
export class MeteoService {
  
  private villes = [
    { nom: 'Dakar', temperature: 28, conditions: 'Ensoleillé' },
    { nom: 'Paris', temperature: 15, conditions: 'Nuageux' }
  ];

  // Méthode pour récupérer toutes les villes
  getVilles() {
    return this.villes;
  }

  // Méthode pour récupérer une ville spécifique
  getVille(nom: string) {
    return this.villes.find(v => v.nom === nom);
  }

  // Méthode pour ajouter une ville
  ajouterVille(ville: any) {
    this.villes.push(ville);
  }
}
```

### Utiliser un Service

```typescript
// meteo.component.ts
import { Component, OnInit } from '@angular/core';
import { MeteoService } from '../services/meteo.service';

@Component({
  selector: 'app-meteo',
  templateUrl: './meteo.component.html'
})
export class MeteoComponent implements OnInit {
  villes: any[] = [];

  // Injection du service
  constructor(private meteoService: MeteoService) {}

  ngOnInit() {
    // Récupération des données au chargement
    this.villes = this.meteoService.getVilles();
  }
}
```

```html
<!-- meteo.component.html -->
<div *ngFor="let ville of villes">
  <h2>{{ ville.nom }}</h2>
  <p>{{ ville.temperature }}°C - {{ ville.conditions }}</p>
</div>
```

---

## ⚡ Commandes Essentielles

### Gestion de Projet

```bash
# Créer un nouveau projet
ng new nom-projet

# Lancer le serveur de développement
ng serve
ng serve -o                    # Ouvre le navigateur automatiquement
ng serve --port 4300           # Change le port

# Compiler pour la production
ng build
ng build --configuration production
```

### Génération de Code

```bash
# Composant
ng g c nom-composant
ng g c dossier/nom-composant   # Dans un sous-dossier

# Service
ng g s services/nom-service

# Module
ng g m nom-module

# Interface (pour TypeScript)
ng g interface models/utilisateur

# Guard (protection de routes)
ng g guard guards/auth
```

### Options Utiles

```bash
# Générer sans fichier de test
ng g c mon-composant --skip-tests

# Générer un composant standalone (Angular 17+)
ng g c mon-composant --standalone

# Voir l'aide d'une commande
ng generate --help
ng serve --help
```

### Mise à Jour

```bash
# Vérifier les mises à jour disponibles
ng update

# Mettre à jour Angular
ng update @angular/cli @angular/core
```

---

## 🎓 Ressources pour Aller Plus Loin

### Documentation Officielle
- [Documentation Angular](https://angular.io/docs) - Le guide complet
- [Angular CLI](https://angular.io/cli) - Toutes les commandes
- [TypeScript Handbook](https://www.typescriptlang.org/docs/handbook/intro.html)

### Tutoriels Pratiques
- [Tour of Heroes](https://angular.io/tutorial/tour-of-heroes) - Tutoriel officiel interactif
- [Angular University](https://angular-university.io/) - Cours vidéo gratuits

### Extensions VS Code Recommandées
- **Angular Language Service** - Autocomplétion intelligente
- **Angular Snippets** - Raccourcis de code
- **Prettier** - Formatage automatique du code
- **Auto Rename Tag** - Renommage automatique des balises
- **Error Lens** - Affichage inline des erreurs

---

## 🆘 Problèmes Courants et Solutions

### Le serveur ne démarre pas

```bash
# Effacer le cache npm
npm cache clean --force

# Réinstaller les dépendances
rm -rf node_modules
npm install
```

### "Port 4200 is already in use"

```bash
# Utiliser un autre port
ng serve --port 4300

# Ou tuer le processus qui utilise le port 4200
# Windows
netstat -ano | findstr :4200
taskkill /PID <numéro_du_processus> /F

# macOS/Linux
lsof -ti:4200 | xargs kill
```

### Erreurs de TypeScript

Vérifiez que votre code respecte les types :
```typescript
// ❌ Mauvais
let age = '25';
age = age + 1;  // Erreur : on ne peut pas additionner string + number

// ✅ Bon
let age: number = 25;
age = age + 1;
```

---

**Bon développement avec Angular ! 🚀**

---

*Module 04 - Angular Framework | Formation Développement Web - Promotion Hiver 2026*
