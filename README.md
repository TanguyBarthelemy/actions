# Actions

**Dépôt d'actions composites** pour automatiser des tâches courantes dans nos projets.

---
## **Actions Disponibles**

| Action                          | Description                                      |
|---------------------------------|--------------------------------------------------|
| [`update-java-dependencies`](./update-java-dependencies/README.md) | Met à jour les dépendances Java et les JARs.     |
| [`release-r-package`](./release-r-package)         | Prépare une release pour un package R.           |

---
## **Utilisation**

```yaml
steps:
  - name: Nom de l'étape
    uses: votre-org/github-actions/actions/nom-de-l-action@v1
    with:
      param1: valeur1
      param2: valeur2
```

---
## **Contribution**

1. Ajoutez votre action dans `actions/`.
2. Documentez-la avec un `README.md`.
3. Testez-la localement ou via le workflow `.github/workflows/test-actions.yml`.

---
## **Versionnement**

Les actions sont versionnées avec des **tags Git** (ex: `v1.0`). Utilisez toujours une version spécifique dans vos workflows.
