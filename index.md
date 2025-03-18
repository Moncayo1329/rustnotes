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