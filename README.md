# 🚀 Formation Complète sur Flutter - Les Fondamentaux  

## 1. Introduction à Flutter  
- Qu'est-ce que Flutter ?  
- Pourquoi utiliser Flutter ?  
- Architecture de Flutter (Dart, widgets, moteur de rendu Skia, etc.)  
- Installation de Flutter SDK et configuration de l’environnement de développement (VS Code, Android Studio)  

## 2. Dart : Le Langage de Programmation  
- Syntaxe de base (variables, types de données, conditions, boucles)  
- Fonctions et classes en Dart  
- Programmation orientée objet (POO) en Dart  
- Asynchronisme avec `Future` et `async/await`  
- Gestion des collections (`List`, `Map`, `Set`)

## 3. Les Widgets : La Base de Flutter
- Différence entre Widgets Stateful et Stateless
- Les widgets de base (Text, Image, Container, Row, Column, ListView, etc.)
- Gestion de l’état avec setState
- Personnalisation des widgets avec Decoration et Padding
## 4. Navigation et Gestion des Écrans
- Navigator et routes
- Passage de données entre écrans
- Gestion de la navigation avec onGenerateRoute
## 5. Gestion de l’État dans Flutter
- setState (gestion d’état locale)
- Provider (gestion d’état globale)
- Autres solutions populaires : Riverpod, Bloc, Redux
## 6. Interaction avec l’Utilisateur
- Formulaires et gestion des entrées utilisateur (TextField, Form, TextEditingController)
- Gestion des événements (onTap, onPressed)
- Affichage de dialogues (AlertDialog, Snackbar)
## 7. Accès aux Données et APIs
- Requêtes HTTP avec http package
- Gestion du JSON (dart:convert)
- Utilisation d’une base de données locale avec sqflite ou Hive
- Firebase (Firestore, Authentification)
## 8. Animations et Effets Visuels
- Animations de base avec AnimatedContainer, AnimatedOpacity
- Utilisation du package Lottie pour des animations avancées
- Hero animations pour la transition entre écrans
## 9. Déploiement et Optimisation
- Gestion des erreurs et debug
- Compilation et génération des APK/IPA
- Optimisation des performances (lazy loading, minimisation des rebuilds)
- Publication sur Google Play Store et Apple App Store

## 1. Introduction à Flutter et Installation  

### 🔷 Qu'est-ce que Flutter ?  
Flutter est un framework open-source développé par Google permettant de créer des applications mobiles, web et desktop avec un seul code source. Il utilise le langage **Dart** et repose sur un système de **widgets** pour créer des interfaces utilisateur fluides et performantes.  

### 🔷 Pourquoi utiliser Flutter ?  
- Développement **cross-platform** (iOS, Android, Web, Desktop).  
- Interface **100% personnalisable** avec des widgets flexibles.  
- **Performances élevées** grâce au moteur Skia et au rendu natif.  
- **Hot Reload** : permet de voir les modifications instantanément.  
- Support de **Firebase, API REST, base de données**, etc.

