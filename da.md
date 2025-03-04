### **1. Collecte et préparation des données**  
#### **Ce que fait l'analyste** :  
- **Extrait les données** :  
  - Écrit des requêtes SQL pour récupérer des données des bases (ex : commandes des utilisateurs du mois dernier) :  
    ```sql
    SELECT user_id, SUM(order_amount) 
    FROM orders 
    WHERE order_date BETWEEN '2023-01-01' AND '2023-01-31'
    GROUP BY user_id;
    ```  
  - Utilise **Power Query** dans Excel pour se connecter à des sources (CSV, Google Sheets, bases de données).  

- **Nettoie les données** :  
  - Supprime les doublons dans Excel via *Données → Supprimer les doublons*.  
  - Corrige les formats de dates/chiffres dans Power BI avec des fonctions comme *Split Column*.  

#### **Outils** :  
  - SQL (DBeaver, accès direct aux bases), Excel, Power Query.  

---

### **2. Analyse des données**  
#### **Ce que fait l'analyste** :  
- **Calcule les métriques** :  
  - Calcule le taux de conversion, le panier moyen, le taux de rétention via des tableaux croisés dynamiques dans Excel.  
  - Utilise des formules Excel : `=SOMME.SI.ENS()`, `=RECHERCHEV()`, `=MOYENNE.SI()`.  

