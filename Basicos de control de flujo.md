# Basicos de control de flujo 

Diapositiva	Duración
Expresiones if	4 minutos
Bucles	           5 minutos
break y continue	4 minutos
Bloques y ámbitos	5 minutos
Funciones	          3 minutos
Macros	           2 minutos
Ejercicio: secuencia de Collatz	15 minutos

# Expresiones if 
Puedes usar expresiones if de la misma forma que en otros lenguajes. 
fn main() {
    let x = 10;
    if x == 0 {
        println!("cero!");
    } else if x < 100 {
        println!("muy grande");
    } else {
        println!("enorme");
    }
}

Además, puedes utilizar if como expresión. La última expresión de cada bloque se convierte en el valor de la expresión if 

fn main() {
    let x = 10;
    let size = if x < 20 { "pequeño" } else { "grande" };
    println!("tamaño del número: {}", size);
} 

# Bucles 

hay tres palabras clave de bucle en rust : while, loop y for: 
Bucle (while)
Qué es:
Ya lo vimos: repite un bloque de código mientras se cumpla una condición.
Loop
Qué es:
## Un loop es un bucle que se ejecuta sin detenerse por sí mismo; es como un ciclo que se repite infinitamente.

## bucles while. La palabra clase while es muy similar a la de otros lenguajes y ejecuta el cuerpo del bucle mientras que la condicion sea valida. 

## Qué es:
Un for se usa para recorrer una colección de elementos o un rango de números. 
Este bucle recorre los números del 0 al 4 y ejecuta el bloque de código para cada número.

Ventaja:
Es muy útil cuando sabes cuántas veces necesitas repetir algo o cuando trabajas con listas, arreglos u otros conjuntos de datos.

fn main() {
    let mut x = 200;
    while x >= 10 {
        x = x /2;
    }

    printl!(x final:{x}");
}


# break y continue 

Si quieres iniciar inmediantamente la siguiente iteracion, usa contiene. 
Si quieres salir de un bucle antes de que termine, usa

n main() {
    let mut i = 0;
    loop {
        i += 1;
        if i > 5 {
            break;
        }
        if i % 2 == 0 {
            continue;
        }
        println!("{}", i);
    }
}


# Etiquetas 
de forma opciona, tanto continue como break pueden utilizar un argumento de etiqueta para interrumpir los bucles anidados. 
fn main() {
    let s = [[5, 6, 7], [8, 9, 10], [21, 15, 32]];
    let mut elements_searched = 0;
    let target_value = 10;
    'outer: for i in 0..=2 {
        for j in 0..=2 {
            elements_searched += 1;
            if s[i][j] == target_value {
                break 'outer;
            }
        }
    }
    print!("elementos travesados: {elements_searched}");
}
