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

