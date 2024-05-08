import prompt from 'prompt';
// Pedir nombre de usuario al alumno. 
let nombreAlumno= prompt("Ingrese nombre de alumno")

// Pedir nombre de materias. 
let materia= prompt("Ingrese el nombre de la materia")

//Pedir las tres notas por usario 

let nota1= parseFloat(prompt("Ingrese la primera nota (de 0 a 10)"))
let nota2= parseFloat(prompt("Ingrese la segunda nota (de 0 a 10)"))
let nota3= parseFloat(prompt("Ingrese la tercera nota (de 0 a 10)"))

// Corroborar que las notas se encuentren dentro de un rango válido (0 a 10). 
if(isNaN(nota1)||isNaN(nota2)||isNaN(nota3)|| nota1 < 0 || nota1 >10|| nota2< 0 || nota2 >10 || nota3<  0 || nota3 > 10){
     console.log("Por favor, ingrese una nota válida, en el rango de 0 a 10.")
     console.log("NOTA1..."+ nota1)
     console.log("NOTA2..."+ nota2)
     console.log("NOTA3..."+ nota3)
}  else{ // Una vez corroborado las condiciones, realizamos el promedio.
 console.log("NOTA2..."+ nota2)
 console.log("NOTA3..."+ nota3)
 let promedio= (nota1+ nota2+ nota3)/3
 console.log("PROMEDIO..."+promedio)

 if(promedio>=7){
     console.log('Felicidades ${nombreAlumno},la materia ${materia}, la aprobaste correctamente con un promedio de ${promedio}.')
     }
      else {
      console.log('Muchas gracias por tu esfuerzo  ${nombreAlumno},desafortunadamente tu promedio es ${promedio} y no es suficiente para aprobar la materia. ')
     }
}
