# AplicacionWebEducativa

**Se desarrolla una aplicación Web educativa acerca de informática para todas las edades. Desde actividades simples en este área para los mas jóvenes hasta mas complejas para los adultos**


</br>

## Incluir Firebase al Proyecto (Código de Ejemplo)

### 1) Bibliotecas de Firebase( Dentro del index.html )
```
<script src="https://www.gstatic.com/firebasejs/7.14.4/firebase-app.js"></script>
<script src="https://www.gstatic.com/firebasejs/7.14.4/firebase-firestore.js"></script>

<script src="js/tuScriptParaFirestore.js"></script>
```


### 2) Inicializar una instancia de Cloud Firestore( Dentro de tu Script para Firestore js )
#### (Se deberá clickear "Agregar Aplicación" en la parte de configuraciones del proyecto al final de todo para obtener el apiKey y todo lo demás)
#### (La apiKey, auth y el proyectId lo encontrás en la parte de configuraciones de tu proyecto en la seccion Firebase SDK snippet)
```
// Initialize Cloud Firestore through Firebase
firebase.initializeApp({
  apiKey: '### FIREBASE API KEY ###',
  authDomain: '### FIREBASE AUTH DOMAIN ###',
  projectId: '### CLOUD FIRESTORE PROJECT ID ###'
});

var db = firebase.firestore();
```

### 3) Agregar Datos( Dentro del mismo js )
#### (Verifica en la consola del navegador si te responde la instancia creada)
```
db.collection("users").add({
    first: "Ada",
    last: "Lovelace",
    born: 1815
})
.then(function(docRef) {
    console.log("Document written with ID: ", docRef.id);
})
.catch(function(error) {
    console.error("Error adding document: ", error);
});

```
