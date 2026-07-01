# Update Java Dependencies

**Action GitHub** pour mettre à jour le pom.xml (selon la version release ou snapshot), copier les JARs et actualiser le `NEWS.md`.

---
### **Utilisation**

```yaml
- uses: TanguyBarthelemy/actions/update-java-dependencies@v1
  with:
    update_type: "release"  # ou "snapshot"
    branch: "develop"       # défaut: develop
```

---
### **Fonctionnalités**

- Met à jour les dépendances Maven
- Copie les JARs (`mvn -Pcopy-jars`)
- Met à jour `NEWS.md` pour les releases
- Commit et push automatiques

---
### **Entrées**

| Entrée         | Description                     | Défaut     |
|----------------|---------------------------------|------------|
| `update_type`  | `release` ou `snapshot`         | `release`  |
| `branch`       | Branche cible                   | `develop`  |


---
### **Prérequis**

- Projet Maven avec `pom.xml`
- Plugin `heylogs-maven-plugin` pour `NEWS.md`
- Permissions `contents: write`
