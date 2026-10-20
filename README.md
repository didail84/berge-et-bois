# Berge & Bois

Logiciel gratuit et open source pour **concevoir et chiffrer les ouvrages bois et de berge** : terrasse, ponton, passerelle, cheminement, pergola, escalier, tunage de berge, génie végétal, terrassement, arrosage, phyto-épuration…

- **Calcul** des pièces (lames, lambourdes, poutres, poteaux), des fixations (vis, tire-fonds, goujons, tiges filetées) et des fondations, avec verdict clair.
- **Plans** simplifiés (vue de dessus, coupes, 3D), export PDF à l'échelle et DXF (AutoCAD).
- **Débit, plan de coupe, devis** et export Excel.
- **Chantier** : fiche, planning, suivi sur tablette avec photos, stock.
- **Tes projets restent sur ton ordinateur** : pas de compte, pas d'abonnement.

> ⚠️ Pré-dimensionnements **indicatifs** : ils ne remplacent pas une note de calcul de bureau d'études.

## Installer

Va dans **[Releases](https://github.com/didail84/berge-et-bois/releases/latest)** et télécharge, dans *Assets*, le fichier qui correspond à ton ordinateur :

| Ordinateur | Fichier |
|---|---|
| Windows 10 ou 11 | `BergeEtBois-x.y.z-win-x64.exe` |
| Mac Intel (macOS 12 Monterey ou plus récent) | `BergeEtBois-x.y.z-mac-x64.dmg` |
| Mac Apple Silicon (M1, M2, M3, M4…) | `BergeEtBois-x.y.z-mac-arm64.dmg` |

N'utilise pas « Source code (zip) » : il ne contient que le code.

### Windows
1. Double-clique sur le `.exe`.
2. Si Windows affiche « Windows a protégé votre ordinateur » : **Informations complémentaires** → **Exécuter quand même** (l'appli n'est pas signée par un certificat payant).
3. Suis l'installation : un raccourci « Berge & Bois » est créé sur le Bureau et dans le menu Démarrer.

### Mac
1. Ouvre le `.dmg` et fais glisser **Berge & Bois** dans **Applications**.
2. La première fois : **clic droit (ou Ctrl-clic) → Ouvrir** → **Ouvrir**.
3. Si macOS dit que l'app est « endommagée » : dans le Terminal, tape
   `xattr -cr "/Applications/Berge & Bois.app"`, puis relance.

### Mises à jour
Au démarrage, l'appli regarde s'il existe une nouvelle version ici et propose de la télécharger. Tes projets sont conservés.

### Reprendre tes projets
Dans l'ancienne version (fichier HTML ou page Claude) : **Exporter → Projet (.json)** pour chaque projet. Dans l'appli : **Exporter → Importer un projet (.json)**.

## Pour les développeurs

L'appli est une page web (`app/index.html`) emballée avec [Electron](https://www.electronjs.org). Les bibliothèques sont dans `app/lib/` pour fonctionner hors ligne.

```bash
npm install          # une seule fois
npm start            # lancer l'appli
npm run dist:win     # installateur Windows
npm run dist:mac     # installateur Mac (sur un Mac)
```

Les installateurs officiels sont fabriqués par GitHub Actions (`.github/workflows/release.yml`) quand une version est publiée (étiquette `v1.0.1`, `V1.0.1`…).

Electron est figé en version 43 : la dernière qui fonctionne encore sur macOS 12.

## Licence

Code sous licence MIT — voir [LICENSE](LICENSE). Bibliothèques et services tiers : voir [NOTICE.md](NOTICE.md).
