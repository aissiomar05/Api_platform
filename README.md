# Projet API Platform - Clinique Vétérinaire

## Membres du groupe
- [Nom 1] (Ton Nom)
- [Nom 2] (Ton Coéquipier)

## Description du projet
Ce projet consiste en la création d'une API pour gérer une clinique vétérinaire. L'application utilise Symfony et API Platform pour gérer les différentes entités et fonctionnalités.

### Entités et Relations
- **User (Directeur, Vétérinaire, Assistant)**
  - Chaque utilisateur a un rôle (`ROLE_DIRECTOR`, `ROLE_VETERINARIAN`, `ROLE_ASSISTANT`).
  - Relations : 
    - Un utilisateur peut avoir plusieurs animaux (relation OneToMany avec `Animal`).

- **Animal**
  - Un animal a un nom, une espèce, une date de naissance et une photo.
  - Relations :
    - Un animal a un propriétaire, qui est un utilisateur (`ManyToOne` avec `User`).

- **Rendez-vous**
  - Un rendez-vous a une date de création, une date de rendez-vous, un motif, un statut (programmé, en cours, terminé).
  - Relations :
    - Un rendez-vous appartient à un animal, un assistant vétérinaire, et un vétérinaire (`ManyToOne` avec `Animal` et `User`).
    - Un rendez-vous peut avoir plusieurs traitements prescrits (`ManyToMany` avec `Traitement`).

- **Traitement**
  - Chaque traitement a un nom, une description, un prix, et une durée.
  
- **Media**
  - Chaque media contient une photo ou un fichier lié à l'animal.

## Prérequis
- PHP 8.1 ou plus
- Composer
- Symfony
- MySQL (ou autre base de données compatible)
- API Platform

## Installation

1. Clonez le dépôt :
   ```bash
   git clone https://github.com/aissiomar05/Api_platform.git