### 🔷 Installation de Flutter  
1. Télécharger et installer **Flutter SDK** depuis [flutter.dev](https://flutter.dev).  
2. Installer **Android Studio** ou **VS Code**.  
3. Configurer les émulateurs (Android/iOS).  
4. Vérifier l’installation avec la commande :  

   ```sh
   flutter doctor
   ```
## 2.  Apprendre le langage Dart
Flutter utilise **Dart**, un langage optimisé pour le développement mobile.
### 🔷 Syntaxe de base
```dart
void main() {
    print("Hello, Flutter!");
}
```
### 🔹 Variables et types de données
```dart
int age = 25;
double pi = 3.14;
String name = "Flutter";
bool isFlutterAwesome = true;
List<String> fruits = ["Pomme", "Banane", "Orange"];
```
### 🔹 Types Dynamiques (var, dynamic)
```dart
void main() {
  var city = "Paris"; // Déduit comme String
  dynamic anyValue = 42; // Peut changer de type

  print(city);
  anyValue = "Maintenant une chaîne";
  print(anyValue);
}
```
### 🔹 Opérateurs et Expressions
```dart
void main() {
  int a = 10;
  int b = 3;

  print(a + b); // Addition (13)
  print(a - b); // Soustraction (7)
  print(a * b); // Multiplication (30)
  print(a / b); // Division (3.3333)
  print(a ~/ b); // Division entière (3)
  print(a % b); // Modulo (1)
}
```
### 🔹 Opérateurs de Comparaison
```dart
void main() {
  int x = 5;
  int y = 10;

  print(x == y); // false
  print(x != y); // true
  print(x > y);  // false
  print(x <= y); // true
}
```
### 🔹 Conditions (if, else, switch)
**if else**
```dart
void main() {
  int score = 85;

  if (score >= 90) {
    print("Excellent !");
  } else if (score >= 75) {
    print("Très bien !");
  } else {
    print("Besoin d'amélioration.");
  }
}
```
**switch (Alternative à if pour tester plusieurs cas)**
```dart
void main() {
  String day = "Lundi";

  switch (day) {
    case "Lundi":
      print("Début de semaine !");
      break;
    case "Vendredi":
      print("Bientôt le week-end !");
      break;
    default:
      print("Jour normal.");
  }
}
```
**Boucles (for, while, do-while)**
**for**
```dart
void main() {
  for (int i = 1; i <= 5; i++) {
    print("Itération $i");
  }
}
```
**while**
```dart
void main() {
  int n = 3;

  while (n > 0) {
    print("Compte à rebours : $n");
    n--;
  }
}
```
**do-while**
```dart
void main() {
  int x = 0;

  do {
    print("Exécuté au moins une fois !");
    x++;
  } while (x < 1);
}
```
### 🔹 Opérateurs Logiques
```dart
void main() {
  bool isFlutter = true;
  bool isDart = false;

  print(isFlutter && isDart); // false (ET logique)
  print(isFlutter || isDart); // true (OU logique)
  print(!isFlutter); // false (NON logique)
}
```

### 🔹 Fonctions
```dart
String greet(String name) {
  return "Bonjour, $name!";
}

// Fonctions fléchées (Arrow Functions)
String greet(String name) => "Bonjour, $name!";

void main() {
  print(greet("Alice"));
}
```
### 🔹 Classes et objets
```dart
class Person {
  String name;
  int age;

  Person(this.name, this.age);

  void sayHello() {
    print("Bonjour, je m'appelle $name et j'ai $age ans.");
  }
}

void main() {
  Person p = Person("Alice", 25);
  p.sayHello();
}
```
### 🔹 Programmation orientée objet (POO) en Dart
Dart est un **langage orienté objet** où tout est un objet (même les nombres et les fonctions). La POO repose sur **quatre concepts clés** :

- ✅ **Encapsulation (protéger les données)**
- ✅ **Héritage (réutilisation du code)**
- ✅ **Polymorphisme (méthodes redéfinies)**
- ✅ **Abstraction (modèle générique)**

**Encapsulation (Getters & Setters)**
- **L'encapsulation** protège les données d'une classe en les rendant privées (_nom) et accessibles via des getters et setters.
```dart
class BankAccount {
  double _balance = 0; // Propriété privée (préfixée par _)

  // Getter
  double get balance => _balance;

  // Setter
  void deposit(double amount) {
    if (amount > 0) {
      _balance += amount;
      print("Dépôt: $amount | Nouveau solde: $_balance");
    }
  }
}

void main() {
  BankAccount account = BankAccount();
  account.deposit(100);
  print(account.balance); // 100
}
```
**Héritage en Dart (extends)**
- **L'héritage** permet à une classe d'hériter des propriétés et méthodes d'une autre classe.
```dart
class Animal {
  void makeSound() {
    print("L'animal fait un bruit.");
  }
}

class Dog extends Animal {
  void bark() {
    print("Le chien aboie !");
  }
}

void main() {
  Dog myDog = Dog();
  myDog.makeSound(); // L'animal fait un bruit.
  myDog.bark();      // Le chien aboie !
}
```
**Polymorphisme (@override)**
- **Le polymorphisme** permet à une classe dérivée de modifier le comportement d'une méthode héritée.

```dart
class Animal {
  void makeSound() {
    print("L'animal fait un bruit.");
  }
}

class Cat extends Animal {
  @override
  void makeSound() {
    print("Le chat miaule !");
  }
}

void main() {
  Animal myAnimal = Cat();
  myAnimal.makeSound(); // Le chat miaule !
}
```
**Abstraction (abstract)**
- Une classe **abstraite** ne peut pas être instanciée directement, mais sert de modèle pour d'autres classes.

```dart
abstract class Shape {
  void draw(); // Méthode abstraite (à implémenter)
}

class Circle extends Shape {
  @override
  void draw() {
    print("Dessine un cercle.");
  }
}

void main() {
  Circle c = Circle();
  c.draw(); // Dessine un cercle.
}
```
**Interfaces et Mixins**
🔹 **Interfaces (Implémentation multiple avec implements)**
- Une interface permet d'imposer un comportement sans hériter.
```dart
class Animal {
  void eat() {
    print("Cet animal mange.");
  }
}

class Flyer {
  void fly() {
    print("Cet animal vole.");
  }
}

// Un oiseau implémente plusieurs comportements
class Bird implements Animal, Flyer {
  @override
  void eat() {
    print("L'oiseau picore.");
  }

  @override
  void fly() {
    print("L'oiseau vole haut.");
  }
}

void main() {
  Bird myBird = Bird();
  myBird.eat(); // L'oiseau picore.
  myBird.fly(); // L'oiseau vole haut.
}
```
🔹 **Mixins (with)**
- Les **mixins** permettent d'ajouter du code à une classe sans héritage.
```dart
mixin CanSwim {
  void swim() {
    print("Cet animal nage.");
  }
}

class Fish with CanSwim {}

void main() {
  Fish nemo = Fish();
  nemo.swim(); // Cet animal nage.
}
```
🎯  **Résumé des Concepts**
| Concept | Explication | Mot-clé 
|-----------|--------|---------------|
| **Classe et Objet**   | Modèle et instance   |  class        |
| **Encapsulation** | Protéger les données | _private, get, set | 
| **Héritage**   | Réutilisation du code  | extends        |
| **Polymorphisme**   | Redéfinition des méthodes  | @override        |
| **Abstraction**   | Modèle générique  | abstract        |
| **Interface**   | Implémentation multiple  | implements        |
| **Mixins**   | Ajouter des fonctionnalités  | with     |
### 🔹 Asynchronisme en Dart (Future, async/await) 
Dart est un langage asynchrone qui permet d'exécuter plusieurs tâches en parallèle sans bloquer l'application. L'asynchronisme repose principalement sur trois concepts :
- ✅ Future : Représente une tâche qui sera terminée plus tard.
- ✅ async/await : Simplifie la gestion des Future pour un code plus lisible.
- ✅ Stream : Gère des suites de données asynchrones (ex : flux de données).
### 🔹 Future : Exécution asynchrone
- Un Future est une valeur qui sera disponible dans le futur après l'exécution d'une tâche asynchrone.
**🔹 Créer un Future et utiliser then()**
```dart
Future<String> fetchData() {
  return Future.delayed(Duration(seconds: 2), () => "Données chargées !");
}

void main() {
  print("Début de la tâche...");
  
  fetchData().then((result) {
    print(result); // Affiché après 2 secondes
  });

  print("Fin du programme !");
}
```
### 🔹async/await : Simplifier l’attente des Future
- L'utilisation de await permet d'attendre la fin d'un Future sans bloquer l'application.
```dart
Future<String> fetchData() async {
  await Future.delayed(Duration(seconds: 2)); // Simule un délai
  return "Données chargées !";
}

void main() async {
  print("Début de la tâche...");

  String result = await fetchData(); // Attente du résultat
  print(result);

  print("Fin du programme !");
}
```
### 🔹Gérer les erreurs avec try/catch
- Les erreurs dans les Future doivent être capturées pour éviter les crashs.
```dart
Future<String> fetchData() async {
  await Future.delayed(Duration(seconds: 2));
  throw Exception("Erreur de chargement !");
}

void main() async {
  print("Début de la tâche...");

  try {
    String result = await fetchData();
    print(result);
  } catch (e) {
    print("Erreur attrapée : $e");
  }

  print("Fin du programme !");
}
```
### 🔹Future.wait() : Attendre plusieurs Future en parallèle
- Si plusieurs tâches doivent être exécutées en parallèle, Future.wait() permet d’attendre toutes les réponses
```dart
Future<String> fetchUser() async {
  await Future.delayed(Duration(seconds: 2));
  return "Utilisateur chargé";
}

Future<String> fetchPosts() async {
  await Future.delayed(Duration(seconds: 3));
  return "Posts chargés";
}

void main() async {
  print("Chargement des données...");

  List<String> results = await Future.wait([fetchUser(), fetchPosts()]);
  print(results[0]); // Utilisateur chargé
  print(results[1]); // Posts chargés

  print("Toutes les données sont chargées !");
}
```
### 🔹Stream : Gérer un flux de données asynchrones
- Contrairement à Future, un Stream permet d’envoyer plusieurs valeurs au fil du temps.
```dart
Stream<int> countStream() async* {
  for (int i = 1; i <= 5; i++) {
    await Future.delayed(Duration(seconds: 1));
    yield i; // Envoie la valeur à chaque seconde
  }
}

void main() async {
  print("Début du Stream...");

  await for (int value in countStream()) {
    print("Valeur reçue : $value");
  }

  print("Fin du Stream !");
}
```dart
Future<String> fetchData() async {
  await Future.delayed(Duration(seconds: 2));
  return "Données récupérées";
}

void main() async {
  print("Chargement...");
  String data = await fetchData();
  print(data);
}
```
### 🔹Transformer un Stream en Future
Parfois, on veut attendre la première valeur d’un Stream et l'utiliser comme un Future.
```dart
void main() async {
  int firstValue = await countStream().first;
  print("Première valeur : $firstValue"); // Première valeur : 1
}
```
🎯  **Résumé des Concepts**
| Concept | Explication | Mot-clé 
|-----------|--------|---------------|
| **Future**   | Exécuter une tâche asynchrone   |  Future        |
| **async/await** | Attendre un Future sans bloquer | async, await | 
| **Gestion des erreurs**   | Capturer les erreurs dans un Future  | try/catch        |
| **Future.wait()**   | Exécuter plusieurs Future en parallèle  | Future.wait()        |
| **Stream**   | Gérer plusieurs valeurs asynchrones  | Stream, yield        |
| **Stream → Future**   | Récupérer une seule valeur d'un Stream	  | .first        |
### 🔹 Gestion des collections (List, Map, Set) flutter
En Flutter (Dart), les collections comme List, Map et Set sont largement utilisées pour stocker et manipuler des données. Voici un aperçu de leur gestion avec des exemples pratiques.
#### List
Une List en Dart est une collection ordonnée qui peut contenir des éléments en double.
**Déclaration et initialisation**
```dart
List<String> fruits = ['Pomme', 'Banane', 'Orange']
```
**Ajout d’éléments**
```dart
fruits.add('Mangue');  // Ajoute à la fin
fruits.insert(1, 'Fraise');  // Ajoute à une position spécifique
```
**Suppression d’éléments**
```dart
fruits.remove('Banane');  // Supprime la première occurrence
fruits.removeAt(0);  // Supprime par index
```
**Accès aux éléments**
```dart
String premierFruit = fruits[0];
print(premierFruit);  // Pomme
```
**Boucle sur une liste**
```dart
for (String fruit in fruits) {
  print(fruit);
}
```
#### Map
Un Map en Dart est une collection associant des clés uniques à des valeurs.
```dart
Map<String, int> ages = {
  'Alice': 25,
  'Bob': 30,
  'Charlie': 35
};
ages['David'] = 40;  // Ajoute un nouvel élément
ages['Alice'] = 26;  // Modifie un élément existant
ages.remove('Bob');
int ageAlice = ages['Alice'] ?? 0;
print(ageAlice);  // 26
ages.forEach((nom, age) {
  print('$nom a $age ans');
});
```
#### Set
Un **Set** est une collection non ordonnée où chaque élément est unique.
```dart
Set<int> nombres = {1, 2, 3, 4, 5};
nombres.add(6);
nombres.add(2);  // Pas d'effet, car 2 est déjà présent
nombres.remove(3);
bool existe = nombres.contains(4);
print(existe);  // true
Set<int> ensembleA = {1, 2, 3};
Set<int> ensembleB = {3, 4, 5};

var union = ensembleA.union(ensembleB);  // {1, 2, 3, 4, 5}
var intersection = ensembleA.intersection(ensembleB);  // {3}
var difference = ensembleA.difference(ensembleB);  // {1, 2}
```
#### Résumé
| Collection | Ordonnée | Duplicats autorisés | Accès par index |
|-----------|--------|---------------|------------|
| List   | Oui   |  Oui        | Oui  |
| Map | Non | Uniquement pour les valeurs | Non (clé utilisée) |
| Set   | Non  | Non        | Non  |

## 3. Les Widgets dans Flutter
Flutter repose sur des **widgets** pour construire l’interface utilisateur.
### 🔹 Différence entre StatelessWidget et StatefulWidget
- **StatelessWidget** → Interface statique
- **StatefulWidget** → Interface dynamique (qui change avec setState)
**Exemple : StatelessWidget**
```dart
class MyWidget extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Text("Ceci est un widget statique");
  }
}
```
**Exemple : StatefulWidget**
```dart
class MyCounter extends StatefulWidget {
  @override
  _MyCounterState createState() => _MyCounterState();
}

