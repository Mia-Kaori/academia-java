# Personal de una Academia

Aplicación Java con interfaz gráfica (Swing) y persistencia en fichero de texto para gestionar el personal (profesores y administrativos) de una academia, usando herencia y polimorfismo.

## Diseño

**Clase base `Persona`**: `dni`, `nombre`, `apellidos`, `edad`, `hombre` (booleano), `salario`.

**Subclases**
- `Profesor` — `asignatura`, `salario`, `horasLectivas`
- `Administrativo` — `departamento`, `salario`, `antiguedad`

Todos los objetos se almacenan en una única colección de tipo `Persona`, aprovechando herencia y polimorfismo para tratarlos y mostrarlos de forma unificada.

## Persistencia (`personal.txt`)

Cada línea representa una persona, indicando primero su tipo:

```
PROFESOR;dni;nombre;apellidos;edad;sexo;asignatura;salario;horasLectivas
ADMINISTRATIVO;dni;nombre;apellidos;edad;sexo;departamento;salario;antiguedad
```

Ejemplo:
```
PROFESOR;12345678A;Laura;Gómez Pérez;35;true;Programación;2150.5;18
ADMINISTRATIVO;87654321B;Carlos;Sánchez Ruiz;41;false;Secretaría;1800.0;12
```

Al iniciar, se carga el fichero en memoria; si no existe, se arranca con la lista vacía.

## Interfaz gráfica (Swing)

Dos ventanas, una por tipo de personal, cada una con los campos correspondientes y botones **Añadir** / **Eliminar**:
- Añadir: valida que todos los campos estén completos y añade la persona a la colección.
- Eliminar: valida que el DNI exista y elimina esa persona.

## Menú (consola)

1. Mostrar todo el personal
2. Mostrar solo profesores
3. Mostrar solo administrativos
4. Buscar por DNI
5. Guardar datos en archivo
6. Salir

## Validaciones

- Ningún campo vacío.
- Edad, salario, horas lectivas y antigüedad deben ser números positivos.
- DNI no puede repetirse.
- Los errores se muestran mediante la interfaz gráfica.

## Autor

**Kaori** — DAW 2025/2026  
[GitHub](https://github.com/Mia-Kaori)
