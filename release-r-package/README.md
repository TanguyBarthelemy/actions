# Release R Package

**Action GitHub** pour automatiser la release d'un package R : merge des branches, mise à jour de `DESCRIPTION`, `NEWS.md`, tag GitHub et création d'une release draft.

---
### **Utilisation**

```yaml
- uses: votre-org/repo/actions/release-r-package@v1
  with:
    tag: "v1.0.0"               # requis
    main-branch: "main"         # défaut: branche par défaut
    dev-branch: "develop"       # optionnel
    change-remotes: "false"     # défaut: false
    github_token: ${{ secrets.GITHUB_TOKEN }}
```

---
### **Entrées**

| Entrée           | Description                                      | Défaut     |
|------------------|--------------------------------------------------|------------|
| `tag`            | Tag de la release (ex: `v1.0.0`)                | -          |
| `main-branch`    | Branche principale (ex: `main`)                 | -          |
| `dev-branch`     | Branche de développement (ex: `develop`)        | -          |
| `change-remotes` | Mettre à jour les `Remotes` dans `DESCRIPTION`  | `false`    |
| `github_token`   | Token GitHub (défaut: `${{ github.token }}`)   | -          |

---
### **Fonctionnalités**

✅ Merge `dev-branch` → `main-branch` → `dev-branch`
✅ Met à jour `DESCRIPTION` et `NEWS.md`
✅ Crée un tag Git et une **release draft**
✅ Incrémente la version de développement
✅ Gère les `Remotes` si `change-remotes: true`

---
### **Prérequis**

- Projet R avec `DESCRIPTION` et `NEWS.md`
- Package `releaser` installé (`pak::pak("TanguyBarthelemy/releaser")`)
- Permissions `contents: write`
- Outils système: `libcurl4-openssl-dev`, `libuv1-dev`
