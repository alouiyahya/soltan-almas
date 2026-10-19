# Soltan & Almas · Parfumerie Tétouan

Site e-commerce statique (HTML/CSS/JS, sans build) pour la parfumerie **Soltan & Almas** à Tétouan.
Testeurs de parfums 100 % originaux, livraison Tétouan et Tanger, paiement à la livraison.
Les commandes partent directement sur WhatsApp (07 81 91 35 01).

## Structure

```
index.html     page complète (styles et scripts inclus)
images/        photos des flacons + logo
vercel.json    config Vercel (cache des images)
```

## Modifier les produits

Dans `index.html`, cherchez `const P=[`. Chaque produit a :
- `img` : nom du fichier dans `images/` (sans `.webp`)
- `h` marque, `n` nom, `p` prix en dh, `o` ancien prix (optionnel, active la promo)
- `g` genre (`رجالي` / `للجنسين` / `نسائي`), `f` famille, `top` / `heart` / `base` notes
- `isNew:1` pour le badge « جديد »

Pour ajouter un parfum : déposez sa photo (fond transparent, `.webp` ou `.png`) dans `images/`,
ajoutez-la dans `const IMG=` et ajoutez une ligne dans `const P=[`.

## Lancer en local

Ouvrez `index.html` dans le navigateur, ou :

```
npx serve .
```

## Déploiement

Hébergé sur Vercel : chaque `git push` sur `main` met le site à jour automatiquement.
