# Rendu — API de citation

Vérifications effectuées avec `curl -i` sur le serveur local .

## `GET /citations`

- **Statut :** `200 OK`
- **Contenu :**

  ```json
  [{ "id": 1, "texte": "Apprendre en pratiquant.", "auteur": "Équipe du TP" }]
  ```

- **Content-Type :** `application/json; charset=utf-8`
- **Format renvoyé :** JSON (un tableau de citations).

## `GET /inconnue`

- **Statut :** `404 Not Found`
- **Contenu :**

  ```json
  { "message": "Route introuvable" }
  ```

- **Content-Type :** `application/json; charset=utf-8`
- **Format renvoyé :** JSON ( un objet contenant le message d’erreur).

## Rôle de `req` et `res`

`req` représente la requête HTTP envoyée par le client : elle contient notamments la méthode et l’URL demandées . `res` sert à construire et envoyer la réponse du serveur, notamment son statut ,ses en-têtes et son contenu.

## Formats des réponses

- **`GET /ping` — `Content-Type: text/plain; charset=utf-8` :** texte brut (« Serveur de citations prêt.»).
- **`GET /citations` — `Content-Type: application/json; charset=utf-8` :** JSON ( tableau de citations).
