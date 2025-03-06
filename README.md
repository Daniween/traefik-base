# 🚀 Configuration de Base pour Traefik et Portainer

Ce repository contient des fichiers de configuration Docker Compose pour **Traefik** et **Portainer**, facilitant la gestion des services avec un reverse proxy et la prise en charge du certificat SSL.

---

## 📂 Contenu du Repository

### Fichiers disponibles :

- **`traefik-docker-compose.yml`** : Configuration principale de Traefik
- **`traefik-docker-compose-light.yml`** : Version allégée de la configuration Traefik sans la gestion du SSL
- **`portainer-docker-compose.yml`** : Configuration pour déployer Portainer avec Docker Compose
- **`README.md`** : Guide d'utilisation et instructions de configuration

---

## ⚙️ Configuration à Modifier

Avant de déployer, certaines valeurs doivent être mises à jour dans les fichiers de configuration :

### 🔹 `traefik-docker-compose.yml`

- **Ligne 19** : Remplacez votre adresse mail pour la gestion des certificats SSL.
- **Ligne 33** : Remplacez le sous-domaine par votre propre domaine :
  ```yaml
  traefik.nomdedomaine.com
  ```
- **Ligne 48** : Remplacez le sous-domaine utilisé pour le service Whoami :
  ```yaml
  whoami.nomdedomaine.com
  ```

### 🔹 `portainer-docker-compose.yml`

- **Ligne 16** : Remplacez le sous-domaine utilisé pour Portainer :
  ```yaml
  portainer.nomdedomaine.com
  ```

---

## 🚀 Déploiement

Une fois les configurations modifiées, utilisez les commandes suivantes pour déployer :

### 🔹 Démarrer Traefik

```bash
docker-compose -f traefik-docker-compose.yml up -d
```

### 🔹 Démarrer Portainer

```bash
docker-compose -f portainer-docker-compose.yml up -d
```

### 🔹 Vérifier les logs

```bash
docker-compose logs -f
```

---

✨ **Bon déploiement !** 🚀
