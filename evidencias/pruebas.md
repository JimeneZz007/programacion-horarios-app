# Evidencias de pruebas del sistema

Este documento registra las pruebas realizadas al sistema de programación de horarios académicos, con el fin de validar restricciones duras, restricciones blandas y estabilidad del motor de generación.

## Prueba 1. Generación de horario válido

**Restricciones validadas:** RH-01 a RH-16 y RA-01 a RA-05.

**Escenario:** Se ejecuta el sistema con datos iniciales de docentes, aulas, cursos, grupos y franjas horarias.

**Resultado esperado:** El sistema genera un horario válido o un reporte de conflictos trazable.

**Resultado obtenido:** Pendiente de ejecución.

**Evidencia:** prueba_horario_valido.png

---

## Prueba 2. Docente con solapamiento horario

**Restricción validada:** RA-01 - Un docente no puede estar en dos sesiones simultáneas.

**Escenario:** Se intenta generar una asignación donde un mismo docente pueda quedar en dos clases en la misma franja.

**Resultado esperado:** El sistema bloquea la asignación y reporta conflicto.

**Resultado obtenido:** Pendiente de ejecución.

**Evidencia:** prueba_docente_solapado.png

---

## Prueba 3. Aula ocupada en la misma franja

**Restricción validada:** RA-02 - Un aula no puede tener dos sesiones simultáneas.

**Escenario:** Se fuerza la generación con aulas limitadas para validar que el motor no asigne dos grupos a la misma aula en el mismo horario.

**Resultado esperado:** El sistema bloquea la doble asignación del aula.

**Resultado obtenido:** Pendiente de ejecución.

**Evidencia:** prueba_aula_ocupada.png

---

## Prueba 4. Capacidad insuficiente del aula

**Restricción validada:** RH-09 - La capacidad del aula debe ser mayor o igual al tamaño del grupo.

**Escenario:** Se usa un grupo con más estudiantes que la capacidad del aula disponible.

**Resultado esperado:** El sistema rechaza aulas con capacidad insuficiente.

**Resultado obtenido:** Pendiente de ejecución.

**Evidencia:** prueba_capacidad_aula.png

---

## Prueba 5. Franja bloqueada de almuerzo

**Restricción validada:** RH-05 - No se programan sesiones en la franja 12:00-13:00.

**Escenario:** Se verifica que el motor excluya la franja marcada como bloqueada.

**Resultado esperado:** Ninguna clase queda asignada entre 12:00 y 13:00.

**Resultado obtenido:** Pendiente de ejecución.

**Evidencia:** prueba_franja_almuerzo.png
