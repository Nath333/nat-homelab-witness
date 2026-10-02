# nat-homelab-witness

Témoin EXTERNE du homelab (NAT Home Server 192.168.2.100).

Le homelab publie « vivant » toutes les 5 min sur un topic ntfy.sh secret
(`VIVANT_TOPIC`). Ce dépôt fait tourner un workflow GitHub Actions toutes les
10 min sur les runners GitHub (toujours vivants) : si aucun « vivant » depuis
25 min, il publie une alerte haute priorité sur `ALERT_TOPIC` (= le topic
ntfy.sh reçu par le téléphone).

Pourquoi public : les runners GitHub-hosted sont gratuits et illimités sur les
dépôts publics. Les noms de topics restent cachés (secrets GitHub).
Pourquoi ce témoin : Kuma vit SUR le homelab — un gel nocturne le tue avec la
machine. Le PC-témoin est éteint la nuit. GitHub, lui, ne dort jamais.