class _MyCounterState extends State<MyCounter> {
  int _counter = 0;

  void _increment() {
    setState(() {
      _counter++;
    });
  }

  @override
  Widget build(BuildContext context) {
    return Column(
      children: [
        Text("Compteur: $_counter"),
        ElevatedButton(
          onPressed: _increment,
          child: Text("Incrémenter"),
        ),
      ],
    );
  }
}
```
### 🔹 Widgets de base
Flutter repose sur des widgets pour construire l’interface utilisateur. Voici les widgets de base indispensables :
- ✅ Text → Afficher du texte
- ✅ Image → Afficher une image
- ✅ Container → Boîte avec des marges, padding, couleur
- ✅ Row & Column → Disposer les éléments horizontalement ou verticalement
- ✅ ListView → Liste défilante
- ✅ ElevatedButton → Bouton interactif
- ✅ Scaffold → Structure de base d'une page
#### 1️⃣ Widget Text (Afficher du texte)
Le widget Text permet d'afficher du texte avec plusieurs styles.
**Exemple : Texte simple**
```dart
Text("Bonjour, Flutter !");
```
**Texte avec style**
```dart
Text(
  "Bienvenue sur Flutter",
  style: TextStyle(
    fontSize: 20, 
    fontWeight: FontWeight.bold, 
    color: Colors.blue
  ),
);
```
#### 2️⃣ Widget Image (Afficher des images)
Flutter permet d'afficher des images depuis :
- 📌 Un fichier local (AssetImage)
- 📌 Internet (NetworkImage)
**🔹 Image depuis un fichier local**
Ajoute l’image dans **pubspec.yaml**:
```dart
flutter:
  assets:
    - assets/images/flutter_logo.png
```
Puis dans le code :
```dart
Image.asset("assets/images/flutter_logo.png");
```
**🔹 Image depuis Internet**
```dart
Image.network("https://flutter.dev/images/flutter-logo-sharing.png");
```
#### 3️⃣ Widget Container (Bloc personnalisable)
Container est un widget flexible pour ajouter :
- 🟩 Couleur de fond
- 📏 Taille
- 🎨 Marges & Padding
***🔹 Exemple d’un Container stylisé***
```dart
Container(
  width: 200,
  height: 100,
  padding: EdgeInsets.all(10),
  margin: EdgeInsets.symmetric(vertical: 10),
  decoration: BoxDecoration(
    color: Colors.blue,
    borderRadius: BorderRadius.circular(10),
  ),
  child: Text("Hello Flutter", style: TextStyle(color: Colors.white)),
);
```
#### 4️⃣ Widgets Row & Column (Alignement d’éléments)
- Row → Disposition horizontale
- Column → Disposition verticale

**🔹 Exemple Row (alignement horizontal)**
```dart
Row(
  mainAxisAlignment: MainAxisAlignment.spaceAround,
  children: [
    Icon(Icons.star, color: Colors.orange),
    Icon(Icons.star, color: Colors.orange),
    Icon(Icons.star, color: Colors.orange),
  ],
);
```
**🔹 Exemple Column (alignement vertical)**
```dart
Column(
  mainAxisAlignment: MainAxisAlignment.center,
  children: [
    Text("Élément 1"),
    SizedBox(height: 10), // Espacement
    Text("Élément 2"),
  ],
);
```
| Propriété | Explication 
|-----------|--------|
| **mainAxisAlignment**   | Alignement principal (start, center, end, spaceAround, spaceBetween)   |
| **crossAxisAlignment** | Alignement secondaire (start, center, end) |
#### 5️⃣ Widget ListView (Liste défilante dynamique)
ListView est utilisé pour afficher des listes longues, avec ou sans défilement.
**🔹 Liste simple**
```dart
ListView(
  children: [
    ListTile(title: Text("Élément 1")),
    ListTile(title: Text("Élément 2")),
    ListTile(title: Text("Élément 3")),
  ],
);
```
**🔹 Liste dynamique (générée avec ListView.builder)**
```dart
ListView.builder(
  itemCount: 10,
  itemBuilder: (context, index) {
    return ListTile(
      title: Text("Élément ${index + 1}"),
    );
  },
);
```
#### 6️⃣ Widget ElevatedButton (Bouton interactif)
Permet d'ajouter un bouton cliquable.
**🔹 Exemple de bouton**
```dart
ElevatedButton(
  onPressed: () {
    print("Bouton cliqué !");
  },
  child: Text("Clique-moi"),
);
```
**🔹 Bouton avec style**
```dart
ElevatedButton(
  style: ElevatedButton.styleFrom(
    backgroundColor: Colors.blue,
    padding: EdgeInsets.symmetric(horizontal: 20, vertical: 10),
  ),
  onPressed: () {},
  child: Text("Appuyer", style: TextStyle(color: Colors.white)),
);
```
#### 7️⃣ Widget Scaffold (Structure d’une page complète)
Le Scaffold est le squelette d’une application Flutter. Il inclut :
- ✅ AppBar → Barre supérieure
- ✅ Body → Contenu principal
- ✅ FloatingActionButton → Bouton flottant
**🔹 Exemple d’un Scaffold**
```dart
  Scaffold(
  appBar: AppBar(title: Text("Mon App")),
  body: Center(child: Text("Bienvenue")),
  floatingActionButton: FloatingActionButton(
    onPressed: () {},
    child: Icon(Icons.add),
  ),);
