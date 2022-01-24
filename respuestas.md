//1,2 y 3 fueron hechos en clases.


// Encuentra si existe un restaurante cuyo nombre sea "Cafe Espanol"    
 db.restaurants.find({name:"Cafe Espanol"}).count() 
  Resultado 2
 
 // Encuentra todos los restaurantes que, en su nombre (name), contengan la palabra 'Cafe'. Debes
usar una expresion regular
  db.restaurants.find({"name" : {$regex : "Cafe"}}).count()
  Resultado 1650
  
  // Encuentra todos los restaurantes que esten en el edificio "41" o "66"
  db.restaurants.find({$or: [{"address.building" : "66"},{"address.building" : "41"}]}).count()
  Resultado 62
  
