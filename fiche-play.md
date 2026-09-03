# Fiche Google Play — PhotoCalc

Textes à copier-coller dans la console Play. La fiche française (langue par défaut du
projet) est ci-dessous ; la fiche anglaise est dans sa propre section plus loin. Les
limites de caractères indiquées sont celles imposées par Play ; le décompte réel de
chaque texte est donné à côté — à revérifier si le texte est modifié.

⚠️ **Application pas encore publiée** (`versionCode = 1` / `versionName = "0.1.0"` dans
[app/build.gradle.kts](../app/build.gradle.kts), `applicationId = "com.photocalc.app"`)
— cette fiche est une création, pas une mise à jour. Contenu à jour au 2 septembre 2026
d'après [SUIVI.md](../SUIVI.md) : 8 calculateurs implémentés (règle des 500, règle NPF,
Voie lactée, hyperfocale, profondeur de champ, champ de vision, équivalence focale,
séquence), profils appareil/objectif, 51 tests unitaires au vert.

---

## Nom de l'application

*(30 caractères max — 9 utilisés)*

```
PhotoCalc
```

## Description courte

*(80 caractères max — 77 utilisés)*

```
Hyperfocale, NPF, profondeur de champ : les calculs photo essentiels, offline
```

## Description complète

*(4000 caractères max — environ 1450 utilisés)*

```
PhotoCalc regroupe les calculs techniques utiles aux photographes en un seul endroit : renseignez quelques valeurs, obtenez le résultat immédiatement — sans connaissances mathématiques et sans connexion Internet.

■ MODULE ASTRO
Règle des 500, règle NPF et calcul dédié à la Voie lactée pour connaître le temps de pose maximum avant que les étoiles ne commencent à filer, avec vos objectifs enregistrés.

■ MODULE PHOTO
Hyperfocale, profondeur de champ, champ de vision et équivalence focale — les calculs indispensables pour le paysage, la macro et le choix d'un objectif.

■ SÉQUENCES
Calculez la durée totale d'une session d'intervallomètre ou d'un empilement à partir du nombre de photos, du temps de pose et de l'intervalle.

■ VOS APPAREILS ET OBJECTIFS
Enregistrez vos boîtiers et objectifs (capteur, résolution, ouverture réelle) : les calculs se pré-remplissent automatiquement avec les bonnes valeurs, sans ressaisie à chaque fois. Plusieurs appareils possibles, avec un favori.

■ PENSÉ POUR LE TERRAIN
Interface lisible, utilisable d'une seule main, unités au choix (mètres, centimètres, pieds, pouces).

■ 100 % HORS LIGNE
Aucune connexion nécessaire pour calculer. Aucun compte, aucune inscription, aucune donnée envoyée à un serveur : vos appareils et objectifs restent sur votre téléphone.

Une bannière publicitaire discrète finance l'application gratuite.
```

---

## Fiche anglaise (English store listing)

Play traite chaque langue comme une fiche séparée. Le chemin dans la console :
**Accroître le nombre d'utilisateurs → Traductions**, puis « ajouter vos propres
textes de traduction » — pas la traduction automatique de Google.

### App name

*(30 characters max — 9 used)*

```
PhotoCalc
```

### Short description

*(80 characters max — 67 used)*

```
Hyperfocal, NPF rule, depth of field: essential photo math, offline
```

### Full description

*(4000 characters max — approx. 1330 used)*

```
PhotoCalc brings together the technical calculations photographers need in one place: enter a few values, get the result instantly — no math background and no internet connection required.

■ ASTRO MODULE
500 rule, NPF rule and a dedicated Milky Way calculation to know the maximum exposure time before stars start trailing, using your saved lenses.

■ PHOTO MODULE
Hyperfocal distance, depth of field, field of view and focal length equivalence — the calculations you need for landscape, macro and choosing a lens.

■ SEQUENCES
Calculate the total duration of an intervalometer session or a focus stack from the number of shots, exposure time and interval.

■ YOUR CAMERAS AND LENSES
Save your camera bodies and lenses (sensor, resolution, actual aperture): calculations are pre-filled automatically with the right values, no retyping every time. Multiple cameras supported, with a favorite.

■ BUILT FOR THE FIELD
Readable interface, usable with one hand, choice of units (meters, centimeters, feet, inches).

■ 100% OFFLINE
No connection needed to calculate. No account, no sign-up, no data sent to a server: your cameras and lenses stay on your phone.

A discreet banner ad funds the free app.
```