```
**🎯 Résumé des Widgets de Base**
| Concept | Explication | Mot-clé 
|-----------|--------|---------------|
| **Text**   | Affiche du texte   |  Text("Bonjour")        |
| **Image** | Affiche une image	 | Image.asset("path") | 
| **Container**   | Encapsule et stylise un élément  | Container(color: Colors.blue)        |
| **Row**   | Affichage horizontal	  | Row(children: [...])        |
| **Column**   | Affichage vertical	  | Column(children: [...])        |
| **ListView**   | Liste défilante	  | ListView.builder(...)        |
| **ElevatedButton**   | Bouton cliquable	 | ElevatedButton(onPressed: ..., child: Text(...))     |
| **Scaffold**   | Structure d’une page	  | Scaffold(appBar: ..., body: ...)     |

## 4. Navigation entre les écrans
Flutter utilise Navigator pour gérer les transitions entre les pages.
En Flutter, chaque écran est appelé une route et est géré par un Navigator.
📌 Méthodes principales du Navigator :

- push() → Aller vers un nouvel écran.
- pop() → Revenir à l’écran précédent.
- pushReplacement() → Remplace l’écran actuel par un nouveau.
- pushAndRemoveUntil() → Supprime tous les écrans et affiche un nouvel écran.
1️⃣ Navigation de Base avec Navigator.push()
Utilisation de MaterialPageRoute pour naviguer vers un nouvel écran.
### 🔹 Passer d’un écran à un autre
```dart
Navigator.push(
  context,
  MaterialPageRoute(builder: (context) => SecondScreen()),
);
```
### 🔹 Retour à l’écran précédent
```dart
Navigator.pop(context);
```
### 🔹 Passage de données entre écrans
```dart
Navigator.push(
  context,
  MaterialPageRoute(builder: (context) => SecondScreen(data: "Hello")),
);
```
### 🔹 Retourner un Résultat à l'Écran Précédent
Un écran peut retourner un résultat à l’écran précédent via Navigator.pop(context, result).
```dart
Navigator.pop(context, "Option A")
```
### 🔹Remplacer un Écran avec pushReplacement()
```dart
Navigator.pushReplacement(
  context,
  MaterialPageRoute(builder: (context) => HomeScreen()),
);
```
**📌 Cas d’utilisation :**

- Après une connexion réussie.
- Après un splash screen.
```dart
Navigator.pushAndRemoveUntil(
  context,
  MaterialPageRoute(builder: (context) => HomeScreen()),
  (route) => false, // Supprime toutes les routes
);
```
**📌 Cas d’utilisation :**
- Après une déconnexion (retour à l’écran de connexion).
- Après une réinitialisation d’application.

**📌 Conclusion**
| Concept | Explication 
|-----------|--------
| **push()**   | Aller vers un nouvel écran   
| **pop()** | Revenir à l’écran précédent   
| **pushReplacement()**   | Remplace l’écran actuel 
| **pushAndRemoveUntil()**   | Supprime l’historique et ouvre un nouvel écran	 
| **pushNamed()**   | Naviguer avec des routes nommées

### 🔹Supprimer l’Historique avec pushAndRemoveUntil()
## 5. Gestion de l’état
Il existe plusieurs façons de gérer l’état d’une application Flutter :
🔹 **setState()** → Gestion d’état locale
```dart
setState(() {
  _counter++;
});
```
🔹 Provider → Gestion d’état globale
Provider est une solution officielle de Flutter pour gérer l’état globalement.
**📌 Ajouter Provider au projet**
Ajoutez provider dans pubspec.yaml :
```dart
dependencies:
  flutter:
    sdk: flutter
  provider: ^6.0.0
```
**📌 Créer un ChangeNotifier pour gérer l’état**
```dart
class CounterProvider with ChangeNotifier {
  int _counter = 0;

  int get counter => _counter;

  void increment() {
    _counter++;
    notifyListeners();
  }
}
```
## 6. Interaction avec l’Utilisateur
### 🔹 Formulaires et gestion des entrées utilisateur (TextField, Form, TextEditingController)
Les formulaires sont essentiels pour les inscriptions, connexions, recherches et d’autres interactions utilisateur. En Flutter, nous utilisons TextField, Form, et TextEditingController pour capturer et gérer les entrées utilisateur.
**1️⃣ TextField – Le Champ de Saisie de Base**
Exemple : Champ de texte simple
```dart
TextField(
  decoration: InputDecoration(
    labelText: "Entrez votre nom",
    border: OutlineInputBorder(),
  ),
)
```
**📌 Personnalisation :**

- labelText → Affiche un texte dans le champ.
- border: OutlineInputBorder() → Ajoute une bordure.
- hintText → Donne une indication à l’utilisateur.
**2️⃣ Gérer le Texte avec TextEditingController**
Pour récupérer et manipuler la valeur d’un TextField, on utilise TextEditingController.
**📌 Exemple : Lire l’entrée utilisateur**
```dart
class TextFieldExample extends StatefulWidget {
  @override
  _TextFieldExampleState createState() => _TextFieldExampleState();
}

class _TextFieldExampleState extends State<TextFieldExample> {
  TextEditingController _controller = TextEditingController();

  void _showText() {
    print("Texte saisi : ${_controller.text}");
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: Text("TextField Controller")),
      body: Padding(
        padding: EdgeInsets.all(16),
        child: Column(
          children: [
            TextField(
              controller: _controller,
              decoration: InputDecoration(
                labelText: "Entrez du texte",
                border: OutlineInputBorder(),
              ),
            ),
            SizedBox(height: 10),
            ElevatedButton(
              onPressed: _showText,
              child: Text("Afficher le Texte"),
            ),
          ],
        ),
      ),
    );
  }
}
```
**📌 Explication :**

- TextEditingController récupère le texte saisi.
- _controller.text accède au contenu du champ.
- Le bouton affiche la valeur dans la console.

**3️⃣ Form & TextFormField – Validation des Données**
Pour valider les champs, on utilise un Form avec TextFormField.
```dart
class FormExample extends StatefulWidget {
  @override
  _FormExampleState createState() => _FormExampleState();
}

class _FormExampleState extends State<FormExample> {
  final _formKey = GlobalKey<FormState>();
  TextEditingController _emailController = TextEditingController();

  void _submitForm() {
    if (_formKey.currentState!.validate()) {
      print("Email Valide : ${_emailController.text}");
    }
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: Text("Formulaire avec Validation")),
      body: Padding(
        padding: EdgeInsets.all(16),
        child: Form(
          key: _formKey,
          child: Column(
            children: [
              TextFormField(
                controller: _emailController,
                decoration: InputDecoration(
                  labelText: "Email",
                  border: OutlineInputBorder(),
                ),
                validator: (value) {
                  if (value == null || value.isEmpty) {
                    return "Veuillez entrer un email";
                  } else if (!value.contains("@")) {
                    return "Email invalide";
                  }
                  return null;
                },
              ),
              SizedBox(height: 10),
              ElevatedButton(
                onPressed: _submitForm,
                child: Text("Valider"),
              ),
            ],
          ),
        ),
      ),
    );
  }
}
```
**4️⃣ Masquer le Texte (Mot de Passe)**
On peut masquer un texte en utilisant obscureText: true.
```dart
TextField(
  obscureText: true,
  decoration: InputDecoration(
    labelText: "Mot de passe",
    border: OutlineInputBorder(),
  ),
)
```
5️⃣ Plusieurs Champs dans un Formulaire
Créons un formulaire email + mot de passe avec validation.
**📌 Exemple : Formulaire de Connexion**
```dart
class LoginForm extends StatefulWidget {
  @override
  _LoginFormState createState() => _LoginFormState();
}

class _LoginFormState extends State<LoginForm> {
  final _formKey = GlobalKey<FormState>();
  TextEditingController _emailController = TextEditingController();
  TextEditingController _passwordController = TextEditingController();
  bool _obscurePassword = true;

