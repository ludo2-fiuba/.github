# Profesores

### Crear semestre (no está en la propuesta)
Falta 

### ~Colaboración entre docentes~
Pedimos comisiones -> entro a una comision y pido permisos -> 
```json
{ 
	"rol": "Ayudante", 		
	"permisos": {"poner_notas": true, ...},
}
```

#### Acciones que puede realizar un docente:
- Corregir / poner notas
- Asignar correctores
- Generar QR de asistencia
- Crear un final
- Crear un parcial
- Ver docentes
- Agregar docente
- Editar rol de docente
- Etc

Falta: ~Nueva pantalla de editar de edición de permisos de lo que puede hacer cada rol~

### Asignación automática de correctores

Falta 
- Pantalla para editar los pesos de los docentes
- ~Endpoint para editar los pesos~
- Agregar botón "asignar correctores" y que se haga la call al endpoint que ya existe.
- Solo debería poder editar la nota el corrector asignado (debatible)

### Registro de asistencias (tanto alumnos como docentes)

- Pantalla para ver asistencias de una fecha 
- Pantalla para agregar una asistencia manual
- ~Lo que necesito del backend es tipo:~ -> Hecho
```json
[
    "fecha": "13/4/2024",
    "asistentes": ["41318038", "41..."]
]
```

### Modelado de los criterios de aprobación

Es un endpoint que {{baseUrl}}/api/semesters/is_passing?semester_id=2

Lo que tenemos:
- Cantidad de clases de un cuatrimestres
- Porcentaje de asistencia minimo
- Nota minima para las evaluaciones (para cada una de las evaluaciones) (está definido en la evaluación)
- Todas las evaluaciones que tienen notas se consideran obligatorias para aprobar
- Se consideran recuperatorios

Como modificamos esto desde el teacher:
- cantidad de clases totales: endpoint + front
- Porcentaje de asistencia minimo: endpoint + front 
- Nota minima para las evaluaciones: endpoint + front (edición de evaluaciones)

### Estadísticas
 - ~Alumnos: falta el front~
   - ~Promedio a lo largo del tiempo -> sí~
   - ~Comparación de mis promedios vs. global -> sí~
   - ~Comparación avance de carrera vs. global -> (deprecada por otra)~
   - ~mis top 3 materias (nota mucho mejor que el resto) -> sí~

 - Profesores (falta todo): 
   - correlación entre asistencias y aprobación -> (deprecada por otra)
   - tasa de retención: cuando abandonan más los alumnos la materia -> sí
   - promedio de notas de alumnos a lo largo del tiempo -> sí
   - porcentaje de asistencias durante el cuatrimestre -> sí

# Alumnos
### ~Registro de cursada  completa~
Done

### Notificaciones y avisos 
Falta testear

# Backoffice
### Registro de auditoría
Mostrar tabla en el backoffice

### ~Finales unificados~
~Discutir~
