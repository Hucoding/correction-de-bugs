# correction-de-bugs

1 ère étape :
- Le premier est une faute de frappe.
  -> Controller.js : erreur de frappe concernant à la ligne 95 du fichier.
  
  	Controller.prototype.adddItem = function (title) {  -> Controller.prototype.addItem = function (title) {
    
- Le deuxième introduit un conflit éventuel entre deux IDs identiques.
  -> store.js : en effet nous remarquons que le code qui gère les ids des items ne fait aucunes vérifications et se contente uniquement de générer des ids                aléatoires. (lignes 84 à 89). 
      
     
    
    
