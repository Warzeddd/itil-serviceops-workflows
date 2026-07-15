# Enterprise Inventory & Retail Management Portal

Une application web d'administration d'inventaire et de gestion de commandes, développée en architecture découplée avec **Next.js**, des **Server Actions** et un modèle d'accès aux données de type **DAO (Data Access Object)**.

---

## 🛠️ Stack Technique & Architecture Logicielle

* **Frontend Framework** : Next.js (App Router) exploitant le rendu hybride (Static & Dynamic) pour une navigation fluide et performante.
* **UI/UX Design** : Construit à l'aide de **NextUI** et **Tailwind CSS**, offrant une interface d'administration épurée, responsive et accessible.
* **Server Actions** : Gestion asynchrone des formulaires et des mutations de données sans chargement de page (`clientActions`, `orderActions`, `productActions`), garantissant une expérience utilisateur moderne.
* **Data Access Layer (DAO)** : Séparation stricte de la logique métier et de la persistance via un pattern DAO (`dao_client`, `dao_order`, `dao_product`), assurant un typage robuste côté backend.

---

## 🔒 Focus Cybersécurité & Hardening

* **Prévention des Injections (SQLi)** : Les Data Access Objects (DAOs) sont isolés et utilisent des requêtes préparées paramétrées (`dao_connection.ts`), neutralisant les risques d'exploitation de vulnérabilités SQL (OWASP Top 10 - Injection).
* **Isolation des Configurations** : Gestion stricte des variables d'environnement via un fichier `.env` privé, éliminant tout risque de fuite d'identifiants (*hardcoded credentials*) sur le dépôt distant.
* **Typage Stricte TypeScript** : Implémentation de définitions de types exhaustives (`.d.ts`) pour toutes les entités métiers (Client, Line, Order, Product), prévenant les comportements instables de l'application en production.

---

## 📊 Structure des Données (Modèle Relationnel)

L'application organise les flux commerciaux à travers une modélisation transactionnelle normalisée :
* **Client** : Profil des acheteurs professionnels ou particuliers.
* **Product** : Catalogue de l'inventaire avec tarification et description dynamique.
* **Order** : En-tête des transactions liant les clients aux commandes de vente.
* **Line** : Lignes d'association de commande, définissant la quantité et le prix unitaire d'un produit spécifique au sein d'une transaction parent.

---

## 📂 Architecture des Dossiers

```text
.
├── actions/                  # Couche d'orchestration (Server Actions pour les mutations)
├── app/                      # Routage applicatif Next.js et API endpoints d'intégration
├── component/                # Composants réutilisables d'interface (Navbar, Providers, Connectors)
├── constants/                # Déclaration des routes et constantes globales
├── dao/                      # Data Access Objects (Requêtes préparées d'accès à la base de données)
├── public/                   # Assets graphiques statiques
└── types/                    # Déclarations de types TypeScript strictes