  void _submit() {
    if (_formKey.currentState!.validate()) {
      print("Connexion réussie !");
      print("Email : ${_emailController.text}");
      print("Mot de passe : ${_passwordController.text}");
    }
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: Text("Connexion")),
      body: Padding(
        padding: EdgeInsets.all(16),
        child: Form(
          key: _formKey,
          child: Column(
            children: [
              TextFormField(
                controller: _emailController,
                decoration: InputDecoration(
                  labelText: "Email",
                  border: OutlineInputBorder(),
                ),
                validator: (value) {
                  if (value == null || value.isEmpty) return "Veuillez entrer un email";
                  if (!value.contains("@")) return "Email invalide";
                  return null;
                },
              ),
              SizedBox(height: 10),
              TextFormField(
                controller: _passwordController,
                obscureText: _obscurePassword,
                decoration: InputDecoration(
                  labelText: "Mot de passe",
                  border: OutlineInputBorder(),
                  suffixIcon: IconButton(
                    icon: Icon(_obscurePassword ? Icons.visibility : Icons.visibility_off),
                    onPressed: () {
                      setState(() {
                        _obscurePassword = !_obscurePassword;
                      });
                    },
                  ),
                ),
                validator: (value) {
                  if (value == null || value.length < 6) return "Mot de passe trop court";
                  return null;
                },
              ),
              SizedBox(height: 10),
              ElevatedButton(
                onPressed: _submit,
                child: Text("Se connecter"),
              ),
            ],
          ),
        ),
      ),
    );
  }
}
```
**📌 Conclusion**
| Fonctionnalité | Widget Utilisé 
|-----------|--------|
| **Champ de texte simple**   | Aller vers un nouvel écran   |
| **Lire le texte saisi** | Revenir à l’écran précédent  |  
| **Valider les données**   | Remplace l’écran actuel  |
| **Masquer le mot de passe**   | Supprime l’historique et ouvre un nouvel écran	  |
| **Bouton pour afficher/cacher**   | Naviguer avec des routes nommées	  |
| **Plusieurs champs dans un formulaire** | Column + TextFormField

### 🔹 Gestion des événements (onTap, onPressed)
En Flutter, les interactions utilisateur sont capturées via des événements comme clics, tapotements, gestes et plus encore. Les plus courants sont onTap et onPressed, mais d’autres existent pour gérer différents types d’actions.
**1️⃣ onPressed – Bouton Cliquable**
L’événement onPressed est utilisé principalement avec les boutons (ElevatedButton, TextButton, IconButton).
```dart
ElevatedButton(
  onPressed: () {
    print("Bouton appuyé !");
  },
  child: Text("Appuyez-moi"),
)
```
**📌 Explication :**
Lorsque l’utilisateur clique, la fonction affiche un message dans la console.*
**2️⃣ onTap – Détection du Tapotement**
Si un widget n’a pas de onPressed, on peut utiliser GestureDetector ou InkWell pour détecter les taps.
**📌 Exemple : Détection d’un Tap sur un Texte**
```dart
GestureDetector(
  onTap: () {
    print("Texte cliqué !");
  },
  child: Text(
    "Cliquez ici",
    style: TextStyle(fontSize: 20, color: Colors.blue),
  ),
)
```
**📌 Explication :**
GestureDetector permet d’ajouter un comportement interactif à n’importe quel widget.
**3️⃣ InkWell – Effet de Tap avec Animation**
InkWell ajoute un effet visuel (ripple) lorsqu’on appuie sur un widget.
**📌 Exemple : Carte Cliquable**
```dart
InkWell(
  onTap: () {
    print("Carte cliquée !");
  },
  child: Container(
    padding: EdgeInsets.all(20),
    decoration: BoxDecoration(color: Colors.blue, borderRadius: BorderRadius.circular(10)),
    child: Text("Cliquez-moi", style: TextStyle(color: Colors.white)),
  ),
)
```
**4️⃣ onLongPress – Pression Longue**
Utile pour afficher un menu contextuel ou exécuter une action spéciale.

**📌 Exemple : Bouton avec Pression Longue**
```dart
ElevatedButton(
  onPressed: () {
    print("Bouton pressé");
  },
  onLongPress: () {
    print("Pression longue détectée !");
  },
  child: Text("Appuyez longtemps"),
)
```
5️⃣ Détection de Glisser (Swipe)
On peut détecter un glissement horizontal ou vertical avec GestureDetector.
**📌 Exemple : Détecter un Swipe Gauche/Droite**
```dart
GestureDetector(
  onHorizontalDragEnd: (details) {
    if (details.primaryVelocity! > 0) {
      print("Swipe vers la DROITE !");
    } else {
      print("Swipe vers la GAUCHE !");
    }
  },
  child: Container(
    width: double.infinity,
    height: 200,
    color: Colors.amber,
    child: Center(child: Text("Glissez-moi")),
  ),
)
```
**6️⃣ Détection de Double Tap**
Pour détecter un double tap, on utilise GestureDetector.
**📌 Exemple : Double Tap pour Changer de Couleur**
```dart
class DoubleTapExample extends StatefulWidget {
  @override
  _DoubleTapExampleState createState() => _DoubleTapExampleState();
}

class _DoubleTapExampleState extends State<DoubleTapExample> {
  Color _color = Colors.green;

