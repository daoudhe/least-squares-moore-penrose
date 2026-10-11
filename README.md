# Moindres carrés et pseudo-inverse de Moore-Penrose

En cours, les moindres carrés se résument souvent à une formule : x̂ = (AᵀA)⁻¹Aᵀb. J'ai voulu comprendre d'où elle vient, ce qu'elle signifie géométriquement, et pourquoi on évite de la calculer telle quelle en pratique.

Le notebook contient :

- un rappel de cours : problème des moindres carrés, projection orthogonale sur Im(A), équations normales, pseudo-inverse ;
- trois façons de résoudre : équations normales, QR et SVD. Elles donnent le même résultat en théorie, mais pas la même stabilité numérique, car le conditionnement de AᵀA est le carré de celui de A ;
- cinq exercices corrigés :
  1. une régression linéaire à la main ;
  2. la comparaison des trois méthodes sur un problème 100×10 bruité ;
  3. la projection orthogonale visualisée en 2D ;
  4. le conditionnement, et comment une petite perturbation de b est amplifiée ;
  5. la régression polynomiale (degrés 1 à 15) sur des données sinusoïdales bruitées, pour voir apparaître le sur-apprentissage.

Le rapport (`rapport.pdf`, source `rapport.tex`) reprend la démarche complète : la dérivation de la fonction coût, les propriétés de Moore-Penrose, un exemple numérique calculé entièrement à la main, le lien avec la SVD et la régression polynomiale. Les figures de `assets/` (interpolation de Lagrange, phénomène de Runge) viennent de ce rapport.

## Lancer

```bash
pip install -r requirements.txt
jupyter notebook moindres_carres.ipynb
```

Daoud Hechaïchi, élève-ingénieur ETI à CPE Lyon · [portfolio](https://daoud-hechaichi-cv.vercel.app)
