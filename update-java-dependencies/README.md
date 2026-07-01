# Update Java Dependencies

**Action GitHub** pour mettre à jour les dépendances Java (release/snapshot), copier les JARs et actualiser le `NEWS.md`.

---
### **Utilisation**

```yaml
- uses: votre-org/repo/actions/update-java-dependencies@v1
  with:
    update_type: "release"  # ou "snapshot"
    branch: "develop"       # défaut: develop
    java_version: "21"      # défaut: 21
```

---
### **Entrées**

| Entrée         | Description                     | Défaut     |
|----------------|---------------------------------|------------|
| `update_type`  | `release` ou `snapshot`         | `release`  |
| `branch`       | Branche cible                   | `develop`  |
| `java_version` | Version de Java                | `21`       |

---
### **Fonctionnalités**

✅ Met à jour les dépendances Maven
✅ Copie les JARs (`mvn -Pcopy-jars`)
✅ Met à jour `NEWS.md` pour les releases
✅ Commit et push automatiques

---
### **Prérequis**

- Projet Maven avec `pom.xml`
- Plugin `heylogs-maven-plugin` pour `NEWS.md`
- Permissions `contents: write`
