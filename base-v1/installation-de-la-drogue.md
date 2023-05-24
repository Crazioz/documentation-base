---
description: 'Script : esx_drugsbuilder'
---

# 🌱 Installation de la drogue

Avant de commencer vous devez récupérer votre identifiant qui se trouve dans la user \
(après votre première connexion) :&#x20;

<figure><img src="../.gitbook/assets/Screenshot_1 (1).png" alt="" width="563"><figcaption></figcaption></figure>

Par la suite ajouter le dans le fichier config.lua : \


<figure><img src="../.gitbook/assets/Screenshot_2 (2).png" alt="" width="563"><figcaption></figcaption></figure>

Pour commencer la création, vous devez entrer la commande :  `/drugsbuilder`\
**N'oubliez pas de bien ajouter chaque item dans votre sql avant cela !**

{% hint style="info" %}
Les items sont déjà pré installer avec les icons : \
\[Meth/Meth\_Pochon] / \[weed/weed\_pochon] / \[coke/coke\_pochon]
{% endhint %}

Exemple de ce que vous devez ajouter dans le SQL pour ajouter vos items \[**ils existent déjà !]**

```sql
INSERT INTO `items` (`name`, `label`, `weight`, `rare`, `can_remove`) VALUES
	('meth', 'Meth', 1, 0, 1),
	('weed', 'Weed', 1, 0, 1),
	('coke', 'Coke', 1, 0, 1)
;
```
