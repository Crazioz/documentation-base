---
description: Tuto pour connecter votre sql
---

# 💾 Connexion database

Pour vous connecter à votre DB en localhost tout est déjà préparer vous avez juste a modifier par le nom de votre base :

<pre class="language-properties"><code class="lang-properties">"<a data-footnote-ref href="#user-content-fn-1">basecrazioz"</a>
</code></pre>

Vous le retrouverez à cet endroit à la ligne 12 : [https://github.com/Crazioz/BaseCraziozV1/blob/main/server.cfg](https://github.com/Crazioz/BaseCraziozV1/blob/main/server.cfg)



Pour vous connecter à votre DB à votre serveur voici la ligne que vous devez remplacer.

`set mysql_connection_string "server=127.0.0.1;database=essentialmode;userid=root;password=YourPassword"`

Server = (vous le retrouvez généralement sur votre hébergeur) \
database = Nom de la base sur votre phpmyadmin\
userid = nom d'utilisateur (vous le retrouvez généralement sur votre hébergeur)&#x20;

Vous le retrouverez à cet endroit à la ligne 12 : [https://github.com/Crazioz/BaseCraziozV1/blob/main/server.cfg](https://github.com/Crazioz/BaseCraziozV1/blob/main/server.cfg)

[^1]: de base sur la ligne de connexion
