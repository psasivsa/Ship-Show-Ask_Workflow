# Ship-Show-Ask_Workflow

> Ship / Show / Ask es una estrategia de ramas que combina la idea de crear Pull Request con la habilidad de seguir publicando cambios rápidamente.

![](images/Ship-Show-Ask.png)

El flujo de trabajo Ship / Show / Ask es un enfoque utilizado en el desarrollo de software para gestionar la entrega de código y la toma de decisiones en equipo. Este método se enfoca en tres posibles estados o acciones que un desarrollador puede tomar con su trabajo: enviar (ship), mostrar (show) o preguntar (ask). A continuación, se describe cada uno de estos estados y cómo se aplica en un flujo de trabajo típico.

### 1. **Ship (Enviar)**

**Objetivo**: Integrar código directamente en la rama principal sin necesidad de revisión, cuando el desarrollador está seguro de que los cambios son correctos y no necesitan revisión adicional.

**Acciones**:
- Realizar los cambios necesarios en el código.
- Asegurarse de que el código pasa todas las pruebas y cumple con los estándares de calidad.
- Integrar los cambios en la rama principal.

**Ejemplo**:
```sh
git checkout main
git pull origin main
# Realizar cambios en el código
git add .
git commit -m "Descripción de cambios seguros"
git push origin main
```

### 2. **Show (Mostrar)**

**Objetivo**: Compartir el trabajo con el equipo para obtener feedback, sin que los cambios se integren inmediatamente en la rama principal.

**Acciones**:
- Realizar cambios en una rama separada.
- Crear un pull request (PR) para compartir el trabajo con el equipo.
- Solicitar feedback específico, pero sin necesidad de una aprobación formal.

**Ejemplo**:
```sh
git checkout -b feature/nueva-funcionalidad
# Realizar cambios en el código
git add .
git commit -m "Descripción de cambios para revisión"
git push origin feature/nueva-funcionalidad
# Crear un pull request en GitHub
```

### 3. **Ask (Preguntar)**

**Objetivo**: Solicitar una revisión y aprobación formal de los cambios, cuando el desarrollador no está seguro o los cambios son significativos y necesitan una evaluación detallada.

**Acciones**:
- Realizar cambios en una rama separada.
- Crear un pull request (PR) solicitando una revisión completa y aprobación.
- Proveer una descripción detallada de los cambios y la razón detrás de ellos.
- Esperar a que el equipo revise y apruebe los cambios antes de integrarlos en la rama principal.

**Ejemplo**:
```sh
git checkout -b feature/cambio-importante
# Realizar cambios en el código
git add .
git commit -m "Descripción de cambios para aprobación"
git push origin feature/cambio-importante
# Crear un pull request en GitHub solicitando revisión
```

### Beneficios del flujo de trabajo Ship / Show / Ask

- **Flexibilidad**: Los desarrolladores pueden decidir la mejor manera de proceder con sus cambios dependiendo de su confianza y la naturaleza de los cambios.
- **Agilidad**: Permite una integración rápida de cambios menores y seguros, mientras que facilita la colaboración y revisión para cambios más grandes o inciertos.
- **Colaboración y Transparencia**: Promueve la comunicación y la transparencia en el equipo, facilitando el intercambio de ideas y la mejora continua del código.

### Desafíos del flujo de trabajo Ship / Show / Ask

- **Disciplina y Juicio**: Requiere que los desarrolladores tengan buen juicio para decidir cuándo enviar, mostrar o preguntar, evitando así potenciales problemas en la rama principal.
- **Gestión de Pull Requests**: Necesita una gestión eficaz de pull requests y revisiones para asegurar que los cambios mostrados o preguntados sean revisados de manera oportuna.
- **Cultura de Equipo**: Fomenta una cultura donde todos los miembros del equipo se sientan cómodos dando y recibiendo feedback constructivo.

### Ejemplo de Ciclo Completo en Ship / Show / Ask

1. **Evaluar los cambios necesarios**: Determinar si los cambios son seguros y menores (ship), si necesitan feedback (show) o si requieren una revisión formal (ask).
2. **Realizar los cambios**: Trabajar en una rama separada si es necesario.
3. **Tomar acción**:
   - **Ship**: Integrar directamente a la rama principal.
   - **Show**: Crear un pull request y solicitar feedback.
   - **Ask**: Crear un pull request y solicitar una revisión formal y aprobación.
4. **Revisión y feedback**: Colaborar con el equipo según sea necesario.
5. **Integración**: Una vez aprobados, integrar los cambios en la rama principal y desplegar si corresponde.

Este flujo de trabajo equilibra la necesidad de rapidez con la necesidad de calidad y colaboración en el desarrollo de software.
