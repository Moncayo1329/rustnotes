# Tuplas y arrays 

Arrays 

fn main () { 
    let mut a:[i8;10] = [42;10];
    a[5] = 0;
    println!("a:{a?}");
}

## Tuplas

fn main(){
let t:(i8,bool)= (7,true);
println!("t,0:{}, t.0");
println!("t.1: {}", t.1);



}

git 

## Iteracion de Arreglos (Arrays)

### La instruccion for permite iterar sobre arrays, poero no sobre tuplas
fn main() {
    let primes = [2, 3, 5, 7, 11, 13, 17, 19];
    for prime in primes {
        for i in 2..prime {
            assert_ne!(prime % i, 0);
        }
    }
}

### This slide should take about 3 minutes.
### Esta función usa el trait IntoIterator, pero aún no lo hemos estudiado.

### La macro assert_ne! es nueva. También existen las macros assert_eq! y assert!. Estas variantes siempre se comprueban mientras las variantes de solo depuración, como debug_assert!, no compilan nada en las compilaciones de lanzamiento. 


## Patrones y desestructuracion. 

