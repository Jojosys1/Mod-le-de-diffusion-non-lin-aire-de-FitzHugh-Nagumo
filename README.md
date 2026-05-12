# Mod-le-de-diffusion-non-lin-aire-de-FitzHugh-Nagumo

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![LaTeX](https://img.shields.io/badge/LaTeX-Beamer-green.svg)](https://www.latex-project.org/)

> Simulation numérique du modèle réaction-diffusion de FitzHugh-Nagumo en régime instationnaire. Étude des ondes de propagation dans les milieux excitables.

## 📖 À propos

Ce projet présente l'implémentation numérique et l'analyse du **modèle de FitzHugh-Nagumo** pour la propagation d'ondes instationnaires dans un milieu excitable. Le modèle couple une variable rapide (potentiel membranaire) et une variable lente (courant de récupération) avec des termes de diffusion linéaires et non linéaires.

### Contexte académique
Ce travail a été réalisé dans le cadre d'un projet de modélisation mathématique et simulation numérique. Il inclut :
- L'implémentation complète du solveur (notebook Jupyter)
- Une présentation au format LaTeX Beamer
- Un document principal détaillant la théorie et les résultats

## 📁 Structure du repository

```
├── simulation_final.ipynb       # Notebook principal avec le code de simulation
├── Problème_instationnaire_Nagumo_s_model.pdf  # Document principal (résultats)
├── Groupe_3_beamer.pdf          # Présentation orale (Beamer)
├── beamer.tex                   # Source LaTeX de la présentation
├── main.tex                     # Source LaTeX du document principal
├── page_de_garde.tex            # Page de garde LaTeX
└── README.md                    # Ce fichier
```

## 🧮 Modèle mathématique

### Équation de Nagumo (instationnaire)

Le modèle s'écrit sous la forme d'un système réaction-diffusion :

```math
\frac{\partial u}{\partial t} = D \frac{\partial^2 u}{\partial x^2} + f(u)
```

avec la réaction non linéaire cubique :

```math
f(u) = u(1 - u)(u - a) \quad \text{où} \quad 0 < a < 1
```

### Version complète de FitzHugh-Nagumo

```math
\begin{cases}
\dfrac{\partial u}{\partial t} = \dfrac{\partial^2 u}{\partial x^2} + u - \dfrac{u^3}{3} - v \\ \\
\dfrac{\partial v}{\partial t} = \varepsilon (u + \beta - \gamma v)
\end{cases}
```

## 🚀 Utilisation

### Lancer la simulation

```bash
# Lancer le notebook Jupyter
jupyter notebook simulation_final.ipynb
```

### Paramètres simulés

| Paramètre | Description | Valeur |
|-----------|-------------|--------|
| `a` | Seuil d'excitabilité | 0.1 - 0.9 |
| `D` | Coefficient de diffusion | 0.1 - 10 |
| `ε` | Séparation d'échelles | ≪ 1 |

## 🎯 Résultats principaux

Le notebook `simulation_final.ipynb` permet de :

- ✅ Résoudre numériquement l'équation de Nagumo instationnaire
- ✅ Visualiser la propagation des fronts d'onde
- ✅ Analyser l'influence des paramètres sur la vitesse de propagation
- ✅ Observer la formation d'ondes progressives

## 📊 Exemple de simulation

```python
# Extrait du notebook
import numpy as np
import matplotlib.pyplot as plt

# Paramètres
nx = 1000        # points spatiaux
nt = 10000       # pas de temps
dx = 0.1         # pas spatial
dt = 0.001       # pas temporel
a = 0.2          # paramètre de seuil

# ... résolution du schéma numérique
```

## 📚 Documentation LaTeX

La présentation `beamer.tex` et le document `main.tex` contiennent :
- La formulation mathématique complète
- L'analyse de stabilité linéaire
- La dérivation des vitesses d'onde
- Les résultats numériques détaillés

Pour compiler les sources LaTeX :

```bash
pdflatex main.tex
pdflatex beamer.tex
```

## 📈 Résultats visualisés

| Type de front | Vitesse de propagation | Stabilité |
|---------------|------------------------|-----------|
| Front monotone | $c \propto \sqrt{D}$ | Stable |
| Front pulsé | $c = c_0 + \delta c$ | Métastable |

## 🔬 Applications

Le modèle est utilisé pour comprendre :
- La propagation des influx nerveux
- Les ondes de réaction chimique (BZ)
- La formation de motifs en biologie du développement

## 🤝 Contribution

Les contributions sont les bienvenues !

1. Fork le projet
2. Créez votre branche (`git checkout -b feature/amelioration`)
3. Commitez vos changements
4. Poussez vers la branche
5. Ouvrez une Pull Request

## 📝 Licence

Distribué sous licence MIT. Voir `LICENSE` pour plus d'informations.

## 📧 Contact

**Groupe 3** - Projet de modélisation mathématique

Lien du projet : [https://github.com/votre-username/fitzhugh-nagumo-model](https://github.com/votre-username/fitzhugh-nagumo-model)

## 🙏 Remerciements

- Encadrants du projet
- Référence : Nagumo et al. (1962) - "An Active Pulse Transmission Line Simulating Nerve Axon"

---

⭐️ **N'hésitez pas à mettre une étoile sur ce repository !** ⭐️
