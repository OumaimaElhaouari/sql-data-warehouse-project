# Data Warehouse SQL Server : CRM + ERP

Entrepôt de données construit avec **SQL Server** selon l'architecture **Medallion** (Bronze → Silver → Gold), à partir de six fichiers CSV issus de deux systèmes : un CRM et un ERP.

> Projet basé sur le projet pédagogique de [Data With Baraa](https://github.com/DataWithBaraa/sql-data-warehouse-project) (licence MIT), que j'ai adapté et amélioré.

## 🎯 Objectif

Consolider les données de ventes de deux sources dans un modèle propre, intégré et prêt pour l'analyse.

## 🏗️ Architecture


- **Bronze** : données brutes chargées depuis les CSV (`BULK INSERT`).
- **Silver** : données nettoyées et standardisées.
- **Gold** : modèle en étoile (`fact_sales`, `dim_customers`, `dim_products`).



## 🧹 Principaux traitements (Silver)

- Suppression des doublons (un seul enregistrement par client)
- Normalisation des libellés (genre, statut marital, pays, gamme de produit)
- Correction des dates et des montants incohérents
- Gestion des valeurs manquantes (`n/a`, `0`, `NULL`)



## ▶️ Exécution

​```sql
EXEC bronze.load_bronze;
EXEC silver.load_silver;
​```

## 🛠️ Outils

SQL Server · SSMS · Git · draw.io

## 👤 Auteur

**[Ton nom]**, [LinkedIn](https://www.linkedin.com/in/oumaima-el-haouari-57a800250/?isSelfProfile=true)
