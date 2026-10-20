# bonita-test : processus Demande d'habilitation

Processus Bonita de demande d'habilitation, conçu avec Bonita Studio Community 2025.2.

## Le processus

1. Le demandeur remplit une demande : application, type d'accès, justification
2. Le validateur accepte ou refuse
3. Le processus se termine sur Demande acceptée ou Demande refusée

## Éléments du modèle

- Deux lanes : Employé (demandeur) et Validateur
- Variables : application, typeAcces, justification, approuve
- Un contrat et des opérations sur chaque tâche humaine
- Un formulaire généré par tâche (formRemplirDemande, formValiderDemande)
- Une passerelle exclusive qui lit la variable approuve

## Ouvrir le projet

1. Cloner le dépôt dans le workspace de Bonita Studio
2. Importer le projet existant dans Studio
3. Lancer le processus avec Run pour un test local

## Déployer sur un serveur

1. Construire le fichier .bar depuis Studio
2. L'installer dans l'application Administrator du serveur
3. Mapper les acteurs Employé et Validateur sur des utilisateurs
4. Activer le processus

Le serveur Docker de test est décrit dans le dépôt Test-Bonita-BPM.

## Versions

- v1.0-stable : flux de base, sans notification