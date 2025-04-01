https://google.github.io/comprehensive-rust/es/types-and-values/values.html

# rust notes
# Que es rust?
Rust es un lenguaje de programacion de sistemas de codigo abierto que puede usar para desarrollar software seguro y eficaz. 
## En rust declaramos una funcion 
fn main(){
 println!("hello world");

}

fn main(){
    let= x: i32 = 5;
    let y = i32;

    assert_eq!(x,5);
    println!("Success!") ; 
}

1.Las funciones se introducen con fn. 
2. Los bloques se dlimitan con llaves, como en C y c++ 
3. La funcion main es el punto de entrada adel programa. 
4. rust tiene macros higienicas, como por ejemolo println!
5. Las cadenas de rust estan codificiadas en UTF-8 y pueden conetener caracteres Unicode

## Variables

Rust ofrece seguridad de tipos mediante tipado estatico. Los enlances a variables son hechos con let: 

fn main() {

let x: i32 = 10;
println!("x: {x}");
// x= 20 
// println!("x:{x}");


}

## Valores 

Los tipos tienen la siguiente anchura:

iN, uN, and fN son N bits de capacidad,
isize y usize tienen el ancho de un puntero,
char tiene un tamaño de 32 bits,
bool tiene 8 bits de ancho.

## Aritmetica 

fn interproduct(a:i32, b:i32, c:i32) => i32{

return a*b+ b * c/c *a;

}

fn main() {
    println!("resultado: {}", interproduct(120, 100, 248));
} 


## Inferencia de tipos 

fn takes_u32(x:u32){

    println!("u32:{x}");

}

fn takes_i8(y:i8){
    println!("i8":{y});

}


fn main(){
    let x = 10;
    let y = 20;


    takes_u32(x);
    takes_i8(y);
}

## Ejercicio : fibonacci. 

### La secuencie de Fibonacci empieza con [0, 1]. Para n>1, el número de Fibonacci en la posición n se calcula de forma recursiva como la suma de los números de Fibonacci n-1 y n-2.

Escribe una función fib(n) que calcule el número n de Fibonacci. ¿Cuándo da error pánico esta función?
fn fib(n: u32) -> u32 {
    if n < 2 {
       return n;
    } else {
         return fib(n - 1) + fib(n - 2);
    }
}

fn main() {
    let n = 20;
    println!("fib({n}) = {}", fib(n));
}