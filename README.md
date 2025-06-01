# 🩺 PluginRevive pour Nova-Life

*Initié à partir du plugin de Victor2603 (maintenant obsolète)*

Le plugin **/revive** permet aux joueurs inconscients de se soigner eux-mêmes automatiquement si aucun médecin n’est disponible et si aucune autre personne n’est proche. Cette fonctionnalité est accessible via la commande `/revive`.

---

## ✨ Fonctionnalités principales

* ⚕️ **Auto-revive** : le joueur inconscient peut se soigner seul en dépensant 1000 €.
* 👨‍⚕️ **Détection des médecins en service** : si un ou plusieurs médecins sont disponibles, l’auto-revive est bloqué et une alerte est envoyée aux médecins.
* 👥 **Détection des joueurs proches** : si un autre joueur est proche, le revive automatique est interdit pour encourager l’entraide.
* 💸 **Coût fixe** de 1000 € pour l’auto-revive.
* ⏳ **Délai d’attente de 15 secondes** pendant lequel le joueur voit un message indiquant l’utilisation d’une trousse de secours.

---

## 🚀 Installation

1. Copier le fichier `PluginRevive.dll` (ou le code source) dans le dossier plugins de votre serveur Nova-Life.
2. S’assurer que le plugin est bien chargé au démarrage du serveur.
3. Configurer le webhook Discord si besoin en modifiant la constante `WebhookUrl` dans le code.

---

## 🎮 Utilisation

* Le joueur inconscient tape la commande `/revive` dans le chat.
* Si aucune condition bloquante n’est détectée (médecins en service, joueur proche, manque d’argent), l’auto-revive démarre :

  * Le joueur perd 1000 €.
  * Un message central s’affiche pendant 15 secondes.
  * Après 15 secondes, le joueur reprend conscience avec 30 points de vie, 10 de faim et 10 de soif.
* Si un médecin est en service, le joueur reçoit une notification et les médecins reçoivent une alerte avec la position.
* Si un autre joueur est proche, le joueur est invité à demander de l’aide.
* Si le joueur manque d’argent, il est prévenu.

---

## 📋 Commande

```plaintext
/revive
```

Description : Auto-revive si inconscient et seul.

---

## 📦 Dépendances

* Plugin compatible avec Nova-Life et ses APIs (`Life.Network`, `Life.BizSystem`, etc.).

---

## 📄 Licence

Vous n'avez pas le droit de copier le code de ce Plugin pour vous l'approprier et le vendre.
