# 🛡️ Microsoft Entra ID - Audit des Utilisateurs Inactifs (90 jours)

Ce dépôt contient un script PowerShell permettant d'identifier les utilisateurs qui ne se sont pas connectés à leur compte Microsoft Entra ID (anciennement Azure AD) depuis plus de **90 jours**.

## 📋 Description

Le script utilise le module **Microsoft Graph** pour interroger la propriété `signInActivity`. Cette méthode est la plus fiable car elle prend en compte :
* Les connexions interactives (saisie de mot de passe).
* Les connexions non-interactives (tokens de rafraîchissement).
* Les utilisateurs n'ayant jamais effectué de connexion.

## 🚀 Utilisation

### Prérequis

1.  **Module PowerShell** : Vous devez avoir installé le module Microsoft Graph.
    ```powershell
    Install-Module Microsoft.Graph -Scope CurrentUser
    ```
2.  **Permissions** : Un compte avec au moins le rôle **Lecteur de rapports** ou **Administrateur d'utilisateurs**.
3.  **Licence** : Une licence **Entra ID P1 ou P2** est requise dans le tenant pour accéder aux données de `signInActivity`.
