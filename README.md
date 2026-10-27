# Teapot Router

**Passerelle de modèles IA pour développeurs** — une seule clé pour Claude Code et le SDK OpenAI sur un endpoint unique.

Site officiel: <https://teapotrouter.com/fr>

## - **Double protocole** : Anthropic Messages (compatible Claude Code) et OpenAI Chat Completions (`/v1`) avec la même clé
- **Paiement à l'usage, tarifs publics**, avec API JSON gratuite (`/api/pricing`)
- **Historique des coûts par requête** : modèle, tokens et montant à chaque appel
- **Clés d'organisation et journal d'audit**
- **Basculement automatique multi-fournisseurs**

## Démarrage rapide (Claude Code)

```bash
export ANTHROPIC_BASE_URL=https://api.teapotrouter.com
export ANTHROPIC_AUTH_TOKEN=sk-xxxx
claude
```

## Démarrage rapide (OpenAI SDK / Codex CLI)

```bash
export OPENAI_BASE_URL=https://api.teapotrouter.com/v1
export OPENAI_API_KEY=sk-xxxx
```

## Tarifs

Paiement à l'usage (prépayé dès 1 $).
Tarifs: <https://teapotrouter.com/fr> / JSON: <https://teapotrouter.com/api/pricing>

## À propos

- Projet indépendant
- Le nom vient du code HTTP 418 « I'm a teapot » 🫖
- Contact : support@teapotrouter.com