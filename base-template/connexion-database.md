---
description: Tuto pour connecter votre sql
---

# 💾 Connexion database

Pour vous connecter à votre DB en localhost tout est déjà préparer vous avez juste a modifier par le nom de votre base :

Pour vous connecter à votre DB à votre serveur voici la ligne que vous devez remplacer.

```
set mysql_connection_string "mysql://USERID:MOTDEPASSE@IP/DATABASENAME?charset=utf8mb4"
```

USERID = Nom d'utilisateur SQL\
MOTDEPASSE = Mot de passe de la database\
IP = IP+Port de la database\
DATABASENAME = Nom de la database