  void _changeColor() {
    setState(() {
      _color = _color == Colors.green ? Colors.red : Colors.green;
    });
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: Center(
        child: GestureDetector(
          onDoubleTap: _changeColor,
          child: Container(
            width: 200,
            height: 200,
            color: _color,
            child: Center(child: Text("Double Tap", style: TextStyle(color: Colors.white))),
          ),
        ),
      ),
    );
  }
}
```
### 🔹 Affichage de dialogues (AlertDialog, Snackbar)
En Flutter, il est courant d’afficher des boîtes de dialogue et des notifications pour informer l’utilisateur, demander une confirmation, ou afficher une erreur. Les widgets les plus utilisés sont AlertDialog et Snackbar.

**1️⃣ AlertDialog – Fenêtre Modale de Confirmation**
Un AlertDialog est une boîte de dialogue qui bloque l’écran jusqu’à ce que l’utilisateur prenne une décision.

**📌 Exemple : Affichage d’un AlertDialog**
```dart
void _showDialog(BuildContext context) {
  showDialog(
    context: context,
    builder: (BuildContext context) {
      return AlertDialog(
        title: Text("Confirmation"),
        content: Text("Voulez-vous continuer ?"),
        actions: [
          TextButton(
            onPressed: () {
              Navigator.of(context).pop(); // Ferme la boîte de dialogue
            },
            child: Text("Annuler"),
          ),
          ElevatedButton(
            onPressed: () {
              print("Action confirmée !");
              Navigator.of(context).pop(); // Ferme la boîte de dialogue
            },
            child: Text("Oui"),
          ),
        ],
      );
    },
  );
}
```
**📌 Explication :**

- showDialog → Ouvre un dialogue.
- AlertDialog → Contient un titre, un message, et des boutons d’action.
- Navigator.of(context).pop() → Ferme le dialogue.
**📌 Exemple : Bouton pour Afficher un AlertDialog**
```dart
ElevatedButton(
  onPressed: () => _showDialog(context),
  child: Text("Afficher le Dialogue"),
)
```
**2️⃣ AlertDialog avec Champs de Texte**
On peut ajouter un TextField dans un AlertDialog pour capturer une entrée utilisateur.
**📌 Exemple : Demander un Nom d’Utilisateur**
```dart
void _showInputDialog(BuildContext context) {
  TextEditingController _controller = TextEditingController();

  showDialog(
    context: context,
    builder: (BuildContext context) {
      return AlertDialog(
        title: Text("Votre Nom"),
        content: TextField(
          controller: _controller,
          decoration: InputDecoration(hintText: "Entrez votre nom"),
        ),
        actions: [
          TextButton(
            onPressed: () => Navigator.of(context).pop(),
            child: Text("Annuler"),
          ),
          ElevatedButton(
            onPressed: () {
              print("Nom saisi : ${_controller.text}");
              Navigator.of(context).pop();
            },
            child: Text("OK"),
          ),
        ],
      );
    },
  );
}
```
**3️⃣ Snackbar – Message Temporaire**
Un Snackbar est une notification temporaire qui s’affiche en bas de l’écran.
```dart
void _showSnackbar(BuildContext context) {
  ScaffoldMessenger.of(context).showSnackBar(
    SnackBar(
      content: Text("Action effectuée !"),
      duration: Duration(seconds: 2),
    ),
  );
}
```
**📌 Explication :**
- ScaffoldMessenger.of(context).showSnackBar() → Affiche un Snackbar.
- duration → Détermine combien de temps il reste visible.
**📌 Exemple : Bouton qui Affiche un Snackbar**
```dart
ElevatedButton(
  onPressed: () => _showSnackbar(context),
  child: Text("Afficher Snackbar"),
)
```
**4️⃣ Snackbar avec Bouton d’Action**
On peut ajouter un bouton interactif dans un Snackbar.
**📌 Exemple : Snackbar avec "Annuler"**
```dart
void _showActionSnackbar(BuildContext context) {
  ScaffoldMessenger.of(context).showSnackBar(
    SnackBar(
      content: Text("Suppression en cours..."),
      action: SnackBarAction(
        label: "Annuler",
        onPressed: () {
          print("Suppression annulée !");
        },
      ),
    ),
  );
}
```
**📌 Explication :**
- SnackBarAction → Ajoute un bouton "Annuler".
- onPressed → Exécute une action quand l’utilisateur appuie sur le bouton.
**5️⃣ SimpleDialog – Liste d’Options**
Un SimpleDialog est une boîte de dialogue affichant une liste d’options.
**📌 Exemple : Sélectionner une Option**
```dart
void _showSimpleDialog(BuildContext context) {
  showDialog(
    context: context,
    builder: (BuildContext context) {
      return SimpleDialog(
        title: Text("Choisissez une option"),
        children: [
          SimpleDialogOption(
            onPressed: () {
              print("Option 1 sélectionnée");
              Navigator.of(context).pop();
            },
            child: Text("Option 1"),
          ),
          SimpleDialogOption(
            onPressed: () {
              print("Option 2 sélectionnée");
              Navigator.of(context).pop();
            },
            child: Text("Option 2"),
          ),
        ],
      );
    },
  );
}
```
**6️⃣ BottomSheet – Fenêtre Coulissante**
Un BottomSheet est une boîte qui s’ouvre par le bas de l’écran.
```dart
void _showBottomSheet(BuildContext context) {
  showModalBottomSheet(
    context: context,
    builder: (BuildContext context) {
      return Container(
        padding: EdgeInsets.all(20),
        height: 200,
        child: Column(
          children: [
            Text("Titre du BottomSheet", style: TextStyle(fontSize: 18, fontWeight: FontWeight.bold)),
            SizedBox(height: 10),
            Text("Ceci est un BottomSheet."),
            ElevatedButton(
              onPressed: () => Navigator.of(context).pop(),
              child: Text("Fermer"),
            ),
          ],
        ),
      );
    },
  );
}
```
**📌 Conclusion**
| 🎯 Type de Boîte	 | 🚀 Widget Utilisé	 | 📌 Utilisation
|-----------|--------|---------------|
| **Boîte de dialogue**   | AlertDialog   |  Confirmation, alerte       |
| **Snackbar** | SnackBar	 | Message temporaire | 
| **Boîte d’options**   | SimpleDialog  | Liste d’options        |
| **Fenêtre coulissante**   | BottomSheet	  | Menu ou info en bas de l’écran        |

## 8. Connexion à une API REST et Firebase
Flutter permet de communiquer avec des API ou des serveurs distants grâce au package http.
Cela vous permet d'effectuer des requêtes HTTP (GET, POST, PUT, DELETE, etc.) pour récupérer ou envoyer des données.
### 🔹 Consommer une API REST
**1️⃣ Ajouter le package http à votre projet**
Avant de commencer à utiliser le package http, vous devez l'ajouter à votre projet.
**📌 Étapes :**
- Ouvrez le fichier pubspec.yaml.
- Ajoutez la dépendance suivante sous dependencies :
```dart
dependencies:
  flutter:
    sdk: flutter
  http: ^0.13.3  # Vérifiez la dernière version sur pub.dev
```
- Exécutez la commande pour installer la dépendance :
```sh
flutter pub get
```
**2️⃣ Effectuer une Requête HTTP GET**
La requête GET est utilisée pour récupérer des données à partir d’un serveur distant.
```dart
import 'package:http/http.dart' as http;
import 'dart:convert';

Future<void> fetchData() async {
  final response = await http.get(Uri.parse('https://jsonplaceholder.typicode.com/posts'));

  if (response.statusCode == 200) {
    // Si la requête est réussie, parsez la réponse
    var data = jsonDecode(response.body);
    print(data);
  } else {
    // Si la requête échoue, affichez un message d'erreur
    print('Erreur de chargement des données');
  }
}
```
**📌 Explication :**

- http.get() : Effectue la requête GET.
- jsonDecode() : Décode la réponse JSON en une structure de données Dart.
- statusCode == 200 : Vérifie que la requête a réussi.
**📌 Appeler la fonction dans le widget**
```dart
fetchData();  // Appelez cette fonction dans le `initState` ou lorsque vous en avez besoin
```
**3️⃣ Effectuer une Requête HTTP POST**
La requête POST permet d'envoyer des données au serveur.
**📌 Exemple : Requête POST**
```dart
Future<void> sendData() async {
  final response = await http.post(
    Uri.parse('https://jsonplaceholder.typicode.com/posts'),
    headers: <String, String>{
      'Content-Type': 'application/json; charset=UTF-8',
    },
    body: jsonEncode(<String, String>{
      'title': 'Flutter Demo',
      'body': 'This is a Flutter POST request.',
      'userId': '1',
    }),
  );

  if (response.statusCode == 201) {
    print('Données envoyées avec succès');
  } else {
    print('Erreur d\'envoi des données');
  }
}
```
**4️⃣ Effectuer une Requête HTTP PUT**
La requête PUT permet de mettre à jour des données existantes sur le serveur.
```dart
Future<void> updateData() async {
  final response = await http.put(
    Uri.parse('https://jsonplaceholder.typicode.com/posts/1'),
    headers: <String, String>{
      'Content-Type': 'application/json; charset=UTF-8',
    },
    body: jsonEncode(<String, String>{
      'id': '1',
      'title': 'Flutter Demo (Updated)',
      'body': 'This is the updated Flutter PUT request.',
      'userId': '1',
    }),
  );

  if (response.statusCode == 200) {
    print('Données mises à jour avec succès');
  } else {
    print('Erreur de mise à jour des données');
  }
}
```
**5️⃣ Effectuer une Requête HTTP DELETE**
La requête DELETE permet de supprimer une ressource sur le serveur.
```dart
Future<void> deleteData() async {
  final response = await http.delete(
    Uri.parse('https://jsonplaceholder.typicode.com/posts/1'),
  );

  if (response.statusCode == 200) {
    print('Données supprimées avec succès');
  } else {
    print('Erreur de suppression des données');
  }
}
```
**6️⃣ Gestion des Erreurs**
Lorsque vous effectuez des requêtes HTTP, vous devez toujours gérer les erreurs, telles que les erreurs de réseau ou de serveur.
```dart
Future<void> fetchDataWithErrorHandling() async {
  try {
    final response = await http.get(Uri.parse('https://jsonplaceholder.typicode.com/posts'));

    if (response.statusCode == 200) {
      var data = jsonDecode(response.body);
      print(data);
    } else {
      print('Erreur avec le code de statut : ${response.statusCode}');
    }
  } catch (e) {
    print('Erreur lors de la requête HTTP: $e');
  }
}
```
**7️⃣ Headers et Authentification**
Les requêtes HTTP peuvent inclure des en-têtes pour envoyer des informations supplémentaires comme des tokens d'authentification.
```dart
Future<void> fetchWithAuth() async {
  final response = await http.get(
    Uri.parse('https://jsonplaceholder.typicode.com/posts'),
    headers: <String, String>{
      'Authorization': 'Bearer YOUR_ACCESS_TOKEN',
    },
  );

  if (response.statusCode == 200) {
    var data = jsonDecode(response.body);
    print(data);
  } else {
    print('Erreur d\'authentification');
  }
}
```
**📌 Conclusion**
| 🎯 Type de Requête	 | 🚀 Fonction	 | 📌 Utilisation
|-----------|--------|---------------|
| **GET**   | http.get()   |  Récupérer des données       |
| **POST** | http.post()	 | Envoyer des données | 
| **PUT**   | http.put()  | Mettre à jour des données   |
| **DELETE**   | http.delete()	  | Supprimer des données  |  
| **Gestion d'erreur**   | try-catch	 | Gérer les erreurs de réseau ou de serveur  |
| **Headers & Auth**   | Authorization header	  | Authentification via token |    
### 🔹  Gestion du JSON en Dart avec dart:convert
En Flutter (et en Dart), les données des API sont souvent sous format JSON. Pour traiter ces données, on utilise le package intégré dart:convert.
**📌 Exemple : Conversion JSON → Dart**
```dart
String jsonString = '{"nom": "Alice", "age": 25, "ville": "Paris"}';

