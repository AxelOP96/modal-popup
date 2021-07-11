# modal-popup

*Funciones*

Primero seleccionamos el elemento con la clase modal y lo asignamos a una constante, hacemos lo mismo con la clase btn y la clase close.
const modal = document.querySelector(".modal"),
  btn = document.querySelector(".btn"),
  close = document.querySelector(".close");


Asignamos a la constante btn un addEventListener que al hacer click llame a una funcion en este caso openModal
btn.addEventListener("click", openModal);
Asignamos a la constante close un addEventListener que al hacer click llame a la funcion closeModal
close.addEventListener("click", closeModal);
modal.addEventListener("click", closeModal);

Se crea la funcion openModal y le pasamos por parametro el evento, dentro de la funcion le aplicamos al div el estilo de display block, para que tenga las caracteristicas de un elemento de bloque. 
function openModal(e) {
  e.preventDefault();
  modal.style.display = "block";
}
Se crea la funcion de closeModal que le aplica al div de modal el estilo de display none para que desaparezca.
function closeModal() {
  modal.style.display = "none";
}
