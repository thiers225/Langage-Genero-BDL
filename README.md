# 📚 Cursus de Formation Complet : Langage Genero BDL

Bienvenue dans le dépôt de référence dédié à l'apprentissage et à la maîtrise du langage **Genero BDL** (*Business Development Language*), la plateforme de développement 4GL à haute productivité développée par **Four Js Development Tools**.

Ce cursus pédagogique a été structuré pour accompagner les développeurs depuis les concepts de base et l'architecture DVM jusqu'aux patrons d'ingénierie logicielle avancés (niveaux **Middle** et **Senior**).

---

## 🗂️ Table des Matières du Dépôt

Le cursus est composé de deux guides de référence complets au format Markdown :

| Document | Niveau | Description & Concepts Clés |
| :--- | :--- | :--- |
| 📘 [**cours-bases-genero-bdl.md**](./1.cours-bases-genero-bdl.md) | **Débutant / Fondamentaux** | Architecture DVM/AUI/ODI, environnement Genero Studio, syntaxe BDL, types de données (`RECORD`, `ARRAY`), formulaires `.per`, instructions `DISPLAY`/`INPUT`, intégration SQL de base. |
| 📙 [**cours-avance-genero-bdl.md**](./2.cours-avance-genero-bdl.md) | **Middle & Senior** | Grilles `DISPLAY ARRAY`/`INPUT ARRAY`, bloc unifié `DIALOG`, transactions SQL & verrous, packages (`IMPORT FGL`), manipulation du DOM AUI, SOA REST/SOAP (GWS), Genero Report Writer (GRW). |

---

## 📖 Sommaire Récapitulatif du Programme

### 1. Module 1 : Bases du Langage Genero BDL (`cours-bases-genero-bdl.md`)
* **1. Architecture & Principes** : Découplage Logique / IHM, rôle de la Machine Virtuelle Dynamique (*Dynamic Virtual Machine* - DVM), de l'Interface Utilisateur Abstraite (*Abstract User Interface* - AUI) et de l'Interface de Base de Données Ouverte (*Open Database Interface* - ODI).
* **2. Environnement & Cycle de Vie** : Manipulation de Genero Studio (GST), workflow de compilation (`fglform`, `fglcomp`), types de fichiers (`.4gl`, `.per`, `.42m`, `.42f`, `.42r`).
* **3. Syntaxe & Structures** : Variables et portées (`LOCAL`, `MODULE`, `GLOBAL`), types primitifs et enregistrements (`RECORD`), structures de contrôle (`IF`, `CASE`, `FOR`, `WHILE`).
* **4. Formulaires & Interactions** : Conception des fichiers de masque `.per`, association variable-champ, commandes d'affichage et de saisie mono-enregistrement (`DISPLAY BY NAME`, `INPUT BY NAME`).
* **5. Accès aux Données SQL** : SQL statique et dynamique (`PREPARE`, `EXECUTE`), gestion des curseurs (`DECLARE`, `FOREACH`), contrôle des transactions (`BEGIN WORK`, `COMMIT WORK`, `ROLLBACK WORK`).

### 2. Module 2 : Niveau Avancé - Middle & Senior (`cours-avance-genero-bdl.md`)

#### Section Intermédiaire (Middle Developer)
* **1. Multi-Dialogues & Tableaux** : Navigation et édition dans les grilles (`DISPLAY ARRAY`, `INPUT ARRAY`), syntaxe du bloc interactif unifié `DIALOG`.
* **2. SQL Avancé & Concurrence** : Gestion des accès concurrents (`FOR UPDATE`, `LOCK MODE`), curseurs de mise à jour, pagination et optimisation des requêtes ODI.
* **3. Modularité & Robustesse** : Encapsulation avec `PACKAGE` et `IMPORT FGL`, gestion structurée des exceptions (`TRY...CATCH`), journalisation applicative.

#### Section Expert (Senior / Architecte)
* **4. Dynamic AUI & Manipulation DOM** : Inspection et modification dynamique de l'arbre XML AUI (`ui.Interface`, `om.DomNode`), contrôle des règles graphiques et styles à chaud.
* **5. Architectures SOA & Web Services** : Exposition et consommation de Services Web RESTful et SOAP via Genero Web Services (GWS), manipulation de documents XML (`om.DomDocument`).
* **6. Reporting d'Entreprise (GRW/GRE)** : Conception de rapports complexes avec Genero Report Writer, gestion des flux PDF sécurisés et conformité Factur-X.
* **7. Industrialisation & Déploiement** : Profils de déploiement multi-canaux (GDC desktop, GBC web, GMA/GMI mobile), tuning de la DVM et intégration continue.

---

## 💻 Prérequis Techniques & Environnement

Pour exécuter les programmes et compiler les exemples fournis dans les cours :

1. **Suite Logicielle Genero Enterprise** :
   * Compilateur Genero BDL (`fglcomp`) et compilateur de formulaires (`fglform`).
   * Moteur d'exécution DVM (`fglrun`).
   * Environnement de développement **Genero Studio**.
2. **Gestionnaire de Licences** :
   * Four Js License Manager (FLM) ou utilitaire de contrôle `fglWrt`.
3. **Système de Gestion de Base de Données (SGBD)** :
   * Compatible avec Informix, PostgreSQL, Oracle, Microsoft SQL Server, MySQL ou SQLite.
4. **Clients d'Affichage (Front-ends)** :
   * **GDC** (*Genero Desktop Client*) pour l'affichage natif lourd.
   * **GAS / GBC** (*Genero Application Server / Browser Client*) pour l'exécution dans un navigateur Web.

---

## 🚀 Prise en Main Rapide

### 1. Compilation d'un Formulaire `.per`
```bash
fglform mon_formulaire.per
# Génère le fichier binaire de formulaire : mon_formulaire.42f
```

### 2. Compilation d'un Module BDL `.4gl`
```bash
fglcomp mon_programme.4gl
# Génère le module binaire compilé : mon_programme.42m
```

### 3. Exécution avec la DVM
```bash
fglrun mon_programme.42r
# Lance la Dynamic Virtual Machine et ouvre l'interface sur le front-end configuré
```
