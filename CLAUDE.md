# CLAUDE.md

## Langue

- Parle-moi en français. Toujours.
- Code (variables, fonctions, commits, commentaires) en anglais.
- Messages de commit en anglais.

## Qui je suis

- Dev solo qui construit des produits digitaux avec l'IA (Claude Code, Cursor).
- Objectif : revenus passifs/semi-passifs, rester dans l'ombre (pas de personal brand).
- Projets actifs : MatchAudit (priorité), NinjaKana (attente), devis-plomberie.
- OS : Windows 11.

## Stack principal

### Web (tous mes projets web)

- Next.js (App Router, dernières versions)
- React 19
- TypeScript strict
- Tailwind CSS v4
- Supabase (auth + DB) ou Prisma selon le projet
- Déploiement : Vercel
- Paiements : Stripe ou LemonSqueezy

### Mobile (NinjaKana)

- React Native / Expo (SDK 54+)
- React Navigation
- RevenueCat pour les IAP
- EAS Build / EAS Submit

### IA

- Anthropic SDK (@anthropic-ai/sdk) pour les appels Claude
- OpenAI SDK quand nécessaire (CreatosOS)

## Style de code

- Minimal et concis. Pas de commentaires évidents.
- Commente uniquement la logique non-triviale.
- Pas de sur-ingénierie : la solution la plus simple qui fonctionne.
- Pas de fichiers/fonctions inutiles. Si c'est mort, supprime.
- Préfère les fonctions fléchées et les composants fonctionnels.
- Pas de `any` en TypeScript sauf cas exceptionnel justifié.
- Pas de `console.log` dans le code commité (utilise un logger si besoin).
- Imports : pas d'index barrels inutiles.

## Conventions

- Composants React : PascalCase, un composant par fichier.
- Fichiers/dossiers : kebab-case (convention Next.js App Router).
- Hooks custom : `use` prefix, dans un dossier `hooks/`.
- Types/interfaces : dans le même fichier si utilisés localement, sinon `types/`.
- Server Actions : dans le même fichier route ou dans `actions/`.
- Ne crée jamais de fichier `utils.ts` fourre-tout. Nomme précisément.

## Ce que je ne veux PAS

- Pas de refactoring non demandé.
- Pas de docstrings/JSDoc sauf si je le demande.
- Pas de tests sauf si je le demande.
- Pas de fichiers README ou documentation auto-générés.
- Pas d'emoji dans le code ou les commits.
- Ne propose pas d'alternatives "plus robustes" si ma solution fonctionne.
- Ne crée pas de fichiers `.env.example` ou de configs que je n'ai pas demandées.

## Git

- Commits courts et descriptifs en anglais.
- Ne push jamais sans que je le demande.
- Ne fais pas de commit sans que je le demande.
- Pas de `--force` sauf demande explicite.

## Workflow

- Pour toute tâche complexe ou multi-fichiers, commence en plan mode. Planifie d'abord, code ensuite.
- Utilise des subagents pour paralléliser les tâches lourdes (refacto, recherche large, modifications multi-fichiers).
- Quand je signale une erreur ou une correction, propose de mettre à jour ce CLAUDE.md avec une nouvelle règle pour ne pas la reproduire.
- Pour les bugs : tente de les fixer directement sans micro-management. Montre le résultat, pas le raisonnement étape par étape.
- Quand je te challenge ("prouve que ça marche", "grille-moi sur ces changements"), sois critique et rigoureux. Ne valide pas par complaisance.
- Si mon idée est trop grosse pour un MVP 2-3 semaines, dis-le et propose un starting point plus petit.
- Aide-moi à séparer "must have now" de "add later".

## Quand tu ne sais pas

- Demande. Ne devine pas les noms de tables Supabase, les clés API, ou l'architecture.
- Si tu dois faire un choix d'architecture, présente les options brièvement et laisse-moi choisir.

## Outils par phase

### Idéation / Concepts rapides

- **v0.dev** : UI concepts en secondes via prompt
- **Superdesign.dev** : Canvas infini type Figma, exploration rapide
- **Variant.ai** : Générer plusieurs directions UI en parallèle
- **aura.build** : Concepts UI rapides

### Design / Itération

- **Figma** : Itération, polish, détails (l'IA donne 60%, les 40% restants c'est Figma)

### Build / Code

- **Claude Code** : Principal. Comprend le codebase complet, ship du frontend sans attendre
- **Cursor** : Backup quand crédits Claude épuisés, ou projets spécifiques
- **Vibecodeapp** : Prototypes rapides avec APIs, DB, RevenueCat en quelques clics

### Images / Visuels

- **Midjourney** : Visuels custom, génération créative (image-to-video aussi)
- **Lummi.ai** : Photos stock haute qualité, style plus naturel que Midjourney parfois

### Motion / Animation

- **Jitter.video** : Animations rapides pour social/pitch
- **Claude Code + Remotion** : Vidéo programmatique, itération comme du code

### Landing pages

- **Carrd.co** : Simple, rapide, 19$/an
- **Super.so + Notion** : Plus flexible
- **Framer** : Plus design, tier gratuit

### Paiements (Merchant of Record)

- **LemonSqueezy** : Gère TVA/taxes pour toi
- **Polar** : Alternative à LemonSqueezy

### Email

- **ConvertKit** : Gratuit jusqu'à 1000 subs
- **EmailOctopus** : Alternative gratuite

### SEO / Recherche

- **Ubersuggest** : Recherche mots-clés gratuite
- **Semrush / Ahrefs** : Plus complet (payant)

### Outreach / Lead Gen

- **Instantly** : Cold email à scale (warm-up domaines, jusqu'à 1000 emails/jour)
- **gojiberry.ai** : Lead gen IA, intent signals automatisés

### Automatisation

- **n8n** : Automatisation drag & drop, gratuit (alternative à Zapier)
- **Clawdbot/OpenClaw** : Assistant IA sur WhatsApp/Telegram pour gérer des tâches

### MCP à venir

- **Framer MCP** : Automatiser le travail Framer tedieux (responsiveness, accessibilité)
- **Figma MCP** : Nettoyage design system, descriptions composants

## Checklist avant actions couteuses

Avant de lancer un build, un deploiement, ou une action qui consomme des ressources :

- Verifier les credits/quotas disponibles (EAS, Vercel, etc.)
- Verifier que les versions sont correctes et incrementees
- Verifier qu'il n'y a pas deja un build/deploy en cours
- Confirmer avec moi si doute

Apres chaque tache complexe :

- Resumer ce qui a ete fait
- Lister ce qui aurait pu etre mieux fait
- Proposer une regle CLAUDE.md si erreur evitable