// Convertir la chaîne JSON en Map Dart
Map<String, dynamic> data = jsonDecode(jsonString);

print(data["nom"]);   // Alice
print(data["age"]);   // 25
print(data["ville"]); // Paris
```
**Convertir un Objet Dart en Chaîne JSON (jsonEncode)**
Si on veut envoyer des données à une API, on doit convertir un objet Dart en chaîne JSON.
```dart
Map<String, dynamic> utilisateur = {
  "nom": "Alice",
  "age": 25,
  "ville": "Paris"
};

// Convertir l'objet Dart en JSON
String jsonString = jsonEncode(utilisateur);

print(jsonString); // {"nom":"Alice","age":25,"ville":"Paris"}
```
**Gérer une Liste d’Objets JSON**
Les API renvoient souvent des listes JSON (tableaux). On doit les convertir en List<Map<String, dynamic>>.
```dart
String jsonString = '''
[
  {"nom": "Alice", "age": 25},
  {"nom": "Bob", "age": 30}
]
''';

// Convertir en liste Dart
List<dynamic> utilisateurs = jsonDecode(jsonString);

for (var utilisateur in utilisateurs) {
  print(utilisateur["nom"]); // Alice, puis Bob
}
```
**Convertir JSON en Objet Dart avec une Classe (fromJson)**
Pour mieux gérer les données JSON, on peut utiliser des classes Dart.
```dart
class Utilisateur {
  String nom;
  int age;

  Utilisateur({required this.nom, required this.age});

  // Factory pour convertir JSON → Objet Dart
  factory Utilisateur.fromJson(Map<String, dynamic> json) {
    return Utilisateur(
      nom: json["nom"],
      age: json["age"],
    );
  }
}

void main() {
  String jsonString = '{"nom": "Alice", "age": 25}';
  Map<String, dynamic> jsonData = jsonDecode(jsonString);

  Utilisateur utilisateur = Utilisateur.fromJson(jsonData);
  print(utilisateur.nom); // Alice
}
```
**Convertir un Objet Dart en JSON (toJson)**
Si on veut envoyer un objet à une API, il faut le convertir en JSON.
```dart
class Utilisateur {
  String nom;
  int age;

  Utilisateur({required this.nom, required this.age});

  // JSON → Objet Dart
  factory Utilisateur.fromJson(Map<String, dynamic> json) {
    return Utilisateur(
      nom: json["nom"],
      age: json["age"],
    );
  }

  // Objet Dart → JSON
  Map<String, dynamic> toJson() {
    return {
      "nom": nom,
      "age": age,
    };
  }
}

void main() {
  Utilisateur utilisateur = Utilisateur(nom: "Alice", age: 25);
  
  // Convertir en JSON
  String jsonString = jsonEncode(utilisateur.toJson());

  print(jsonString); // {"nom":"Alice","age":25}
}
```
### 🔹 Utilisation d’une Base de Données Locale en Flutter avec sqflite et Hive
Lorsque vous développez une application Flutter, vous pouvez avoir besoin de stocker des données localement (hors ligne). Deux solutions populaires existent :

- sqflite : Une base de données SQLite pour des données structurées (relationnelles).
- Hive : Une base de données NoSQL rapide, idéale pour stocker des objets simples.
**🎯 1️⃣ Utilisation de sqflite (Base de Données SQLite)**
📌 Quand utiliser sqflite ?
- Si vous avez besoin de relations entre données.
- Si vous voulez effectuer des requêtes SQL.
**➤ Installation de sqflite et path_provider**
  Ajoutez ces dépendances dans pubspec.yaml :
```dart
dependencies:
  flutter:
    sdk: flutter
  sqflite: ^2.3.0
  path_provider: ^2.1.2  # Pour stocker la BD dans un bon emplacement
```
Ensuite, exécutez la commande :
```sh
flutter pub get
```
**➤ Configuration de la base de données**
Dans database_helper.dart, créez une classe pour gérer SQLite :
```dart
import 'package:sqflite/sqflite.dart';
import 'package:path/path.dart';

class DatabaseHelper {
  static Database? _database;
  static final DatabaseHelper instance = DatabaseHelper._privateConstructor();

  DatabaseHelper._privateConstructor();

  Future<Database> get database async {
    if (_database != null) return _database!;
    _database = await _initDatabase();
    return _database!;
  }

  Future<Database> _initDatabase() async {
    String path = join(await getDatabasesPath(), 'app_database.db');
    return await openDatabase(
      path,
      version: 1,
      onCreate: _onCreate,
    );
  }

  Future<void> _onCreate(Database db, int version) async {
    await db.execute('''
      CREATE TABLE users(
        id INTEGER PRIMARY KEY AUTOINCREMENT,
        name TEXT NOT NULL,
        age INTEGER NOT NULL
      )
    ''');
  }
}
```
**📌 Explication :**

- getDatabasesPath() : Trouve le chemin où enregistrer la BD.
- openDatabase() : Ouvre la BD et la crée si elle n’existe pas.
- onCreate : Crée la table users avec id, name, et age.
**➤ Insérer des données**
Ajoutez cette méthode à DatabaseHelper :
```dart
Future<int> insertUser(Map<String, dynamic> user) async {
  Database db = await database;
  return await db.insert('users', user);
}
```
Utilisation :
```dart
await DatabaseHelper.instance.insertUser({
  'name': 'Alice',
  'age': 25
});
```
**➤ Lire les données**
```dart
Future<List<Map<String, dynamic>>> getUsers() async {
  Database db = await database;
  return await db.query('users');
}
```
Utilisation :
```dart
List<Map<String, dynamic>> users = await DatabaseHelper.instance.getUsers();
print(users);
```
**➤ Mettre à jour des données**
```dart
Future<int> updateUser(int id, Map<String, dynamic> user) async {
  Database db = await database;
  return await db.update('users', user, where: 'id = ?', whereArgs: [id]);
}
```
**➤ Supprimer un utilisateur**
```dart
Future<int> deleteUser(int id) async {
  Database db = await database;
  return await db.delete('users', where: 'id = ?', whereArgs: [id]);
}
```
**🎯 2️⃣ Utilisation de Hive (Base de Données NoSQL)**
📌 Quand utiliser Hive ?
- Si vous voulez stocker des objets rapidement.
- Si vous n'avez pas besoin de relations complexes.
Pour les performances élevées.
**➤ Installation de Hive**
Ajoutez les dépendances dans pubspec.yaml :
```dart
dependencies:
  flutter:
    sdk: flutter
  hive: ^2.2.3
  hive_flutter: ^1.1.0

dev_dependencies:
  hive_generator: ^2.0.0
  build_runner: ^2.4.6
```
Puis, exécutez :
```sh
flutter pub get
```
**➤ Configuration de Hive**
Ajoutez cette ligne dans main.dart :
```dart
import 'package:hive_flutter/hive_flutter.dart';

void main() async {
  await Hive.initFlutter();
  runApp(MyApp());
}
```
**➤ Créer un Modèle avec Hive**
Hive utilise des adapters pour stocker des objets.
Créez user.dart :
```dart
import 'package:hive/hive.dart';

