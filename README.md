#  TP2 – Architecture à Trois Couches avec Spring

##  Description du projet

Ce projet illustre une **architecture en couches** basée sur le framework **Spring**, composée de trois parties principales :

- **DAO (Data Access Object)** : gestion des données et de la couche d’accès aux sources de données.  
- **Métier (Service)** : logique de traitement des données et implémentation des règles métier.  
- **Présentation** : point d’entrée de l’application, permettant d’exécuter et de tester l’intégration des couches DAO et Métier.

L’objectif du TP est de comprendre et d’implémenter les mécanismes d’**injection de dépendances** et de **configuration Spring** via les annotations.

---

##  Structure du projet
**src/
└── main/
└── java/
└── org/
└── example/
***├── dao/
│ ├── IDao.java
│ ├── DaoImpl.java
│ └── DaoImpl2.java
***├── metier/
│ ├── IMetier.java
│ └── MetierImpl.java
***└── presentation/
├── Presentation1.java
├── Presentation2.java
└── PresentationXML.java

---

##  Technologies utilisées

- **Java 17+**  
- **Spring Framework (Core / Context)**  
- **Maven** ou **Gradle** (selon la configuration du projet)  
- **IntelliJ IDEA** ou tout autre IDE Java compatible

---

##  Principes mis en œuvre

- Injection de dépendances par **annotations** :
  - `@Component`
  - `@Autowired`
  - `@Configuration`
  - `@ComponentScan`
- Utilisation du **contexte Spring** avec :
  ```java
  AnnotationConfigApplicationContext context = new AnnotationConfigApplicationContext();
  context.register(Presentation2.class);
  context.refresh();


