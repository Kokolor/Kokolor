# Liste de langages de programmation compilés pour débutants

Voici une liste de 20 langages de programmation compilés, adaptés aux débutants et utiles pour le développement de systèmes ou d'OS, avec des exemples de code simples incluant des variables, des structs, et des fonctions.

## 1. C

Le langage C est l'un des langages de programmation les plus anciens et les plus utilisés, particulièrement pour le développement de systèmes et d'OS.

Exemple de code :

    #include <stdio.h>
    #include <string.h>

    typedef struct {
        int id;
        char name[50];
    } Person;

    void greet(Person p) {
        printf("Bonjour, %s!\n", p.name);
    }

    int main() {
        Person person;
        person.id = 1;
        strcpy(person.name, "Alice");
        greet(person);
        return 0;
    }

## 2. C++

Le C++ est une extension du C qui ajoute la programmation orientée objet, très utilisé pour le développement de logiciels performants.

Exemple de code :

    #include <iostream>
    #include <string>

    struct Person {
        int id;
        std::string name;
    };

    void greet(const Person& p) {
        std::cout << "Bonjour, " << p.name << "!" << std::endl;
    }

    int main() {
        Person person;
        person.id = 1;
        person.name = "Bob";
        greet(person);
        return 0;
    }

## 3. Rust

Rust est un langage moderne axé sur la sécurité et la performance, souvent utilisé pour le développement de systèmes.

Exemple de code :

    struct Person {
        id: u32,
        name: String,
    }

    fn greet(p: &Person) {
        println!("Bonjour, {}!", p.name);
    }

    fn main() {
        let person = Person { id: 1, name: String::from("Charlie") };
        greet(&person);
    }

## 4. Go

Go, ou Golang, est un langage conçu par Google, apprécié pour sa simplicité et sa performance, adapté au développement de systèmes et de serveurs.

Exemple de code :

    package main

    import "fmt"

    type Person struct {
        ID   int
        Name string
    }

    func greet(p Person) {
        fmt.Printf("Bonjour, %s!\n", p.Name)
    }

    func main() {
        person := Person{ID: 1, Name: "Diana"}
        greet(person)
    }

## 5. D

Le langage D combine la performance du C++ avec une syntaxe moderne et des fonctionnalités de haut niveau.

Exemple de code :

    import std.stdio;

    struct Person {
        int id;
        string name;
    }

    void greet(Person p) {
        writeln("Bonjour, ", p.name, "!");
    }

    void main() {
        Person person;
        person.id = 1;
        person.name = "Émile";
        greet(person);
    }

## 6. Zig

Zig est un langage de programmation bas niveau axé sur la robustesse et la performance, souvent utilisé pour le développement de systèmes.

Exemple de code :

    const std = @import("std");

    pub const Person = struct {
        id: i32,
        name: []const u8,
    };

    pub fn greet(p: Person) void {
        std.debug.print("Bonjour, {}!\n", .{p.name});
    }

    pub fn main() void {
        var person = Person{ .id = 1, .name = "Fiona" };
        greet(person);
    }

## 7. Nim

Nim est un langage de programmation efficace et expressif, avec une syntaxe similaire à Python, mais compilé en code natif.

Exemple de code :

    type
      Person = object
        id: int
        name: string

    proc greet(p: Person) =
      echo "Bonjour, ", p.name, "!"

    proc main() =
      let person = Person(id: 1, name: "George")
      greet(person)

## 8. Pascal

Pascal est un langage de programmation structuré, souvent utilisé dans l'enseignement et pour le développement de logiciels.

Exemple de code :

    program Greeting;

    type
      Person = record
        id: Integer;
        name: String[50];
      end;

    procedure Greet(p: Person);
    begin
      writeln('Bonjour, ', p.name, '!');
    end;

    var
      person: Person;

    begin
      person.id := 1;
      person.name := 'Hélène';
      Greet(person);
    end.

## 9. Ada

Ada est un langage de programmation fortement typé, utilisé dans les systèmes embarqués et les applications critiques.

Exemple de code :

    with Ada.Text_IO; use Ada.Text_IO;

    procedure Greeting is
      type Person is record
        ID : Integer;
        Name : String(1..50);
      end record;

      procedure Greet(P : Person) is
      begin
        Put_Line("Bonjour, " & P.Name & "!");
      end Greet;

      Person1 : Person := (ID => 1, Name => "Igor");
    begin
      Greet(Person1);
    end Greeting;

## 10. Swift

Swift est un langage de programmation développé par Apple, utilisé principalement pour le développement d'applications iOS et macOS, mais également pour le développement système.

Exemple de code :

    struct Person {
        var id: Int
        var name: String
    }

    func greet(_ p: Person) {
        print("Bonjour, \(p.name)!")
    }

    func main() {
        let person = Person(id: 1, name: "Julia")
        greet(person)
    }

