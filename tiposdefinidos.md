## Rust admite estructuras(struc) personalizadas. 

struct Person {
    name: String,
    age: u8,
}

fn describe(person: &Person) {
    println!("{} tiene {} años", person.name, person.age);
}

fn main() {
    let mut peter = Person { name: String::from("Peter"), age: 27 };
    describe(&peter);

    peter.age = 28;
    describe(&peter);

    let name = String::from("Avery");
    let age = 39;
    let avery = Person { name, age };
    describe(&avery);

    let jackie = Person { name: String::from("Jackie"), ..avery };
    describe(&jackie);
}



## estrcuturas de tuplas 


##3 Enumeraciones
La palabra clave enum permite crear un tipo que tiene diferentes variantes

#[derive(Debug)]
enum Direction {
    Left,
    Right,
}

#[derive(Debug)]
enum PlayerMove {
    Pass,                        // Variante simple
    Run(Direction),              // Variante de tupla
    Teleport { x: u32, y: u32 }, // Variante de struct
}

fn main() {
    let m: PlayerMove = PlayerMove::Run(Direction::Left);
    println!("En este turno: {:?}", m);
}