---
title: "SAE 502 - POC Kubernetes"
date: 2025-01-22 # Ensure this date is not in the future
tags: [Kubernetes, Projet, SAE]
categories: [PortfolioEtu]
layout: post
---

## Introduction

La SAE 502 est axée sur la conception et la mise en œuvre d’un cluster Kubernetes, utilisant une infrastructure de serveurs Debian 12. Ce projet a permis d’explorer les bases de l’orchestration de conteneurs tout en mettant en place une architecture réseau robuste et évolutive.

![Illustration Kube](/assets/img/portfolio/502/kube-logo.svg){: style="height: 300px;"}

## Objectifs

- Comprendre les principes de base de Kubernetes et son rôle dans l’orchestration de conteneurs.
- Configurer une infrastructure de serveurs pour supporter un cluster Kubernetes.
- Implémenter des fonctionnalités avancées comme la persistance des données et la scalabilité des services.
- Tester et valider les déploiements d’applications dans un environnement clusterisé.

## Contenu détaillé

### Configuration initiale des serveurs

Pour assurer une base solide, quatre serveurs ont été configurés avec Debian 12 :

- **srv01-k8s** : 10.108.10.1
- **srv02-k8s** : 10.108.10.2
- **srv03-k8s** : 10.108.10.3
- **srv04-k8s** : 10.108.10.4

Ces serveurs ont été préparés pour accueillir Kubernetes en configurant les dépendances nécessaires, comme `docker`, `kubectl`, et `kubeadm`.

### Déploiement du cluster Kubernetes

- **Initialisation du cluster** :
  - Utilisation de `kubeadm` pour initialiser le maître du cluster.
  - Ajout des nœuds au cluster à l’aide des jetons d’intégration générés.

- **Mise en place des services essentiels** :
  - Installation d’un plan de contrôle haute disponibilité.
  - Configuration du réseau avec pour assurer la communication entre pods.

![Illustration Kube](/assets/img/portfolio/502/ClusterK8S.png){: style="height: 300px;"}

### Validation et tests

- **Scalabilité** :
  - Déploiement de plusieurs réplicas pour tester l’équilibrage de charge.
  - Simulation de charges pour valider la capacité de montée en charge du cluster.

- **Persistance des données** :
  - Création de volumes persistants (PersistentVolume et PersistentVolumeClaim).
  - Test des applications nécessitant des bases de données avec persistance de données.

- **Déploiements automatisés** :
  - Configuration des fichiers `deployment.yaml` pour des mises à jour continues.
  - Utilisation de l’orchestrateur pour gérer les pannes et redémarrer automatiquement les pods défaillants.

## Résultats et apprentissages

- **Compétences techniques** : Maîtrise des outils Kubernetes, gestion des clusters et compréhension des plugins réseau.
- **Expérience pratique** : Déploiement et gestion d’applications critiques dans un environnement clusterisé.
- **Approche stratégique** : Mise en œuvre de solutions scalables et résilientes, tout en garantissant la persistance des données.

## Conclusion

La SAE 502 a permis une immersion complète dans l’univers de l’orchestration de conteneurs, offrant une expérience pratique précieuse pour comprendre les défis liés à la gestion des clusters Kubernetes. Les connaissances acquises renforcent les compétences en ingénierie DevOps et ouvrent la voie à des projets complexes nécessitant une infrastructure moderne et évolutive.

