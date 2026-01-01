# IA Avanzada Simple Navigation

## Modificaciones

### Agente nuevo

Se añade un GameObject 3D tipo Sphere llamado **Student** con los siguientes componentes:

- **Nav Mesh Agent**
  - Tipo de agente: Humanoid for Navigation Sample
  - Resto de valores iguales que el GameObject llamado **Agent** excepto:
    - Obstacle Avoidance:
      - Radius: Se añade el valor 3 para evitar que choque con otros agentes.
    - Path Finding:
      - Area Mask: Solo podrá transitar por Walkable y Jump
- Script **Simple Navigation Agent Controller**

### Obstáculo

Se añade un GameObject 3D tipo Cubre llamado **Wall-not-student** dentro de la jerarquía **Level**.

La función de este obstáculo es que los agentes tipo **Humanoid** puedan atravesarlo pero los agentes tipo **Humanoid for Navigation Sample** lo tengan que bordear

Una vez añadido el obsttáculo a la jerarquía de **Level**, se modifica el componente **Nav Mesh Surface** que afecta a los agentes tipo **Humanoid for Navigation Sample** pulsando el botón **Bake**.

Para diferenciar este obstáculo se añade el material **Wall** al igual que el resto de obstáculos.