---

## Classification et catégorie

| Champ | Valeur |
|---|---|
| Type | Application |
| Catégorie | Photographie |
| Tags | Photographie, Astrophotographie, Calculatrice, Outils |
| Public cible | Tout public |
| Contient des annonces | **Oui** (bannière AdMob) |
| Achats via l'application | Non |

## Questionnaire de classification du contenu (IARC)

Aucun contenu sensible : pas de violence, contenu sexuel, langage grossier, drogues,
jeux d'argent. Pas d'interaction entre utilisateurs (pas de compte, pas de
classement, pas de partage). Pas de partage de position ni de coordonnées
personnelles.

## Sécurité des données

À déclarer, sans quoi la fiche est rejetée :

| Donnée | Collectée | Partagée | Pourquoi |
|---|---|---|---|
| Identifiant publicitaire | Oui | Oui | Publicité (SDK AdMob) |

Aucune autre donnée n'est collectée : pas de compte, pas de position, pas de
contacts, pas de fichiers. Les profils d'appareils et d'objectifs enregistrés par
l'utilisateur restent stockés localement (DataStore) et ne sont jamais envoyés à un
serveur. Le SDK AdMob ajoute lui-même la permission
`com.google.android.gms.permission.AD_ID` au manifeste (voir
[AndroidManifest.xml](../app/src/main/AndroidManifest.xml)) : Play rejette une
application qui la déclare sans déclarer l'usage correspondant ci-dessus.

Données chiffrées en transit ? **Oui** (AdMob en HTTPS). Les calculs eux-mêmes ne
font aucun appel réseau — seule la bannière publicitaire en fait, et son
initialisation est différée (voir `OPTIMIZE_INITIALIZATION` /
`OPTIMIZE_AD_LOADING` dans le manifeste).

### Version anglaise — pour référence uniquement

⚠️ **Le formulaire Sécurité des données n'est pas traduisible dans la Play Console** :
c'est une déclaration unique par application, Google affiche automatiquement les
libellés dans la langue du visiteur.

| Data | Collected | Shared | Why |
|---|---|---|---|
| Advertising ID | Yes | Yes | Advertising (AdMob SDK) |

Data encrypted in transit? **Yes** (AdMob over HTTPS). Saved cameras/lenses stay on
device and are never uploaded.

---

## Identifiants AdMob

Déjà en place dans le code (pas un identifiant de test) :

- `AndroidManifest.xml` : `com.google.android.gms.ads.APPLICATION_ID` =
  `ca-app-pub-7930855717646694~1493351500` (App ID réel)
- [`AdIds.kt`](../app/src/main/java/com/photocalc/app/ads/AdIds.kt) : bannière
  « Accueil » = `ca-app-pub-7930855717646694/5205471001` (bloc réel)

La bannière **bascule automatiquement** entre bloc de test et bloc réel selon
`BuildConfig.DEBUG` : un build de debug continue de servir le bloc de test, un build
release (comme l'AAB envoyé à Play) sert le bloc réel — rien à changer à la main
avant l'envoi. Le consentement RGPD/TCF (Google UMP) est géré par
[`ConsentManager.kt`](../app/src/main/java/com/photocalc/app/ads/ConsentManager.kt),
avec un point d'entrée « Confidentialité » dans les options
([`SettingsScreen.kt`](../app/src/main/java/com/photocalc/app/ui/settings/SettingsScreen.kt)).

## Visuels

Produits le 2 septembre 2026 sur l'émulateur — détails et méthode dans
[visuels/NOTES.md](visuels/NOTES.md).

| Fichier | Format | Usage |
|---|---|---|
| `icone_512.png` | 512×512 PNG | Icône de la fiche Play (obligatoire), partagée entre les langues — rendue depuis les vecteurs sources de l'icône adaptative, pas une capture agrandie |
| `fr/banniere_1024x500.png` | 1024×500 PNG | Image mise en avant, fiche française |
| `en/banniere_1024x500.png` | 1024×500 PNG | Image mise en avant, fiche anglaise |
| `fr/capture-*.png` (4 fichiers) | 1080×2266 à 1080×2400 | Accueil, Voie lactée, Hyperfocale, Champ de vision — app en français |
| `en/capture-*.png` (4 fichiers) | 1080×2266 à 1080×2400 | Mêmes écrans, app basculée en anglais (`cmd locale set-app-locales`) — vraie interface traduite, pas une réutilisation des captures FR |

L'app est maintenant traduite en anglais (`values-fr/strings.xml` +
`values/strings.xml` en repli, ajoutés le 2 septembre 2026) : les captures `en/`
montrent l'interface anglaise réelle, avec le formatage des nombres qui suit (point
décimal au lieu de la virgule). Un sélecteur de langue est disponible **dans l'app**
(Réglages → Langue : Automatique / Français / English), et un second, redondant,
côté système sur Android 13+ (Réglages Android → Applications → PhotoCalc → Langue,
via `android:localeConfig`) — les deux restent synchronisés entre eux.

