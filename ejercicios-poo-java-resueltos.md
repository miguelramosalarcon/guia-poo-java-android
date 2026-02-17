# 📝 Ejercicios Resueltos – Programación Orientada a Objetos en Java


## ✅ Ejercicio 1 – Clase Alumno

📌 Enunciado

Crear una clase Alumno con:

- nombre
- nota
- activo
- método que indique si aprueba

---

### ✔ Solución

```java
public class Alumno {

    private String nombre;
    private double nota;
    private boolean activo;

    public Alumno(String nombre, double nota) {
        this.nombre = nombre;
        this.nota = nota;
        this.activo = true;
    }

    public boolean aprueba() {
        return nota >= 13;
    }

    public void mostrarInformacion() {
        System.out.println("Nombre: " + nombre);
        System.out.println("Nota: " + nota);
        System.out.println("Activo: " + activo);
    }
}
```
🔎 Explicación
- Se usa encapsulamiento (private).
- El constructor inicializa los valores.
- aprueba() devuelve un boolean.
- mostrarInformacion() imprime datos del objeto.

## ✅ Ejercicio 2 – Clase Tecnico
📌 Enunciado

Crear una clase Tecnico con:
- nombre (String)
- especialidad (String)
- disponible (boolean)

Debe incluir:
- Constructor
- Método mostrarInformacion()

```java
public class Tecnico {

    private String nombre;
    private String especialidad;
    private boolean disponible;

    public Tecnico(String nombre, String especialidad) {
        this.nombre = nombre;
        this.especialidad = especialidad;
        this.disponible = true;
    }

    public void mostrarInformacion() {
        System.out.println("Nombre: " + nombre);
        System.out.println("Especialidad: " + especialidad);
        System.out.println("Disponible: " + disponible);
    }
}
```

🔎 Explicación
- Se encapsulan los atributos.
- El constructor inicializa el técnico como disponible.
- mostrarInformacion() permite visualizar el estado del objeto.
- Este modelo podría utilizarse en NovaServiciosApp para asignar técnicos a servicios.

## 💻 Cómo ejecutar los ejercicios online

Para practicar sin instalar software adicional, puedes usar el compilador:

🔗 https://www.onlinegdb.com/online_java_compiler#

### ⚠ Reglas importantes:

- Solo una clase puede ser `public`.
- La clase principal debe llamarse `Main`.
- Las demás clases deben declararse sin `public`.
- Todo el código debe pegarse en un solo archivo.

Esto es solo para práctica.  
En Android Studio, cada clase se crea en su propio archivo.