- **Effectue des tests A/B** :  
  - Compare les métriques de deux groupes avec un test t dans Excel (*Utilitaire d'analyse → Test t à deux échantillons*).  
  - Détermine si les différences sont statistiquement significatives (p-value < 0,05).  

- **Segmente l'audience** :  
  - Regroupe les utilisateurs par comportement dans Power BI en utilisant des filtres et des colonnes calculées.  

#### **Exemple** :  
  > *Tâche* : Identifier la région avec le ROI le plus élevé des campagnes marketing.  
  *Actions* :  
  1. Exporte les données des dépenses et revenus par région via SQL.  
  2. Calcule le ROI dans Excel : `=(Revenu - Dépense) / Dépense`.  
  3. Visualise le top 5 des régions dans Power BI.  

---

### **3. Visualisation et rapports**  
#### **Ce que fait l'analyste** :  
- **Crée des tableaux de bord** :  
  - Conçoit des rapports interactifs dans Power BI ou Tableau :  
    - Ajoute des filtres par date, région, produit.  
    - Utilise des graphiques : histogrammes, courbes de tendance, cartes.  
  - Configure la mise à jour automatique des données (ex : via Power BI Gateway).  

- **Prépare des présentations** :  
  - Exporte des graphiques de Power BI vers PowerPoint.  
  - Formule des conclusions en langage simple :  
    *« Le taux de conversion a augmenté de 15% après la modification de la page d'accueil. Nous recommandons de généraliser ces changements à toutes les régions. »*  

#### **Outils** :  
  - Power BI/Tableau, Excel (pour les tableaux intermédiaires), PowerPoint.  

---

### **4. Collaboration et communication**  
#### **Ce que fait l'analyste** :  
- **Discute des besoins** :  
  - Clarifie avec le responsable marketing les métriques à inclure dans le rapport (ex : CAC, LTV).  
  - Pose des questions : *« Faut-il inclure les retours de produits dans le calcul du LTV ? »*  

- **Explique les résultats** :  
  - Anime des réunions avec des équipes non techniques en utilisant les tableaux de bord comme support visuel.  
  - Répond à des questions comme : *« Pourquoi le panier moyen a-t-il baissé ce mois-ci ? »* (analyse les données et recherche des anomalies).  

---

### **5. Exemple d'emploi du temps**  
| **Heure**       | **Tâche**                                                                 |  
|-----------------|---------------------------------------------------------------------------|  
| 9h00–10h30      | Vérification des rapports automatiques dans Power BI, correction d'erreurs de mise à jour. |  
| 10h30–12h00     | Analyse des résultats d'un test A/B sur un nouveau bouton CTA dans Excel. |  
| 12h00–13h00     | Réunion avec l'équipe marketing : discussion des métriques clés pour le rapport trimestriel. |  
| 13h30–15h00     | Création d'un tableau de bord dans Tableau sur les ventes (filtres : région, catégorie de produit). |  
| 15h00–16h30     | Préparation d'une requête SQL pour exporter les données d'activité utilisateur. |  
| 16h30–17h30     | Finalisation d'une présentation avec les conclusions pour la direction. |  

---

### **6. Problèmes courants et solutions**  
- **Problème** : Données manquantes (ex : région non renseignée pour 20% des utilisateurs).  
  **Solution** : Remplace les valeurs manquantes par *« Non spécifié »* dans Power Query.  

- **Problème** : Le tableau de bord Power BI met trop de temps à charger.  
  **Solution** : Optimise les requêtes SQL, supprime les colonnes inutiles, active la mise en cache.  

---

### **7. Compétences clés** :  
1. **SQL** — Indispensable pour extraire les données de la base.  
2. **Power BI/Tableau** — Essentiels pour rendre les conclusions accessibles.  
3. **Statistiques** — Pour distinguer les tendances réelles des variations aléatoires.  
4. **Excel** — Pour des calculs rapides et des analyses préliminaires.  

Même sans programmation, vous pouvez accomplir 80% des tâches d'un analyste de données avec ces outils. L'essentiel est de comprendre le contexte métier et de poser les bonnes questions aux données 😊.  

=====================

### **1. Compétences et technologies clés**  
#### **a. Statistiques et analyse de données**  
- **À apprendre** :  
  - Bases des statistiques : moyenne, médiane, corrélation, régression.  
  - Tests d'hypothèses : valeur p, intervalles de confiance.  
  - A/B testing : calcul de la taille d'échantillon, interprétation des résultats.  
- **Ressources** :  
  - [**Fun-Mooc : Statistique pour tous**](https://www.fun-mooc.fr/fr/cours/statistique-pour-tous/)  
  - [**Khan Academy : Statistiques**](https://fr.khanacademy.org/math/statistics-probability)  

---

#### **b. SQL (obligatoire)**  
- **À apprendre** :  
  - Requêtes de base : `SELECT`, `JOIN`, `GROUP BY`.  
  - Agrégation : `SUM`, `COUNT`, `AVG`.  
  - Filtrage et tri.  
- **Ressources** :  
  - [**SQL.sh : Cours SQL**](https://sql.sh/cours)  
  - [**W3Schools : Tutoriel SQL**](https://www.w3schools.com/sql/) (traduire en français via le navigateur).  

---

#### **c. Visualisation de données**  
- **Outils** :  
  - **Power BI** : Création de dashboards, intégration avec Excel et SQL.  
  - **Tableau** : Visualisations interactives, filtres.  
  - **Excel/Google Sheets** : Tableaux croisés dynamiques, graphiques.  
- **Ressources** :  
  - [**Power BI : Apprendre les bases**](https://learn.microsoft.com/fr-fr/training/powerplatform/power-bi)  
  - [**Tableau : Tutoriels gratuits**](https://www.tableau.com/fr-fr/learn/training)  

---

#### **d. Outils de traitement de données**  
- **Excel Power Query** :  
  - Nettoyage de données, fusion de tableaux, automatisation ETL.  
- **Alteryx (version d'essai)** :  
  - Conception visuelle de flux ETL.  
- **Ressources** :  
  - [**Excel-Pratique : Power Query**](https://www.excel-pratique.com/fr/cours_excel/power-query)  
  - [**DataCamp : Introduction à Alteryx**](https://www.datacamp.com/)  

---

### **2. Plan d'apprentissage (6–12 mois)**  
#### **Étape 1 : Bases (3–4 mois)**  
- **SQL** : Maîtrisez les requêtes avec `JOIN` et agrégations.  
- **Excel/Google Sheets** : Tableaux croisés dynamiques, formules (`VLOOKUP`, `SUMIFS`).  
- **Statistiques** : Suivez un cours sur Fun-Mooc.  
- **Pratique** : Utilisez des jeux de données de [**data.gouv.fr**](https://www.data.gouv.fr/).  

#### **Étape 2 : Visualisation (3–4 mois)**  
- **Power BI/Tableau** : Créez 2–3 dashboards (ex : analyse des ventes).  
- **Projets** :  
  - Analyse des données COVID-19 : visualisez la dynamique des cas.  
  - Rapport de campagnes marketing : ROI, taux de conversion.  

#### **Étape 3 : Portfolio et recherche d'emploi (2–3 mois)**  
- **Portfolio** :  
  - Publiez vos dashboards sur [**Tableau Public**](https://public.tableau.com/) ou [**Power BI Service**](https://powerbi.microsoft.com/).  
  - Ajoutez des descriptions sur LinkedIn.  
- **Certifications** :  
  - [**Microsoft PL-300 (Power BI)**](https://learn.microsoft.com/fr-fr/certifications/power-bi-data-analyst-associate/)  
  - [**Tableau Desktop Specialist**](https://www.tableau.com/learn/certification)  

---

### **3. Ressources gratuites**  
- **Excel** :  
  - [**Excel Exercice**](https://www.excel-exercice.com/)  
- **SQL** :  
  - [**SQL Practice**](https://www.sql-practice.com/)  
- **Statistiques** :  
  - [**Statistiques pour données spatiales**](https://www.fun-mooc.fr/fr/cours/statistiques-pour-donnees-spatiales/)  

---

### **4. Exemples de projets**  
1. **Analyse des ventes dans Excel** :  
   - Utilisez des tableaux croisés dynamiques pour analyser le chiffre d'affaires par catégorie.  
   - Créez un graphique de saisonnalité.  

2. **Dashboard Power BI** :  
   - Importez des données depuis CSV ou Google Sheets.  
   - Ajoutez des filtres par date et région.  
   - Visualisez les KPI : panier moyen, taux de conversion.  

---

### **5. Conseils pour le travail à distance**  
- **Automatisation** : Utilisez Power BI Dataflows pour actualiser les données.  
- **Networking** :  
  - Rejoignez des groupes LinkedIn : *Data Analysis France*, *Power BI Community*.  
  - Participez aux webinaires Microsoft (ex : [**Power BI Days**](https://powerbiconference.com/)).  

---

### **6. Durée d'apprentissage**  
- **Débutant** : 8 à 12 mois (15–20 heures/semaine).  
- **Avec des bases en Excel** : 6–8 mois.  

---

### **Liens utiles**  
- [**Data.gouv.fr**](https://www.data.gouv.fr/)  
- [**Power BI Community**](https://community.powerbi.com/)  

Bon courage dans votre apprentissage ! 😊  
