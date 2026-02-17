# 📘 Fundamentos de Programación Orientada a Objetos (POO) en Java
Aplicado al Desarrollo en Android Studio

---

# 1️⃣ ¿Qué es Java?

Java es un lenguaje de programación orientado a objetos.  
Esto significa que el código se organiza en clases que representan objetos del mundo real.

En Android Studio utilizamos Java para:

- Crear pantallas (Activities)
- Controlar botones
- Manipular datos
- Conectar con bases de datos (SQLite)

👉 Si entendemos POO, entenderemos Android.

---

# 2️⃣ Clase

Una clase es un molde o plano.

```java
public class Servicio {
}
```
🔎 Explicación sencilla:

Aquí estamos definiendo el molde llamado Servicio.
Aún no existe ningún servicio real en memoria.

# 3️⃣ Objeto

Un objeto es una instancia de una clase.
```java
Servicio s1 = new Servicio();
```
🔎 Explicación sencilla:
- Servicio → tipo de dato.
- s1 → nombre del objeto.
- new Servicio() → crea el objeto en memoria.
En NovaServiciosApp:
- Clase → Servicio
- Objeto → Cada mantenimiento registrado.

# 4️⃣ Atributos

Los atributos describen el estado del objeto.
```java
public class Servicio {

    private String nombre;
    private String descripcion;
    private boolean activo;

}

```
🔎 Explicación sencilla:
- private protege el dato.
- nombre y descripcion almacenan información.
- activo indica si el servicio está disponible.
En bases de datos profesionales no se elimina un registro, se cambia su estado.

# 5️⃣ Encapsulamiento

Encapsular significa proteger los datos y permitir acceso controlado.
```java
private String nombre;

public void setNombre(String nombre) {
    this.nombre = nombre;
}

public String getNombre() {
    return nombre;
}
```
🔎 Explicación sencilla:
- private impide acceso directo.
- set permite modificar.
- get permite obtener el valor.
- this.nombre se refiere al atributo de la clase.
Encapsular evita errores y mejora seguridad del código.

# 6️⃣ Constructor

El constructor inicializa el objeto.
```java
public Servicio(String nombre, String descripcion) {
    this.nombre = nombre;
    this.descripcion = descripcion;
    this.activo = true;
}

```
🔎 Explicación sencilla:
Cuando escribimos:
```java
Servicio s1 = new Servicio("Mantenimiento", "Cambio de piezas");
```
# 7️⃣ Métodos

Los métodos representan comportamientos del objeto.
```java
public void mostrarServicio() {
    System.out.println(nombre + " - " + descripcion);
}
```
🔎 Explicación sencilla:
Este método muestra información del servicio.

En Android usamos métodos como:
```java
button.setOnClickListener(...)
textView.setText(...)
```
Todo objeto tiene comportamientos.

# 8️⃣ Abstracción

La abstracción significa enfocarnos en lo esencial y ocultar detalles internos.

Ejemplo simple:
```java
public void guardarServicio(Servicio servicio) {
    validar(servicio);
    insertarEnSQLite(servicio);
    mostrarConfirmacion();
}
```
🔎 Explicación sencilla:
Desde afuera solo vemos guardarServicio().
No necesitamos saber cómo funciona internamente.

Eso es abstracción: ocultar la complejidad.
```java
public abstract class ServicioBase {

    protected String nombre;

    public ServicioBase(String nombre) {
        this.nombre = nombre;
    }

    public abstract void ejecutar();
}

```
🔎 Explicación sencilla:
- abstract indica que no se puede crear directamente un objeto de esta clase.
- Obliga a que las clases hijas implementen ejecutar().

# 9️⃣ Herencia

Permite que una clase herede características de otra.
```java
public class Persona {
    protected String nombre;
}

public class Tecnico extends Persona {
    private String especialidad;
}
```
🔎 Explicación sencilla:

- extends significa que Tecnico hereda de Persona.
- Tecnico tendrá nombre + especialidad.
Permite reutilizar código.

🔟 Polimorfismo

Significa que un mismo método puede comportarse de distintas formas.
```java
public class ServicioNormal extends ServicioBase {

    public ServicioNormal(String nombre) {
        super(nombre);
    }

    @Override
    public void ejecutar() {
        System.out.println("Ejecutando servicio normal");
    }
}

public class ServicioUrgente extends ServicioBase {

    public ServicioUrgente(String nombre) {
        super(nombre);
    }

    @Override
    public void ejecutar() {
        System.out.println("Ejecutando servicio urgente");
    }
}
```

🔎 Explicación sencilla:

Ambos tienen el método ejecutar(), pero hacen cosas diferentes.
Eso es polimorfismo.

# 1️⃣1️⃣ Relación con Android Studio

En Android:
- MainActivity es una clase.
- Button es un objeto.
- SQLiteDatabase es un objeto.
- Cada registro será convertido en un objeto.

Cuando implementemos CRUD:
- Usuario llena formulario.
- Creamos objeto Servicio.
- Guardamos en SQLite.
- Mostramos en RecyclerView.

Eso es POO aplicada a una app real.
