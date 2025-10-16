function ejercicioUno (a = 0, b = 0, operation = suma) {
  switch (operation) {
    case suma:
      return console.log(a + b);
    case resta:
      return console.log(a - b);
    case multiplicacion:
      return console.log(a * b);
    case division:
      return console.log(a / b);
    default:
      console.error(La operacion {operation}no es valida!!);
  }
}

//EJECUCION DE FUNCIONES
ejercicioUno(2);

function ejercicioDos(a = 0, b = 0){
  let nums=[];
  for(let i = a; i <=b; i++){
    if(i % 2 === 0) nums.push(i);
  }
  console.log(nums);
}

//EJECUCION DE FUNCIONES
ejercicioDos(1,20);

function ejercicioTres(a = 0, x = 12){
  for(let i = 0; i <= x; i++){
    if(i != 5) console.log(${a} X ${i} = ${a * i});
  }
}

//EJECUCION DE FUNCIONES
ejercicioTres(5, 20);

function ejercicioCuatro(){
  let nums = [];
  let multiplos = [];
  for(let i = 1; i <=100; i++){
    nums.push(i);
  }
  console.log(Este es el arreglo principal: ${nums});
  nums.filter((el)=>{
    if(el % 3 === 0) multiplos.push(el)
  });
  console.log(Estos son los numeros que son multiplos del 3 ${multiplos});
}

//EJECUCION DE FUNCIONES
ejercicioCuatro();

function ejercicioCinco(){
  let num = Math.floor(Math.random() * (1000 - 1)+1);
  console.log(El numero es ${num});
  let mitad = num / 2;
  let doble = num * 2;
  let raiz = Math.sqrt(num);
  console.log(La mitad de ${num} es ${mitad}. El doble de ${num} es ${doble}. La raiz de ${num} es ${raiz});
}

//EJECUCION DE FUNCIONES
ejercicioCinco();

function ejercicioSeis(a = "11 nov 2022"){
  let cumple = new Date(a);
  let hoy = new Date();
  let diasRestantes = Math.floor((cumple.getTime() - hoy.getTime()) / (1000 * 60 * 60 * 24));
  console.log(Tu cumpleaños es ${cumple} y faltan ${diasRestantes} dias.);
}

//EJECUCION DE FUNCIONES
ejercicioSeis();

function ejercicioSiete(text = "Hola mundo"){
  let words = text.split(" ");
  console.log(words);
}

//EJECUCION DE FUNCIONES
ejercicioSiete();
ejercicioSiete("Luis Angel Fernandez");

function ejerciciOcho(){
  const personas = [;
  {
  nombre: "Luis"
  apellido:"Fernandez"
  edad:"19"
  },
  {
  nombre: "Luis"
  apellido:"Santos"
  edad:"10"
  },
  {
  nombre: "Kiko"
  apellido:"Perez"
  edad:"28"
  },
  {
  nombre: "Ramon"
  apellido:"Martinez"
  edad:"22"
  },
  {
  nombre: "Luis"
  apellido:"Alvarez"
  edad:"12"
  }
console.log("personas");
console.log("PERSONAS QUE SE LLAMAN LUIS");
personas.filter((el)=>{
if(el.nombre === "Luis") console.log(´${el.nombre} ${el.apellido}´)
});
console.log("MAYORES DE EDAD");
personas.filter((el)=>{
  if(el.edad >= 18) console.log(´${el.nombre} ${el.apellido}´)- $(el.edad)
  });
}

//EJECUCION DE FUNCIONES
ejercicioOcho();




function ejercicioNueve(open = "", close = ""){
  if(open === "" || close === "") return console.error('Faltan parametros');
  else{
    let today = new Date();
    let testOpen = new Date(open);
    let testClose = new Date(close);

    let resultTimeOpen = Math.floor((testClose.getTime() - testOpen.getTime()) / (1000 * 60));
    let resultTimeRest = Math.floor((testOpen.getTime() - today.getTime()) / (1000 * 60));
    /* console.log(resultTimeOpen, resultTimeRest); */

    if(testClose.getTime() < today.getTime()) return console.log("El examen ya cerró");
    else{
      if(resultTimeRest > 0) console.log(Faltan ${resultTimeRest} minutos para que el examen abra);
      else{
        console.log("El examen está abierto");
        console.log(El examen durará abierto ${resultTimeOpen} minutos.);
      }
    }
//EJECUCION DE FUNCIONES
ejercicioNueve('Wed Dec 14 2022 11:00:00', 'Wed Dec 14 2022 15:00:00');

function ejercicioDiez(){
  const nums = [1,2,3,4,5,6,4,2,1];

  let result = nums.filter((item, index)=>{
    return nums.indexOf(item) === index
  });

  console.log(Arreglo original: ${nums});
  console.log(result);

  //SEGUNDA FORMA
  let newNums = new Set(nums);
  //console.log(newNums);
  let result2 = [...newNums];
  console.log(result2);
}

//EJECUCION DE FUNCIONES
ejercicioDiez();
