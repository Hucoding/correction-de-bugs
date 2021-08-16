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
Les tests sont présents dans le fichier test/ControllerSpec.js
   - le premier test vérifie si les todos sont bien affichées (lignes 61 à 71)
   - Ce test vérifie si les todos "actives" s'affichent correctement (lignes 93 à 103)
   - Ce test vérifie si les todos "completed" s'affichent correctement (lignes 105 à 105)



    

      
     
    
    