## Site — page d'accueil et politique de confidentialité

Deux dépôts GitHub distincts, confirmés par l'utilisateur le 2 septembre 2026 :

| Dépôt | Visibilité | Rôle |
|---|---|---|
| `github.com/olivier3dprint/PhotoCalc` | **Privé** | Code source de l'application (celui-ci) |
| `github.com/olivier3dprint/PhotoCalcSite` | **Public** | Site (page d'accueil + politique de confidentialité), via GitHub Pages |

Séparation nécessaire : GitHub Pages sur dépôt privé exige un plan payant, et la
politique de confidentialité doit être accessible publiquement sans authentification.

Sur le même principe que Calculatrice H/M : `index.html` et `confidentialite.html`
vivent **à la racine** de `PhotoCalcSite` (pas dans un sous-dossier — GitHub Pages en
mode `main` / `/ (root)` ne sert `index.html` qu'à la racine).

| Fichier | Rôle | URL une fois publié |
|---|---|---|
| `index.html` | Page d'accueil, bilingue | `https://olivier3dprint.github.io/PhotoCalcSite/` |
| `confidentialite.html` | Politique de confidentialité, bilingue (FR par défaut, `?lang=en` force l'anglais) | `.../confidentialite.html` |

La page d'accueil n'a pas de lien « Télécharger sur Google Play » actif : l'app n'est
pas encore publiée. Bandeau « BIENTÔT SUR GOOGLE PLAY » / « COMING SOON ON GOOGLE
PLAY » — à remplacer par un vrai lien une fois la fiche en ligne (chercher `bientot`
dans `index.html`).

**À faire, dans l'ordre** (commandes à lancer dans ton propre terminal — aucune
authentification GitHub ne passe par Claude) :

```bash
git clone https://github.com/olivier3dprint/PhotoCalcSite.git photocalc-site
```

```bash
xcopy /E /I /Y "D:\dev\PhotoCalc\playstore\index.html" photocalc-site\index.html
xcopy /E /I /Y "D:\dev\PhotoCalc\playstore\confidentialite.html" photocalc-site\confidentialite.html
```

```bash
cd photocalc-site
git add index.html confidentialite.html
git commit -m "Ajoute la page d'accueil bilingue et la politique de confidentialité"
git push
```

Si GitHub Pages n'est pas encore activé sur `PhotoCalcSite`, l'activer après le push
(Settings → Pages → branche `main` / dossier racine).

## Champs restant à remplir

⚠️ **La politique de confidentialité n'est PAS un champ par langue** dans la Play
Console (Surveiller et améliorer → Règles et programmes → Contenu de l'application →
Règles de confidentialité) — un seul champ pour toute l'application, d'où la page
bilingue unique `confidentialite.html`.

- **Politique de confidentialité** — coller l'URL `confidentialite.html` ci-dessus
  une fois GitHub Pages activé.
- **Site web** (facultatif) — `https://olivier3dprint.github.io/PhotoCalcSite/`.
- **Adresse e-mail de contact** — `olivier3dprint@gmail.com`.
- **Visuels** — produits dans les deux langues (voir section « Visuels » ci-dessus).
