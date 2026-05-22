# ⚽ FLEA — Foot Loisir Entre Amis

Application web de gestion de l'association **Foot Loisir Entre Amis** (saison 2025-2026).

## 🚀 Déploiement rapide sur Netlify

1. Crée un compte sur [netlify.com](https://netlify.com) (gratuit)
2. Connecte ton compte GitHub
3. Clique **"Add new site" → "Import an existing project"**
4. Sélectionne ce repo
5. Laisse les paramètres par défaut → **Deploy site**
6. Ton site est live ! Personnalise l'URL dans les paramètres Netlify.

## ✏️ Comment modifier le contenu

Ouvre `index.html` dans n'importe quel éditeur de texte (Notepad, VS Code...).

Utilise **Ctrl+F** et cherche `MODIFIER ICI` pour trouver les zones à éditer.

### Modifications courantes

| Ce que tu veux modifier | Cherche dans le fichier |
|---|---|
| Prochain match (adversaire, date) | `MODIFIER ICI : journée et infos du prochain match` |
| Présences d'un match | `MODIFIER ICI : liste des présences` |
| Résultat d'un match | Section `Passés` dans `sec-calendar` |
| Stats d'un joueur | `MODIFIER ICI : top buteurs` ou section `sec-players` |
| Budget / dépenses | `MODIFIER ICI : chiffres budget` |
| Tâches | Section `sec-tasks` |
| Trophées fin de saison | `MODIFIER ICI à la fin de saison` |

### Ajouter un match passé

Copie ce bloc dans la section "Passés" du calendrier et change les valeurs :

```html
<div class="event-card" data-type="match" style="opacity:0.72">
  <div class="event-date"><div class="event-day">29</div><div class="event-month">Mai</div></div>
  <div class="event-sep"></div>
  <div class="event-info">
    <div class="event-type-label type-match">Match · J14</div>
    <div class="event-title">FLEA 4 – 2 FC Adversaire</div>
    <div class="event-meta"><span class="score-badge res-v">Victoire 4-2</span></div>
  </div>
</div>
```

Classes résultat : `res-v` (victoire) · `res-d` (défaite) · `res-n` (nul)

### Ajouter un joueur

Copie ce bloc dans la section joueurs et personnalise :

```html
<div class="player-card">
  <div class="av av-lg av-gold">XX</div>  <!-- Initiales + couleur avatar -->
  <div class="player-info">
    <div class="player-name">Prénom Nom</div>
    <div class="player-role">Poste</div>
    <div class="player-stats-row">
      <div class="pstat"><strong>0</strong> matchs</div>
      <div class="pstat"><strong>0</strong> buts</div>
    </div>
  </div>
</div>
```

Couleurs avatar : `av-gold` · `av-blue` · `av-green` · `av-red` · `av-purple` · `av-orange`

## 📱 Partager l'appli

Une fois déployée sur Netlify, partage simplement le lien (ex: `flea-foot.netlify.app`) dans le groupe WhatsApp. Le site fonctionne sur mobile comme une appli.

## 🔮 Étapes suivantes

- **Supabase** : pour avoir des données live (présences, stats qui se mettent à jour en temps réel)
- **Notifications WhatsApp** : via Whapi.cloud pour prévenir automatiquement le groupe

## 📁 Structure du projet

```
flea-app/
├── index.html      ← Tout l'app est ici
├── netlify.toml    ← Config déploiement
└── README.md       ← Ce fichier
```

---
*Saison 2025-2026 · FLEA — Foot Loisir Entre Amis · Montélimar*