## 11. Kotlin/Native

Kotlin/Native permet de compiler le langage Kotlin en code natif, adapté au développement de systèmes.

Exemple de code :

    data class Person(val id: Int, val name: String)

    fun greet(p: Person) {
        println("Bonjour, ${p.name}!")
    }

    fun main() {
        val person = Person(1, "Kevin")
        greet(person)
    }

## 12. Haskell

Haskell est un langage fonctionnel pur, compilé avec GHC, utilisé dans des applications nécessitant une grande fiabilité.

Exemple de code :

    data Person = Person { id :: Int, name :: String }

    greet :: Person -> IO ()
    greet p = putStrLn ("Bonjour, " ++ name p ++ "!")

    main :: IO ()
    main = do
        let person = Person { id = 1, name = "Laura" }
        greet person

## 13. OCaml

OCaml est un langage de programmation fonctionnel avec des capacités impératives et orientées objet, utilisé dans la recherche et l'industrie.

Exemple de code :

    type person = {
      id : int;
      name : string;
    }

    let greet p =
      Printf.printf "Bonjour, %s!\n" p.name

    let () =
      let person = { id = 1; name = "Marc" } in
      greet person

## 14. Fortran

Fortran est un langage de programmation principalement utilisé pour les calculs scientifiques et l'ingénierie.

Exemple de code :

    program greeting
        type :: Person
            integer :: id
            character(len=50) :: name
        end type Person

        procedure :: greet

        type(Person) :: person

    contains

        subroutine greet(p)
            type(Person), intent(in) :: p
            print *, 'Bonjour, ', trim(p%name), '!'
        end subroutine greet

    end program greeting

## 15. Crystal

Crystal est un langage de programmation qui combine la performance du C avec une syntaxe proche de Ruby.

Exemple de code :

    struct Person
      property id : Int32
      property name : String

      def initialize(@id, @name)
      end
    end

    def greet(p : Person)
      puts "Bonjour, #{p.name}!"
    end

    person = Person.new(1, "Nina")
    greet(person)

## 16. Julia

Julia est un langage de programmation haut niveau et dynamique, performant, utilisé principalement pour les calculs scientifiques.

Exemple de code :

    struct Person
        id::Int
        name::String
    end

    function greet(p::Person)
        println("Bonjour, ", p.name, "!")
    end

    function main()
        person = Person(1, "Oscar")
        greet(person)
    end

    main()

## 17. V

V est un langage de programmation simple, rapide et sécurisé, conçu pour la facilité d'utilisation et la performance.

Exemple de code :

    struct Person {
        id int
        name string
    }

    fn greet(p Person) {
        println('Bonjour, $p.name!')
    }

    fn main() {
        person := Person{
            id: 1
            name: 'Paul'
        }
        greet(person)
    }

## 18. Modula-2

Modula-2 est un langage de programmation conçu pour la programmation système et l'enseignement de la programmation structurée.

Exemple de code :

    MODULE Greeting;

    TYPE
      Person = RECORD
        id: INTEGER;
        name: ARRAY [1..50] OF CHAR;
      END;

    PROCEDURE Greet(p: Person);
    BEGIN
      WriteString("Bonjour, ");
      WriteString(p.name);
      WriteLn("!");
    END Greet;

    VAR
      person: Person;
    BEGIN
      person.id := 1;
      person.name := "Quentin";
      Greet(person);
    END Greeting.

## 19. Scala (Scala Native)

Scala peut être compilé en code natif avec Scala Native, permettant le développement de systèmes performants.

Exemple de code :

    case class Person(id: Int, name: String)

    def greet(p: Person): Unit = {
      println(s"Bonjour, ${p.name}!")
    }

    @main def main(): Unit = {
      val person = Person(1, "Renee")
      greet(person)
    }

## 20. Delphi (Object Pascal)

Delphi est une version moderne de Pascal, utilisée principalement pour le développement d'applications Windows, mais également pour le développement système.

Exemple de code :

    program Greeting;

    type
      TPerson = record
        ID: Integer;
        Name: string[50];
      end;

    procedure Greet(p: TPerson);
    begin
      Writeln('Bonjour, ', p.Name, '!');
    end;

    var
      person: TPerson;

    begin

## 20. Orys (Mon langage)

Orys sera un langage compilé, performant, mais très mal foutu.

Exemple de code :

    import [orys::std] as std;
    
    fn add(x: i32, y: i16): i32 -> {
       return x + y.cast(i32);
    }
    
    asm[asm::nasm, "
      global _start
             call main
    "];
    
    fn main(): i32 -> {
       def a: i32 = 14;
       def b: i16 = 47;
    
       def c: i32 = add(a, b.cast(i32));
    
       return c;
    }

      Greet(person);
    end.
