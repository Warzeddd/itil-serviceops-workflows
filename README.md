# IT Service Management (ITSM) & ITIL v4 Compliance Workflow

Ce dépôt rassemble les livrables d'ingénierie ITSM, de gouvernance informatique et de processus de gestion des incidents basés sur le référentiel **ITIL v4** via la solution **GLPI**[cite: 3]. 

---

## 🏗️ Architecture & Composants du Répertoire

* **`/database`** : Schéma relationnel d'indexation SQL de la base de données de ticketing de production (`ticket_db_schema.sql`).
* **`/documentation`** : Documents de gouvernance, politiques d'utilisation des systèmes (AUP), logigrammes d'escalade d'incidents (SLA/Slo) et guides opérationnels de sensibilisation de l'utilisateur final.
* **`/presentation`** : Support de formation et d'onboarding technique sur l'outil de gestion de parc et de ticketing GLPI.

---

## 🛡️ Processus de Support & Alignement Cyber

L'intégralité du cycle de vie des requêtes a été modélisée selon les directives ITIL v4 afin de maximiser la disponibilité opérationnelle des systèmes :
1. **Incident Management (N1/N2/N3)** : Logigramme complet de qualification, de priorisation automatique (Matrice d'Urgence / Impact) et de résolution des pannes critiques.
2. **Acceptable Use Policies (AUP)** : Charte de conformité régissant l'usage éthique et sécurisé de l'Intelligence Artificielle en entreprise.
3. **User Awareness Program** : Manuel technique de sensibilisation au Phishing et ingénierie sociale pour endiguer le vecteur d'attaque d'intrusion initial le plus critique (Human-as-a-Security-Sensor).

---

## 📂 Structure du Dépôt

```text
.
├── database/                    # Schéma relationnel de la base SQL (GLPI Ticketing)
├── documentation/               # logigrammes, chartes de conformité et guides de gestion de crise (SOPs)
└── presentation/                # Slides techniques de formation utilisateur et d'onboarding sur GLPI
