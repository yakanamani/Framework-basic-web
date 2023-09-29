# _**A venir prochainement**_

[![Basic Web Framework](/docs/Basic_web_framework.png)]()

## Cucumber BDD Framework with Selenium, TestNG and Java

### Sommaire:

🏷️ [Architecture et Présentation du framework](#Architecture-et-Présentation-du-framework)<br/>
🏷️ [Fonctionnalités](#fonctionnalités)<br/>
🏷️ [Prérequis avant installation](#prérequis-avant-installation)<br/>
🏷️ [Comment installer le framework](#comment-installer-le-framework)<br/>
🏷️ [Comment exécuter le framework](#comment-exécuter-le-framework)<br/>
🏷️ [Comment consulter les rapports](#comment-consulter-les-rapports)<br/>
🏷️ [Comment étendre le framework](#comment-étendre-le-framework)<br/>
🏷️ [Comment maintenir le framework](#comment-maintenir-le-framework)<br/>
🏷️ [Comment déboguer le framework](#comment-déboguer-le-framework)<br/>

### 🎯Architecture et Présentation du framework

````
📦BasicWebFramework
┃ ┣ 📂allure-report
┃ ┃ ┗ 📑index.html
┣ 📂docs
┣ 📂Drivers
┣ 📂src
┃ ┣ 📂test
┃ ┃ ┣ 📂java
┃ ┃ ┃ ┗ 📂testng
┃ ┃ ┃ ┃ ┗ 📂automation
┃ ┃ ┃ ┃ ┃ ┣ 📂base
┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜BasePage.java
┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜BaseTest.java
┃ ┃ ┃ ┃ ┃ ┣ 📂constants
┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜DriverType.java
┃ ┃ ┃ ┃ ┃ ┣ 📂factory
┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜DriverManager.java
┃ ┃ ┃ ┃ ┃ ┣ 📂objects
┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜BillingAddress.java
┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜Product.java
┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜User.java
┃ ┃ ┃ ┃ ┃ ┣ 📂pages
┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜CartPage.java
┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜CheckoutPage.java
┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜HomePage.java
┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜StorePage.java
┃ ┃ ┃ ┃ ┃ ┣ 📂tests
┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜CaseTest.java
┃ ┃ ┃ ┃ ┃ ┣ 📂utils
┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜JacksonUtils.java
┃ ┃ ┣ 📂resources
┃ ┃ ┃ ┗ 📑myBillingAddress.json
┃ ┃ ┃ ┗ 📑products.json
┃ ┃ ┣ 📂target
┃ ┃ ┃ ┗ 📂allure-results
┣ 📑pom.xml
┣ 📑README.md
┣ 📑testng.xml
````

Si vous souhaitez tester une application web de préférence (un ecommerce).</br>
🌟Si vous êtes `TESTEUR AUTOMATICIEN` et que vous voulez apprendre à automatiser des tests fonctionnels.</br>
🌟Si vous êtes un  `RECRUTEUR` pour évaluer les compétences de nos testeurs automaticiens talentueux.</br>
🌟 Ou encore si vous êtes un `PARTICULIER`ou une `ENTREPRISE` à la recherche de solution
répondant à vos besoins d'automatisation en test alors ce framework est fait pour vous!</br></br>

🎁 Ce framework permet d'exécuter vos tests en séquentiel sur le navigateur de votre choix, 
soit `Chrome`, `Firefox`, `Opera`, `Edge` ou `Safari`.</br>
🎁 Il s'exécute également sur plusieurs plateformes comme : `Windows 10` et `Mac`.</br>

### 🎯Fonctionnalités
✅ Java 11<br/>
✅ Selenium 4<br/>
✅TestNG<br/>
✅ Data Driven Testing (Json)<br/>
✅ Page Object Model<br/>
✅ Allure Report<br/>
✅ Exécution séquentielle de tests <br/><br/>

[![My Skills](https://skillicons.dev/icons?i=java,selenium,gherkin,idea)](https://skillicons.dev)

### 🎯Prérequis avant installation

####  🔴 Sur PC Mac

```  bash
   💊 HOMEBREW [Mac]
   🔹Télécharger et installer homebrew (si pas déjà installé): 
    ♾️ /bin/bash -c “$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)”
    ♾️ brew update
```

```
  💊 JAVA 11 [Mac]
  🔹Télécharger et installer Java 11 (openJdk11): 
   ♾️ brew install java11
   ♾️ sudo ln -sfn /usr/local/opt/openjdk@11/libexec/openjdk.jdk /Library/Java/JavaVirtualMachines/openjdk-11.jdk
  🔹Configurer java home: 
   ♾️ export JAVA_HOME = /Library/Java/Home
  🔹Vérifier la version de java: 
   ♾️ java --version
```

```
  💊MAVEN 3.8.6 [Mac]
  🔹 Installer sur Mac à partir du terminal: 
   ♾️ brew install maven
  🔹Configurer les variables d'environment:
      export M2_HOME=/usr/local/apache-maven/apache-maven-3.8.4 
      export M2 = $M2_HOME/bin
      export MAVEN_OPTS = -Xms256m -Xmx512m
```
⚓Installez [Java via HomeBrew sur Mac](https://medium.com/@kirebyte/using-homebrew-to-install-java-jdk11-on-macos-2021-4a90aa276f1c)

```
    💊Allure 2 [Mac - Terminal]  
    ♾️ brew install allure
```
⚓ Installer [Allure via Homebrew](https://brew.sh/)

##### 📮 NAVIGATEURS [A installer]<br/>
🔹[Mac] ➡️ [Safari](https://support.apple.com/downloads/safari), [Chrome](https://setapp.com/how-to/install-google-chrome-for-mac-quickly), [Firefox](https://support.mozilla.org/en-US/kb/how-download-and-install-firefox-mac), [Opera](https://www.opera.com/fr/browsers/opera) et [Edge](https://www.youtube.com/watch?v=FgbXQbBQc_Q).<br/>
🔹[Windows] ➡️ [Chrome](https://www.google.com/chrome/?brand=BNSD&gclid=CjwKCAjw-IWkBhBTEiwA2exyOzIzlgqqwM5oXGEipBtJ4uaCy-J6hSEMkv4jsP27bwUwqfQGxbkBiRoCs8oQAvD_BwE&gclsrc=aw.ds), [Firefox](https://support.mozilla.org/en-US/kb/how-install-firefox-windows), [Opera](https://www.opera.com/fr/browsers/opera) et Edge (Installé par défaut).

####  🔴 PC WINDOWS

#### Liens de téléchargement :<br/>
⚓[Téléchargez](https://maven.apache.org/download.cgi) et [Installez](https://maven.apache.org/install.html) Maven<br/>
⚓[Téléchargez](https://www.oracle.com/eg/java/technologies/javase/jdk11-archive-downloads.html) et [Installez](https://www.youtube.com/watch?v=SQykK40fFds) Java 11<br/>

```
  💊Allure 2 [Windows - Terminal]  
   ♾️ scoop install allure
```
⚓ Installer [Allure via Windows](https://scoop.sh/)

### 🎯Comment installer le framework

📌Téléchargez le repo zip du projet sur gitlab :
[![download_zip](/docs/download-zip.png "download zip")]()

📌Ouvrez le projet dans votre IDE :</br>
+ Faîtes un `mvn clean` </br></br>
  [![mvn_clean](/docs/mvn_clean.png "build project")]()

* Faîtes un ⚠️`build project` et exécutez-le.</br></br>
  [![build-project](/docs/build-project.png "build project")]()

### 🎯Comment exécuter le framework

🔶Exécution séquentiel </br>
Ce framework exécute les tests en séquentiel sur le navigateur ⚠️chrome, via:<br/>

``` bash
 📌Ouvrir le terminal [Git Bash] et saisir la commande suivante:
 🔸 mvn clean test && allure generate target/allure-results --clean -o allure-report
```

🟥 NB: POUR EXÉCUTER CE FRAMEWORK, VOUS DEVEZ AVOIR UNE BONNE CONNEXION INTERNET !

``` 
⛔ Si toute fois, après avoir suivi les étapes d'installation et d'exécution de ce framework,
   vous rencontrez des erreurs, cela est sûrement dû à un faible débit de votre connexion internet ! 
   Et pour résoudre ce problème, suivez les étapes de débogages dans l'étape [Comment déboguer le framework] ⬇️.
```

### 🎯Comment consulter les rapports
Consulter le rapport allure en ouvrant le fichier `index.html` dans votre navigateur, à partir du dossier `test-output/index.html`.
[![allure-report](/docs/allure-report.png "allure-report")]()</br>

###  🎯Comment étendre le framework
* Ce framework vous permet d'effectuer des tests fonctionnels d'interface Utilisateurs (UI) sur une application web d'ecommerce [AskOmDch](https://askomdch.com/store/), les scenarios exécutés ici sont les suivants: <br/><br/>
  ✴️ Rechercher un produit 
   ```
   je veux accéder à la page web `https://askomdch.com/store
   Je veux rechercher un produit avec un mot partiel(Blue)
   Puis je vois le produit recherché s'affiché
   ```
  ✴️ Un invité peut commander un produit
  ```
  En tant qu'un visiteur du site
  J'ajoute un produit au panier
  Je vais à la page de vérification
  je saisis mes données de carte bancaire
  Je passe la commande de mon produit
  Ma commande est effectuée avec succès
  ```

#### 🛠️Création d'un test

🪙 Ajout de nouveaux tests

* Dans le repertoire ⚠tests, ouvrir le fichier CaseTest où l'on souhaite ajouter des tests.
 ```
  📌Dans le répertoire [tests]: ouvrir le fichier 
   🔸CaseTest: rajouter des tests
 ```

🪙 Rédiger un test, comme suit :
``` 
  📌Example
    🔸@Test
    public void newTest() {
    
    }
```

🪙Rédaction des fonctions objets `Page Objects`

* Dans ce framework, nous utilisons le modèle ⚠️Page Object </br>
* vous pouvez soit ajouter vos scripts de tests dans les pages objects déjà présentes 
   ou en créer des nouvelles selon la page concernée par le scénario à exécuter.</br>
  * ex : Si vous voulez ajouter au panier un produit qui se trouve sur la page `Men` 
  de l'[ecommerce](https://askomdch.com/product-category/men/), alors vous devrez ajouter
 un `Page Object` pour cette page et les autres et pour toutes les autres pages concernées par le scénario en question.

  * Et définir les `locators` des éléments d'interface utilisateurs (IU) présents sur cette page ou les autres concernant le scénario à exécuter 
  * puis définir les actions à effectuer sur ces éléments.
```
 🔸 StorePage.java 
    ➡️ /src/test/java/testng/automation/pages/StorePage.java
 🔸 CartPage.java 
    ➡️ /src/test/java/testng/automation/pages/CartPage.java
 🔸 CheckoutPage.java
    ➡️ /src/test/java/testng/automation/pages/CheckoutPage.java
```

🟥 NB : Pour ajouter un nouveau test correspondant à l'une
de nos fonctionnalités déjà développées dans ce framework,
vous pouvez ajouter le tag`@Test` au nouveau test et le lancer pour le voir s'exécuter !

* voici un example de test à ajouter: </br>
[![addTest](/docs/ExpleTest.png "addTest")]()</br>

### 🎯Comment maintenir le framework

🪙 Ajout d'un nouveau navigateur dans le fichier TestNG

[![addTest](/docs/AjoutTest.png "addTest")]()</br>

### 🎯Comment déboguer le framework
 
```
💡 Si vous rencontrez une erreur de ⚠️build Failed❌ 
```
* Pour résoudre tous ces problèmes, relancez de nouveau les tests !
```
 ➡️Faîtes un [mvn clean] {dans l'onglet Maven ou  en console}
 ➡️ Puis faîtes un [build project] {Dans l'onglet Build d'Intellij}
```
