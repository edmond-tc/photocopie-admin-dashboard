# Admin Gestion Photocopie — tableau de bord

Cloudflare Workers + D1 + R2. Miroir public (sans secrets) du dossier
`admin/` de edmond-tc/Photo (dépôt privé), pour permettre le déploiement
via le bouton "Deploy to Cloudflare".

Au déploiement, il te sera demandé deux valeurs :
- `ADMIN_PASSWORD` : le mot de passe pour te connecter au tableau de bord.
- `LICENSE_SECRET` : copie exacte de la constante `SECRET` dans
  `src-tauri/src/license.rs` du dépôt principal — doit être identique,
  sinon les clés générées ici ne marcheront pas dans l'application.

Après déploiement : va dans **Paramètres** pour renseigner tes numéros
Mobile Money et ton contact WhatsApp (affichés aux gérants sur
`/renouveler`), et dépose ton `.exe` dans le bucket R2
`photocopie-telechargements` (nom exact : `GestionPhotocopie-Installateur.exe`)
pour activer la page `/telecharger`.
