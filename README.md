# CYTech 2024 - Support du cours § Cours d'industrialisation d'IA en Finance

## Introduction 

Ce cours fait suite au cours "Data Science pour la Finance", ayant pour but d'introduire un certain nombre de concept de Machine Leaning, Data Science et modélisations statistiques appliqués au domaine de la banque et de l'assurance. 

A la fin de ce cours, vous avez été capables de constuire un modèle de Machine Learning sur des données réelles et d'en mesurer les performances.

L'aventure liée à ce modèle n'est pas encore finie ! Maintenant que ce modèle a été développé sur votre ordinateur, il est temps de le rendre disponible à la terre entière :)

## Objectif de ce cours

L'objectif de ce cours est donc de rendre disponible le modèle en le mettant en production. Ce cours proposera donc une introduction à la construction et le déploiement d'une telle solution, ainsi que d'un grand nombre d'enjeux liés à ce sujet.

Ce cours abordera donc la création d'un système de mise à disposition d'un modèle de Machine Learning par la création d'une application associée (API - Application Programing Interface). 
Cette application sera ensuite déployée en production sur des environnements adaptés encapsulé dans une image Docker elle même déployée et configurée en production par des fichiers de Configuration kubernetes. 

Ces travaux sont l'occasion de (re)découvrir tout un ensemble de bonnes pratiques MLOps, avec des aspects de clean code, sécurité et résillience. Ces bonnes pratiques sont essentielles à la bonne réalisation d'un projet de Data Science. 

## Plan détaillé du cours

1. Introduction au cours
    - Présentation du cours
    - Présentation des intervenants du cours 
    - Présentation du projet 
    - Notation 


2. Norme de codes, clean code & ingéniérie logicielle
    - Norme de code Python : PEP8
    - Notebook VS fichier Python : vers le scaling d'une application
    - Programation orientée objet 
    - Programation asynchrone
    - Programation SOLID

3. Git & GitHub : introduction au code en collaboration
    - Git 
    - Motivation à l'utilisation 
    - GitHub
    - Branches & Nommenclatures
    - Quelques commandes de base
    - Quelques fichiers à connaitre

4. API : Création d'une application en Python
    - Définition & motivation
    - Framework de développement Python 
    - Open API (ou Swagger)
    - PyPI : packaging de code

5. Infrastucture de production
    - Développement 
    - Recette 
    - Pre-production
    - Production
    - Framework de BDD
    - Nomenclature de BDD
    - Architecture on-premise
    - Cloud 

6. Docker
    - Qu'est ce que Docker ? 
    - Motivation 
    - Quelques commandes dans Docker
    - Repertoire d'images
    - Que faire avec mon image ?

7. Kubernetes
    - Qu'est ce que Kubernetes ? 
    - Motivation 
    - Scalabilité horizontale VS verticale
    - Redondance, maintenance et persistence

8. Continuous Integration (CI)
    - Qu'est ce que la CI ? 
    - Testing Automatique (Unit tests, Pen Tests, Tests de charge...)
    - Evaluation de qualité de code
    - Build automatique d'image
    - Construction de documentations automatique
    - Outils d'exécution de CI
    - [OPTIONNEL] Promotion d'images

9. Continuous Delivry (CD)
    - Qu'est ce que la CD ? 
    - Combinaison à Kubernetes
    - Infrastructure as Code (IaC) : Yaml VS Terraform
    - Quelques outils de CD : ArgoCD, Red Hat Openshift...

10. Quelques autres pratiques MLOps
    - Suivi d'applications en production (logging, kafka, data drift)
    - Pipeline d'entrainement automatique 
    - Feedback Loop
    - Pipeline d'inférence
