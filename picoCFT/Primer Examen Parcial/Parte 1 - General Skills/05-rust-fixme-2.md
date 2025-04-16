## Rust fixme 2
The Rust saga continues? I ask you, can I borrow that, pleeeeeaaaasseeeee?Download the Rust code [here](https://challenge-files.picoctf.net/c_verbal_sleep/babfbee79718a6363826ba86300173ffde6d81577e9dd07d4130c53a7eecf6c3/fixme2.tar.gz).

#### Hints:
1. https://doc.rust-lang.org/book/ch04-02-references-and-borrowing.html


## Solución:
```

1. Descargar archivo https://challenge-files.picoctf.net/c_verbal_sleep/babfbee79718a6363826ba86300173ffde6d81577e9dd07d4130c53a7eecf6c3/fixme2.tar.gz

brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/part1/rusfix2$ wget https://challenge-files.picoctf.net/c_verbal_sleep/babfbee79718a6363826ba86300173ffde6d81577e9dd07d4130c53a7eecf6c3/fixme2.tar.gz
--2025-04-15 16:21:11--  https://challenge-files.picoctf.net/c_verbal_sleep/babfbee79718a6363826ba86300173ffde6d81577e9dd07d4130c53a7eecf6c3/fixme2.tar.gz
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 18.238.132.88, 18.238.132.26, 18.238.132.49, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|18.238.132.88|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1585 (1.5K) [application/octet-stream]
Saving to: ‘fixme2.tar.gz’

fixme2.tar.gz                 100%[=================================================>]   1.55K  --.-KB/s    in 0s

2025-04-15 16:21:12 (26.1 MB/s) - ‘fixme2.tar.gz’ saved [1585/1585]

brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/part1/rusfix2$






2.  Descomprimir con :  tar -xvzf fixme2.tar.gz
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/part1/rusfix2$ tar -xvzf fixme2.tar.gz
fixme2/
fixme2/Cargo.toml
fixme2/Cargo.lock
fixme2/src/
fixme2/src/main.rs


3. Checar: ls
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/part1/rusfix2$ ls
fixme2  fixme2.tar.gz


4. Entrar a la carpeta del paso 3: cd fixme2
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/part1/rusfix2$ cd fixme2
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/part1/rusfix2/fixme2$


5. Ejecutar cargo build:  'cargo build' y aparecera un error en el codigo

brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/part1/rusfix2/fixme2$ cargo build
   Compiling crossbeam-utils v0.8.20
   Compiling rayon-core v1.12.1
   Compiling either v1.13.0
   Compiling crossbeam-epoch v0.9.18
   Compiling crossbeam-deque v0.8.5
   Compiling rayon v1.10.0
   Compiling xor_cryptor v1.2.3
   Compiling rust_proj v0.1.0 (/home/brisguz/SegPrac/pico/part1/rusfix2/fixme2)
error[E0596]: cannot borrow `*borrowed_string` as mutable, as it is behind a `&` reference





6. Entrar a cd src
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/part1/rusfix2/fixme2$ cd src
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/part1/rusfix2/fixme2/src$ ls
main.rs



7. Cambiar código mal, entrar con:  sudo nano main.rs
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/part1/rusfix2/fixme2/src$ sudo nano main.rs
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/part1/rusfix2/fixme2/src$



Código corregido:

//
use xor_cryptor::XORCryptor;

fn decrypt(encrypted_buffer:Vec<u8>, borrowed_string: &mut String){ // How do we pass values to a function that we want>
    // Key for decryption
    let key = String::from("CSUCKS");

    // Editing our borrowed value
    borrowed_string.push_str("PARTY FOUL! Here is your flag: ");

    // Create decrpytion object
    let res = XORCryptor::new(&key);
    if res.is_err() {
        return; // How do we return in rust?
    }
    let xrc = res.unwrap();

    // Decrypt flag and print it out
    let decrypted_buffer = xrc.decrypt_vec(encrypted_buffer);
    borrowed_string.push_str(&String::from_utf8_lossy(&decrypted_buffer));
    println!("{}", borrowed_string);
}


fn main() {
    // Encrypted flag values
    let hex_values = ["41", "30", "20", "63", "4a", "45", "54", "76", "01", "1c", "7e", "59", "63", "e1", "61", "25", ">
    // Convert the hexadecimal strings to bytes and collect them into a vector
    let encrypted_buffer: Vec<u8> = hex_values.iter()
        .map(|&hex| u8::from_str_radix(hex, 16).unwrap())
        .collect();

    let mut party_foul = String::from("Using memory unsafe languages is a: "); // Is this variable changeable?
    decrypt(encrypted_buffer, &mut party_foul); // Is this the correct way to pass a value to a function so that it can>}










8. Ahora correrlo con: cargo run
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/part1/rusfix2/fixme2/src$ cargo run
   Compiling rust_proj v0.1.0 (/home/brisguz/SegPrac/pico/part1/rusfix2/fixme2)
    Finished dev [unoptimized + debuginfo] target(s) in 4.16s
     Running `/home/brisguz/SegPrac/pico/part1/rusfix2/fixme2/target/debug/rust_proj`
Using memory unsafe languages is a: PARTY FOUL! Here is your flag: picoCTF{4r3_y0u_h4v1n5_fun_y31?}
brisguz@DESKTOP-8V24E1B:~/SegPrac/pico/part1/rusfix2/fixme2/src$

```


#### Bandera
```
picoCTF{4r3_y0u_h4v1n5_fun_y31?}
```