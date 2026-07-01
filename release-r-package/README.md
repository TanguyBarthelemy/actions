# Release R Package

**Action GitHub** pour automatiser la release d'un package R : mise à jour du répertoire, management des branches et préparation d'une release draft.

---
### **Utilisation**

```yaml
- uses: TanguyBarthelemy/actions/release-r-package@v1
  with:
    tag: "v1.0.0"               # requis
    main-branch: "main"         # défaut: branche par défaut
    dev-branch: "develop"       # optionnel
    change-remotes: "false"     # défaut: false
    github_token: ${{ secrets.GITHUB_TOKEN }}
```

---
### **Fonctionnalités**

- Met à jour `DESCRIPTION` et `NEWS.md`
- Crée un tag Git et une **release draft**
- Incrémente la version de développement
- Gère les `Remotes` si `change-remotes: true`

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
### **Prérequis**

- Projet R avec `DESCRIPTION` et `NEWS.md`
- Permissions `contents: write`

---
### **Prérequis**

- R packages : {releaser} et {gh}
- Outils système: `libcurl4-openssl-dev`, `libuv1-dev`
