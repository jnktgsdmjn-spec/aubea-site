# aubea.app — site vitrine

Site statique (HTML/CSS, sans framework, sans JavaScript, polices auto-hébergées).
Hébergé sur GitHub Pages, domaine géré chez Gandi.

## Pages
- `index.html` — accueil
- `mentions-legales.html`
- `cgu.html` et `confidentialite.html` — générées depuis `src/content/aubea/legalTexts.ts` de l'app (version 1.1 du 10 septembre 2026). À régénérer à chaque nouvelle version des textes.

## Mettre en ligne (une seule fois)
1. Créer le dépôt `aubea-site` sur GitHub (public), y pousser ce dossier.
2. Sur GitHub : Settings → Pages → Source « Deploy from a branch », branche `main`, dossier `/ (root)`.
3. Même page, « Custom domain » : `aubea.app` → Save. Le fichier `CNAME` est déjà dans le dépôt.
4. Chez Gandi → Nom de domaine → aubea.app → Enregistrements DNS :
   - supprimer les enregistrements A / CNAME existants sur `@` et `www` (ceux de Lovable) ;
   - ajouter 4 enregistrements A sur `@` : 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153 ;
   - ajouter un CNAME `www` → `jnktgsdmjn-spec.github.io.` (remplacer par votre identifiant GitHub si différent).
5. Attendre la propagation (quelques minutes à quelques heures), puis sur GitHub → Pages, cocher « Enforce HTTPS » dès qu'il devient disponible.

## Mettre à jour
Modifier les fichiers, commit, push : GitHub Pages redéploie en une à deux minutes.
