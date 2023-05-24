---
description: Ajouter un item dans le PhpMyAdmin (SQL/BDD)
---

# 🍕 Ajouter un item Utilisable

Documentation de l'inventaire pour la création d'item : [https://overextended.github.io/docs/ox\_inventory/Guides/creatingItems](https://overextended.github.io/docs/ox\_inventory/Guides/creatingItems)

{% hint style="danger" %}
N'oubliez pas d'ajouter dans le script : esx\_basicneeds l'item que vous souhaitez attribuer de la Faim ou de la soif
{% endhint %}

Voici un exemple de ce que vous devez ajouter dans le fichier server.lua du script :&#x20;

{% code lineNumbers="true" %}
```lua
ESX.RegisterUsableItem('bread', function(source)

	local _source = source
    local xPlayer = ESX.GetPlayerFromId(_source)

	xPlayer.removeInventoryItem('bread', 1)

	TriggerClientEvent('esx_status:add', source, 'hunger', 250000)
	TriggerClientEvent('esx_basicneeds:onEat', source)
	TriggerClientEvent('esx:showNotification', source, _U('used_bread'))

end)
```
{% endcode %}

La ligne 1 et 6 vous devez remplacer 'bread' par l'item que vous souhaitez que vous aviez ajouté auparavant dans le SQL\
\
Dans la ligne 8 ou il y a marquer 'hunger' vous pouvez la remplacer par 'thirst' ou 'drunk'\
\
Vous pouvez également ajoutez plusieurs d'affiler  :&#x20;

<pre class="language-lua"><code class="lang-lua">TriggerClientEvent('esx_status:add', source, 'hunger', 250000)
<strong>TriggerClientEvent('esx_status:add', source, 'thirst', 250000)
</strong>TriggerClientEvent('esx_status:add', source, 'drunk', 250000)
</code></pre>

Et pour finir à la fin de la ligne, vous remarquerez les chiffres '75000' ce qui signifie ce que vous donnez à la personne qui l'utilise\
\
**Exemple :** \
\
1000000 = 100% de votre barre de faim ou soif\
500000 = 50%\
250000 =25%
