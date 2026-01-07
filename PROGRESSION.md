# Apprendre le Japonais - App Mobile

**Version** : 2.1.2
**Stack** : React Native / Expo SDK 54
**Mise a jour** : 7 janvier 2026

---

## Statut du Projet

```
Application                         [####################] 100%
Contenu (47 lecons, 450 exercices)  [####################] 100%
Audio VOICEVOX (250 fichiers)       [####################] 100%
Monetisation (RevenueCat + AdMob)   [####################] 100%
UI/UX Design Figma                  [####################] 100%
Publication Stores                  [                    ] Pret pour build
```

---

## Structure

```
JaponaisApp/mobile-app/
├── App.js
├── assets/audio/        # 250 MP3 VOICEVOX
└── src/
    ├── components/      # 21 composants
    ├── contexts/        # PremiumContext
    ├── data/            # Lecons (47)
    ├── screens/         # 11 ecrans
    ├── services/        # 22 services
    └── styles/          # Theme
```

---

## Ecrans

| Ecran | Description |
|-------|-------------|
| HomeScreen | Dashboard avec calendrier, Rank, Ki, quetes |
| LessonsScreen | Tabs categories + liste lecons |
| LessonDetailScreen | Liste caracteres, audio, tips |
| ExerciseScreen | Questions MCQ avec feedback cognitif |
| ProfileScreen | Avatar, stats, achievements, techniques |
| SettingsScreen | Notifications, vacances, danger zone |
| PaywallModal | Features grid, plans pricing |

---

## Services Principaux

| Service | Fonction |
|---------|----------|
| srsSystem | Algorithme SM-2 (repetition espacee) |
| confusionTracker | Tracking erreurs + feedback personnalise |
| livesSystem | Gestion vies (7 max, recharge 3h) |
| badgesSystem | 12 badges maitrise |
| premiumService | RevenueCat integration |
| exerciseService | Validation + feedback enrichi |
| audioService | Lecture audio VOICEVOX |
| notificationService | Rappels streak et quotidiens |

---

## Philosophie Anti-Duolingo

| Element | Implementation |
|---------|----------------|
| Feedback | Toast discret (pas ecran full-screen) |
| Couleurs | Bleu/teal correct, Orange incorrect |
| Progression | Texte "X / N" (pas barre arcade) |
| Gamification | Sobre, focus sur maitrise reelle |

---

## Commandes

```bash
# Dev local
cd JaponaisApp/mobile-app && npx expo start --clear

# Preview OTA
npx eas update --branch preview --message "Description"

# Build production
npx eas build --platform all
```

---

## Monetisation

| Plan | Prix |
|------|------|
| Mensuel | 7,99 EUR/mois |
| Annuel | 39,99 EUR/an (-58%) |
| Lifetime | 99,99 EUR |

---

## Prochaines Etapes

- [ ] Build production EAS
- [ ] Publication Play Store
- [ ] Publication App Store
- [ ] ASO (App Store Optimization)
