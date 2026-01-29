# NinjaKana - Progression

**Mise a jour** : 29 janvier 2026

---

## Statut

| Plateforme | Version | Etat |
|------------|---------|------|
| iOS | 1.0.1 (build 13) | ⏳ Soumis pour examen Apple le 29 janv. 2026 (en attente de verification) |
| Android | 1.0.0 (versionCode 7) | ✅ Build reussi — .aab pret, soumettre apres 2 fev |

---

## A faire

- [x] Recuperer build iOS (EAS) → build 11 finished
- [x] Relancer build Android (fix lint ExtraTranslation) → build reussi, .aab pret
- [x] iOS 1.0.1 build 13 : build reussi + uploade sur App Store Connect
- [x] Version 1.0.1 creee dans App Store Connect, build 13 selectionne, soumis pour examen le 29 janv.
- [ ] Soumettre Android pour examen sur Play Store (apres 2 fev)
- [ ] Migration compte Apple Developer → Organisation (DUNS demande, 5-14 jours)
- [ ] Ajouter les vrais IDs AdMob iOS (actuellement placeholders)
- [ ] Ecrire articles SEO (difference hiragana/katakana, guide JLPT N5)
- [ ] Creer sitemap.xml
- [ ] Creer pins Pinterest (tableaux kana)
- [ ] Rejoindre groupes Facebook japonais
- [ ] Outreach YouTubers/blogueurs

---

## Fait

- ✅ iOS publie sur l'App Store
- ✅ ASO Play Store
- ✅ Article SEO : apprendre-hiragana.html
- ✅ Article SEO : tableau-hiragana-complet.html
- ✅ Google Search Console + indexation demandee
- ✅ Contrats Apple (fiscal W-8BEN, compte bancaire PostFinance, Paid Apps + Free Apps actifs)
- ⏳ **DSA (Digital Services Act)** : formulaire soumis le 28 janv. 2026, en cours de verification par Apple
  - 27 pays UE (dont France) en "Vente impossible" en attendant validation
  - 148 pays disponibles en attendant
- ✅ **Fix build Android** : plugin Expo `withDisableExtraTranslationLint` ajoute
  - Cause : locales/fr.json contient des cles iOS (CFBundleDisplayName, NSUserTrackingUsageDescription)
  - Le lint Android echouait sur ExtraTranslation dans values-b+fr/strings.xml
  - Build Android relance et reussi (versionCode 7, .aab pret)
- ✅ **Version bump iOS** : 1.0.0 → 1.0.1 (build 13)
  - Build 11 (1.0.0) ne pouvait pas etre soumis (version deja existante sur ASC)
  - Nouveau build 13 (1.0.1) lance avec auto-submit
  - Build reussi + uploade sur App Store Connect avec succes
- ✅ **Soumission iOS 1.0.1** : soumis pour examen Apple le 29 janv. 2026
  - Description ASO optimisee (nouvelle description marketing)
  - Texte promotionnel ajoute
  - Notes de version ajoutees
  - Publication automatique activee
- ✅ **Fix NSUserTrackingUsageDescription** : ajoute dans infoPlist de app.json (pour prochain build)
- ✅ Landing page Carrd mise a jour (lien App Store)
- ✅ **Monetisation v2** :
  - Content gate : 5 lecons gratuites par categorie, le reste = Premium
  - Limite quotidienne : 25 exercices/jour (reset minuit)
  - Bonus pub : +10 exercices par pub rewarded (max 3/jour)
  - Bonus SRS : +5 exercices par session de revision
  - PaywallModal mis a jour (feature "Toutes les lecons" + accents corriges)
- ✅ **Corrections UI** :
  - Accents francais corriges partout (ExerciseScreen, PaywallModal)
  - Taille texte stat cards reduite (overflow)
  - Bouton fermer PaywallModal repositionne (chevauchement status bar)
  - Timer countdown avec secondes sur ecran limite quotidienne
- ✅ **Corrections HomeScreen** :
  - Quetes du jour dynamiques (etaient hardcodees avec fausses valeurs)
  - Streak demarre a 0 (etait a 1 des l'ouverture)
  - Calendrier coeurs base sur le streak reel (etait rouge pour tous les jours)
  - Rank demarre a 0 pour nouveaux utilisateurs
- ✅ **Locale francaise** : app.json configure pour afficher "French" sur le Store

---

## Architecture monetisation

```
FREE                              PREMIUM
─────────────────────────         ─────────────────────────
5 lecons / categorie              Toutes les lecons
25 exercices / jour               Exercices illimites
7 vies (recharge 3h)              Vies illimitees
Pubs affichees                    Sans pub
Bonus: pub (+10 exos, 3x/j)      SRS illimite
Bonus: SRS (+5 exos)
```

Les lecons 6+ sont BLOQUEES : ni le temps, ni les pubs ne les debloquent.

---

## Liens

- [App Store](https://apps.apple.com/app/id6757958764)
- [Play Store](https://play.google.com/store/apps/details?id=com.apprendre.japonais)
- [Landing Page](https://ninjakana.carrd.co)
- [App Store Connect](https://appstoreconnect.apple.com)
- [Play Console](https://play.google.com/console)
- [RevenueCat](https://app.revenuecat.com)
- [Google Search Console](https://search.google.com/search-console)
- [Blog](https://ninjakana.github.io/App/blog/)
- [MARKETING_STRATEGY.md](./MARKETING_STRATEGY.md)
