### Los enum compartidos es como esa caja de crayones es una lista de nombres que todos pueden usar y entender, sin necesidad de crear nuevas listas cada vez 

## Ejemplo si estas jugando con tus amigos  y quieren elegir un color de la caja, todos pueden usar los mismos nombres sin confunsion.

### En programacion, esto ayuda a que diferencias partes de un programa que usen los mismo valores sin equivocarse. 

public enum ColorCrayon {
 rojo, 
 azul,
 verde
}

ColorCrayon mi Color = ColorCrayon.Rojo;

Ventajas de usar enums compartidos en backend
✔ Evitan errores al escribir strings manualmente.
✔ Hacen el código más claro y fácil de mantener.
✔ Permiten que el frontend y el backend usen los mismos valores sin inconsistencias.
✔ Se pueden mapear fácilmente a bases de datos o APIs. 

Si tienes un backend para una tienda en línea, puedes usar un enum para definir los posibles estados de una orden: 

public enum EstadoOrden {
    Pendiente,
    Pagada,
    Enviada,
    Entregada,
    Cancelada
}
 ### en la base de datos

 orden.Estado = EstadoOrden.Pagada;

 En una API:

 if(orden.Estado == EstadoOrden.Enviada) {
NotificarCliente("Tu pedido ha sido enviado.");

 }


 ### Referencias Exclusivas 

 #### Las referencias exclusivas, también denominadas referencias mutables, permiten cambiar el valor al que hacen referencia. Tienen el tipo &mut T

 n main() {
    let mut point = (1, 2);
    let x_coord = &mut point.0;
    *x_coord = 20;
    println!("point: {point:?}");
} 

### slices 
Un slice es una parte de una coleccion, como un array. Se usan para acceder a una seccion de datos sin necesidad de copiarla. 
Los slices no son dueños de los datos, solo los referencian. Esto evita copias innecesarias y mejora la eficiencia. 

n main() {
    let mut a: [i32; 6] = [10, 20, 30, 40, 50, 60];
    println!("a: {a:?}");

    let s: &[i32] = &a[2..4];

    println!("s: {s:?}");
}


#### Cadenas de  texto 

Un &str es una referencia a una parte de una cadena de texto en Rust. 
✔ &str es como un puntero a una parte del texto, sin ser dueño de él.
✔ String es un buffer que puede modificar y crecer en el heap.
✔ Usa &str para eficiencia y String cuando necesites modificar texto.