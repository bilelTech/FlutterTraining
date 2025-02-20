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

# 🚀 Formation Complète sur Flutter - Les Fondamentaux  

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
- Text() → Afficher du texte
- Container() → Boîte avec padding, margin, background
- Row() et Column() → Disposition horizontale et verticale
- ListView() → Liste scrollable
- Image.asset() / Image.network() → Affichage d’images
Exemple :
```dart
Column(
  children: [
    Text("Bienvenue dans Flutter!"),
    Image.network("https://flutter.dev/assets/homepage/logo.png"),
  ],
)
```
## 4. Navigation entre les écrans
Flutter utilise Navigator pour gérer les transitions entre les pages.
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
## 5. Gestion de l’état
Il existe plusieurs façons de gérer l’état d’une application Flutter :
🔹 **setState()** → Gestion d’état locale
```dart
setState(() {
  _counter++;
});
```
🔹 Provider → Gestion d’état globale
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
## 6. Connexion à une API REST et Firebase
### 🔹 Consommer une API REST
```dart
Future<void> fetchData() async {
  final response = await http.get(Uri.parse("https://api.example.com/data"));
  if (response.statusCode == 200) {
    print(response.body);
  }
}
```
🔹 Intégration Firebase
- Authentification Firebase (Google, Facebook, Email)
- Firestore Database (Stockage en temps réel)
Exemple : Connexion avec Firebase Authentication
```dart
UserCredential user = await FirebaseAuth.instance.signInWithEmailAndPassword(
  email: "user@example.com",
  password: "password123",
);
```
## 7. Animations et Effets Visuels
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
## 8. Déploiement et Optimisation
### 🔹 Générer un APK
```sh
flutter build apk
```
### 🔹 Publier sur le Play Store
- Générer une clé de signature
- Modifier android/app/build.gradle
- Compiler l’APK et l’envoyer sur Google Play Console


