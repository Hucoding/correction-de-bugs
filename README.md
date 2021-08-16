Todo-app - projet 8 :

1 ère étape corrections de bugs :

- La première erreur est une faute de frappe.
  -> Controller.js : erreur de frappe concernant à la ligne 95 du fichier.
  
  	Controller.prototype.adddItem = function (title) {  -> Controller.prototype.addItem = function (title) {
    
- Le deuxième introduit un conflit éventuel entre deux IDs identiques.
  -> store.js : en effet nous remarquons que le code qui gère les ids des items ne fait aucunes vérifications et se contente uniquement de générer des ids                aléatoires. (lignes 84 à 89). 
     Pour régler ce problème nous vérifions dans le tableau "todos" si l'id est existant si c'est le cas alors nous passons la variable "idIsUsed" à "true". Et tant      que cette variable est vrai nous générons un nouvel id différent. 
     
     Code complet de la solution (lignes 105 à 143) du fichier "store.js"
     
 - Un message dans la console qui n'a pas lieu d'être :
    <img width="1547" alt="Capture d’écran 2021-07-15 à 17 28 49" src="https://user-images.githubusercontent.com/53316189/125815229-ccdd0716-2b20-4cfd-8a9d-c6c52d9a68f5.png">
    
    Après vérifications et recherche j'ai constaté que le fichier appeler ligne 248 du fichier base.js du dossier => todomvc-common est inexistant
    J'ai donc supprimer cette ligne.
    
 - Un id est manquant sur la flèche id="toggle-all" au niveau du fichier index.html à la ligne : 16

Tests unitaires :
Les tests sont présents dans le fichier test/ControllerSpec.js. 
9 de tests unitaires on été réalisés dans ce fichier.

   - le premier test vérifie si les todos sont bien affichées (lignes 61 à 74)
   - Ce test vérifie si les todos "actives" s'affichent correctement (lignes 96 à 110)
   - Ce test vérifie si les todos "completed" s'affichent correctement (lignes 112 à 126)
   - Ce test vérifie que l'onglet "All" est chargé correctement lorsque l'utilisateur arrive sur la page (lignes 171 à 193)
   - Ce test vérifie que l'onglet "Active" s'active correctement lorsque l'utilisateur clique dessus (lignes 185 à 198)
   - Ce test vérifie si le bouton "toggleAll" est bien fonctionnel et que la séléction des todos l'est également (lignes 201 à 224)
   - Ce test effectue une vérification pour voir si l'application mets à jours la vue (test en liens avec toggleAll) (lignes 226 à 250)
   - Ce test effetue une vérification pour voir si la note est bien ajouté à la liste actuelle (lignes 254 à 271)
   - Ce test effetue une vérification pour voir si la note est bien supprimé de la liste (lignes 309 à 328)



    

      
     
    
    