part 'user.g.dart'; // Nécessaire pour générer le code

@HiveType(typeId: 0)
class User extends HiveObject {
  @HiveField(0)
  String name;

  @HiveField(1)
  int age;

  User({required this.name, required this.age});
}
```
Puis, exécutez :
```sh
flutter pub run build_runner build
```
Cela générera un fichier user.g.dart.
**➤ Ouvrir une Boîte (Base de Données)**
```dart
Future<void> openBox() async {
  await Hive.openBox<User>('users');
}
```
**➤ Insérer un Utilisateur**
```dart
var box = Hive.box<User>('users');
box.add(User(name: "Alice", age: 25));
```
**➤ Lire les Données**
```dart
var users = Hive.box<User>('users').values.toList();
for (var user in users) {
  print(user.name);
}
```
**➤ Mettre à Jour un Utilisateur**

```dart
User user = box.getAt(0);
user.name = "Alice Updated";
user.save();
```
**➤ Supprimer un Utilisateur**
```dart
box.deleteAt(0);
```

**🎯 Comparaison : sqflite vs Hive**
| 🎯 Critère	 | sqflite	 | Hive
|-----------|--------|---------------|
| **Type**   | Base SQL   | Base NoSQL       |
| **Complexité** | Complexe (SQL)	 | Simple (objets) | 
| **Performance**   | Moyen  | Très rapide   |
| **Relations entre données**   | ✅ Oui		  | ❌ Non  |  
| **Taille des données**   | Grande	 | Petite  |  

**7️⃣ Détection de Tous les Gestes**
GestureDetector peut gérer plusieurs événements en même temps.
```dart
GestureDetector(
  onTap: () => print("Tap détecté"),
  onDoubleTap: () => print("Double Tap détecté"),
  onLongPress: () => print("Pression Longue détectée"),
  onVerticalDragUpdate: (details) => print("Glissement Vertical détecté"),
  child: Container(
    width: double.infinity,
    height: 200,
    color: Colors.lightBlue,
    child: Center(child: Text("Interagissez avec moi")),
  ),
)
```
### 🔹 Firebase dans Flutter : Firestore & Authentification
Firebase est un Backend-as-a-Service (BaaS) qui fournit plusieurs services comme Firestore (base de données NoSQL) et l'authentification utilisateur.

- 🔹 Firestore → Base de données NoSQL en temps réel.
- 🔹 Authentication → Connexion via e-mail, Google, Facebook, etc.
**1️⃣ Configuration de Firebase dans Flutter**
**📌 Étape 1 : Créer un projet Firebase**
- Allez sur Firebase Console et créez un projet.
- Ajoutez une application Flutter (Android & iOS).
- Téléchargez et ajoutez les fichiers google-services.json (Android) et GoogleService-Info.plist (iOS).
**📌 Étape 2 : Installer Firebase dans Flutter**
- Ajoutez ces dépendances dans pubspec.yaml :
```dart
dependencies:
  flutter:
    sdk: flutter
  firebase_core: latest_version
  cloud_firestore: latest_version
  firebase_auth: latest_version
```
Puis exécutez :
```sh
flutter pub get
```
**📌 Étape 3 : Initialiser Firebase**
- Modifiez main.dart :
```dart
import 'package:firebase_core/firebase_core.dart';
import 'package:flutter/material.dart';

void main() async {
  WidgetsFlutterBinding.ensureInitialized();
  await Firebase.initializeApp();
  runApp(MyApp());
}
```
**✅ Firebase est maintenant prêt à être utilisé !**
**2️⃣ Firestore : Base de Données NoSQL**
- Firestore permet de stocker et récupérer des données
**📌 Ajouter des Données**
```dart
import 'package:cloud_firestore/cloud_firestore.dart';

void addUser(String name, int age) {
  FirebaseFirestore.instance.collection('users').add({
    'name': name,
    'age': age,
    'createdAt': FieldValue.serverTimestamp(),
  });
}
```
**📌 Lire les Données**
```dart
void getUsers() async {
  QuerySnapshot querySnapshot =
      await FirebaseFirestore.instance.collection('users').get();

  for (var doc in querySnapshot.docs) {
    print(doc.data());
  }
}
```

**📌 Lire les Données en Temps Réel**
```dart
void listenToUsers() {
  FirebaseFirestore.instance.collection('users').snapshots().listen((snapshot) {
    for (var doc in snapshot.docs) {
      print(doc.data());
    }
  });
}
```
**📌 Explication :**
- .snapshots().listen() permet d'écouter les changements en temps réel.
**📌 Mettre à Jour un Document**
```dart
void updateUser(String userId, String newName) {
  FirebaseFirestore.instance.collection('users').doc(userId).update({
    'name': newName,
  });
}
```
**📌 Supprimer un Document**
```dart
void deleteUser(String userId) {
  FirebaseFirestore.instance.collection('users').doc(userId).delete();
}
```
**3️⃣ Authentification Firebase**
- Firebase Auth permet de gérer la connexion des utilisateurs.
**📌 Inscription par Email & Mot de Passe**
```dart
import 'package:firebase_auth/firebase_auth.dart';

Future<void> signUp(String email, String password) async {
  try {
    UserCredential userCredential = await FirebaseAuth.instance
        .createUserWithEmailAndPassword(email: email, password: password);
    print("Utilisateur créé : ${userCredential.user!.uid}");
  } catch (e) {
    print("Erreur : $e");
  }
}
```
**📌 Connexion par Email & Mot de Passe**
```dart
Future<void> signIn(String email, String password) async {
  try {
    UserCredential userCredential = await FirebaseAuth.instance
        .signInWithEmailAndPassword(email: email, password: password);
    print("Connecté : ${userCredential.user!.uid}");
  } catch (e) {
    print("Erreur : $e");
  }
}
```

**📌 Déconnexion**
```dart
Future<void> signOut() async {
  await FirebaseAuth.instance.signOut();
  print("Déconnecté !");
}
```
**📌 Vérifier l'État de Connexion**
```dart
void checkAuthState() {
  FirebaseAuth.instance.authStateChanges().listen((User? user) {
    if (user == null) {
      print("Utilisateur déconnecté");
    } else {
      print("Utilisateur connecté : ${user.uid}");
    }
  });
}
```
**📌 Connexion avec Google**
```dart
import 'package:firebase_auth/firebase_auth.dart';
import 'package:google_sign_in/google_sign_in.dart';

Future<void> signInWithGoogle() async {
  try {
    final GoogleSignInAccount? googleUser = await GoogleSignIn().signIn();
    final GoogleSignInAuthentication googleAuth = await googleUser!.authentication;

    final AuthCredential credential = GoogleAuthProvider.credential(
      accessToken: googleAuth.accessToken,
      idToken: googleAuth.idToken,
    );

    UserCredential userCredential =
        await FirebaseAuth.instance.signInWithCredential(credential);

    print("Utilisateur connecté : ${userCredential.user!.displayName}");
  } catch (e) {
    print("Erreur : $e");
  }
}
```

## 9. Animations et Effets Visuels
### 🔹 Animation simple avec AnimatedContainer
```dart
AnimatedContainer(
  duration: Duration(seconds: 1),
  width: _isExpanded ? 200 : 100,
  height: _isExpanded ? 200 : 100,
  color: _isExpanded ? Colors.blue : Colors.red,
)
```
### 🔹 Animation avancée avec Hero
```dart
Hero(
  tag: "imageTag",
  child: Image.asset("assets/image.png"),
)
```
## 9. Déploiement et Optimisation
### 🔹 Générer un APK
```sh
flutter build apk
```
### 🔹 Publier sur le Play Store
- Générer une clé de signature
- Modifier android/app/build.gradle
- Compiler l’APK et l’envoyer sur Google Play Console

https://chatgpt.com/share/682a0ae5-23f0-8000-8a85-c779175631fc
https://chatgpt.com/share/6833062f-2e94-8000-9451-47ee3baaa682
