<div align="center">

# Teapot Router — passerelle API LLM pour agents de code

**Une clé. Deux protocoles. Paiement à l'usage — et le solde n'expire jamais.**

Passerelle hébergée pour Claude Code, Codex CLI et les outils OpenAI SDK : changez deux variables d'environnement et tous vos outils de code IA passent par un seul endpoint, un seul solde, un registre de coûts par requête.

[Commencer](https://teapotrouter.com/fr/register) · [Tarifs — publics, JSON lisible par machine](https://teapotrouter.com/api/pricing) · [Documentation](https://teapotrouter.com/fr/docs)

</div>

---

## Pourquoi une passerelle pour les agents de code ?

Si vous utilisez Claude Code à côté d'outils OpenAI SDK, vous connaissez le problème : chaque outil veut son endpoint et sa clé, et la facture devient une boîte noire mensuelle.

Une passerelle remet la plomberie en ordre :

| | Connexion directe (par fournisseur) | Via passerelle |
| --- | --- | --- |
| Endpoints & clés | un par fournisseur | **une clé, deux protocoles** |
| Facturation | N tableaux de bord, totaux mensuels | un solde, **registre par requête** |
| Visibilité des coûts | « c'était $84 » | « cette session a coûté $6.20 — 78 % de contexte renvoyé » |
| Conditions | politique par fournisseur | ici : **solde sans expiration**, remboursement au solde restant |

## Configuration : deux variables d'environnement

```bash
# Claude Code (protocole Anthropic)
export ANTHROPIC_BASE_URL="https://api.teapotrouter.com"
export ANTHROPIC_AUTH_TOKEN="sk-****"

# OpenAI SDK / Codex CLI — même clé, endpoint /v1
# base_url = https://api.teapotrouter.com/v1
```

Guides pas à pas (inscription → première requête → dépannage) : [teapotrouter.com/fr/docs](https://teapotrouter.com/fr/docs)

## Ce que vous pouvez voir sur le site

- **Tarifs publics** — tarif de base et prix réellement payé pour chaque modèle, avec un endpoint JSON sans connexion ([`/api/pricing`](https://teapotrouter.com/api/pricing)) pour comparer par script
- **Page de tarifs par modèle** — ex. [claude-opus-5-5](https://teapotrouter.com/fr/pricing/claude-opus-5-5)
- **Guide tarifaire Claude Code** — abonnement vs à l'usage vs passerelle, avec le vrai calcul : [documentation](https://teapotrouter.com/fr/docs/claude-code-pricing)
- **Guide de dépannage** — connexion, 401 et erreurs de quota associés à leur solution : [documentation](https://teapotrouter.com/fr/docs/claude-code-troubleshooting)

## Deux questions à poser à toute passerelle (y compris celle-ci)

- **D'où viennent les modèles ?** De canaux API officiels/autorisés, mesurés et payés à l'usage. Pas de comptes partagés, pas de revente d'abonnements.
- **Qu'est-ce qui est journalisé ?** Seulement les métadonnées de facturation (modèle, tokens, coût, latence) — c'est ce qui rend le registre par requête possible. Pas de théâtre « zéro log » ; nous ne touchons pas au contenu des conversations.

## Limites honnêtes

Projet solo, lancé récemment, sans budget marketing — l'endpoint de tarifs affiche toujours la liste vivante des modèles : vérifiez par vous-même plutôt que de croire ce README. Le failover multi-amont est intégré, mais une passerelle reste une dépendance : gardez une route de secours.

Contact : support@teapotrouter.com

---

<div align="center">

Le nom vient du code HTTP 418 « I'm a teapot » 🫖 — [toute l'histoire](https://teapotrouter.com/fr/418)

**[Teapot Router](https://teapotrouter.com/fr)** — passerelle IA stability-first pour Claude Code et GPT.

</div>
