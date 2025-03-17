Proyecto Amigo Secreto
Este es mi pequeño proyecto en JavaScript para realizar un sorteo de "Amigo Secreto", el cual permite ingresar nombres de participantes y seleccionar aleatoriamente uno de ellos. Los usuarios pueden acceder al proyecto a través de los siguientes enlaces:

Repositorio en GitHub: https://github.com/Tamara0222/Challenge-Amigo-Secreto.git
Demo en GitHub Pages: https://tamara0222.github.io/Challenge-Amigo-Secreto/ 
Características
Permite agregar nombres a una lista.
Realiza un sorteo aleatorio entre los participantes.
Muestra el resultado del sorteo en pantalla.
Tecnologías utilizadas
HTML
CSS
JavaScript
Cómo usarlo
Escribe el nombre de un participante en el campo de entrada.
Haz clic en el botón "Agregar" para añadirlo a la lista.
Una vez añadidos todos los participantes, haz clic en "Sortear" para obtener un amigo secreto.
Código principal
javascript
Copiar código
const inputAmigo = document.getElementById("amigo");
const listaAmigos = [];
const ulListaAmigos = document.getElementById("listaAmigos");
const ulResultado = document.getElementById("resultado");

function agregarAmigo(){   
    if (inputAmigo.value.trim() === "") {
        alert("Por favor, ingresa un nombre válido.");
        return;
    }
    listaAmigos.push(inputAmigo.value);
    ulListaAmigos.innerHTML += `<li>${inputAmigo.value}</li>`;
    inputAmigo.value = "";
};

function sortearAmigo(){
    if (listaAmigos.length === 0){
        alert("No hay amigos para sortear. Agrega nombres primero.");
        return;
    }
    const random = Math.floor(Math.random() * listaAmigos.length);
    const amigoSecreto = listaAmigos[random];
    ulResultado.innerHTML = `<li>El amigo secreto es: ${amigoSecreto}</li>`;
}
Mejoras posibles
Evitar que una persona se asigne a sí misma como su amigo secreto.
Implementar un diseño más atractivo con CSS.
Agregar la opción de reiniciar el sorteo.
Desarrollado por
Tamara Saavedra Rojas
