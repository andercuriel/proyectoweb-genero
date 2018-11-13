# Cómo usar este repositorio para vuestro proyecto web

Accesos rápidos:

- :arrow_forward: [Empezar a trabajar en una nuevo borrador](#cada-vez-que-empezemos-con-nuevo-apartado)

Cada vez que nos reunamos:
- :arrow_forward: [Recoger acta](#actas) (si eres la persona encargada de Secretaría)
- :arrow_forward: [Realizar las autoevaluaciones](#autoevaluaciones)

## Descripción del contenido del repositorio 

Hay un directorio para cada unidad didáctica (o capítulo del proyecto), con la siguiente estructura:

```
0-nombreunidad
|_ actas-reuniones
|   |_ 2018MMDD.md
|   |_ ...
|_ evaluaciones
|   |_ MiApellidoMiNombre-2018MMDD.xlsx
|_ img
|   |_ ...   
|_ README.md
|_ roles.md
```

- En el directorio `actas-reuniones` recogeréis las actas de las reuniones que el equipo base realice fuera de clase. Podéis ver más información sobre la estructura y formato de estas actas en el [modelo de acta](1-estrategia/actas-reuniones/2018MMDD.md). Un acta por reunión.
- El directorio `evaluaciones` se recogen las autoevaluaciones que realizaréis al finalizar cada reunión presencial del equipo base.
- En el directorio `img` recogeréis las imágenes que vayáis a incorporar a vuestro contenido.
- El archivo `README.md` será el que contenga el contenido de la sección o capítulo en sí.
- El archivo `roles.md` debe recoger quién se encargará de cada tarea durante el tiempo en el que estéis trabajando en el borrador del plano correspondiente. 

## Flujo de trabajo para la redacción de los borradores de cada plano 

### Solamente la primera vez

Antes de empezar con el primer borrador, cada miembro del grupo deberá clonar el repositorio central recién creado a su ordenador (en la terminal, ubícate en el directorio donde guardes los repositorios de git y haz `git clone https://github.com/DeustpoPWEB2018/proyectoweb-VUESTROTEMA`). 
 
**Cada persona realizará modificaciones solamente sobre un branch en este repositorio, nunca directamente sobre el branch `master`.**

### Cada vez que empezemos con nuevo apartado

1. En la primera reunión del equipo, asignad los roles para el trabajo durante la elaboración de este borrador. :memo: La persona encargada de Secretaría deberá:
    - rellenar el documento `roles.md` de la unidad correspondiente con los nombres para cada rol
2. Realizad una división preliminar del archivo `README.md` correspondiente, y determinad a qué apartado va a contribuir cada persona. :memo: La persona encargada de Secretaría deberá:
    - recoger estos apartados en el documento `README.md`
    - publicar estos dos cambios en el repositorio central, mediante `git add .`, `git commit -m "Establecer roles y distribuir contenido"` y `git push origin master` (éste será el **único momento** en el que se publicará algo directamente sobre `master`)
2. Actualiza la copia personal de tu ordenador con las últimas modificaciones del repositorio central con `git pull origin master`
3. Crea un nuevo branch en tu ordenador, con tu nombre de usuario y el nombre del plano en el que vas a trabajar (por ejemplo, `mberasategi-estrategia`): `git checkout -b NOMBREDEBRANCH`
4. Trabaja en tu ordenador **sobre ese branch** (compruébalo con `git status` si hace falta), realizando las modificaciones correspondientes en el apartado que vayas a trabajar tú del documento `README.md`. Recuerda hacer commit para confirmar tus cambios, y push para enviarlos a tu copia personal en la nube.
5. Cuando hayas avanzado lo suficiente en tu trabajo como para compartirlo con tus compañeros, inicia un pull request:
    - accede mediante el navegador al repositorio central (`https://github.com/DeustoPWEB2018/proyectoweb-VUESTROTEMA`); clic en la pestaña **Pull requests**, y después clic en el botón **New pull request**
    - **base** debe ser `master`
    - **compare** debe ser tu branch de trabajo, `tunombre-plano`
    - Haz clic en **Create pull request**
    - Una vez hayas creado el pull request, en la barra lateral derecha, establece como **Reviewer** a la persona encargada del Control para este plano.
6. :memo: La persona encargada de Control revisa los pull requests para asegurar que las aportaciones de los compañeros cumplen los requerimientos. Solicita cambios cuando son necesarios y aprueba los pull requests cuando están preparados para incluirse en el borrador.
7. Cuando tu aportación personal esté lo suficientemente avanzada y finalizada como para incluirse en el borrador, y tenga el visto bueno de la persona de Control, :memo: la persona de Coordinación hará merge de tus cambios. 
    - Recuerda [actualizar tu fork personal](https://deustopweb2018.github.io/actualizar-fork) una vez tus cambios estén combinados con el repositorio central.
8. Cuando todas las aportaciones estén combinadas (merge) y el borrador esté listo para entregar, :memo: la persona encargada de Comunicación creará un release y lo entregará en ALUD. 
    - Acceder a `https://github.com/DeustoPWEB2018/proyectoweb-VUESTROTEMA/releases/new`:
    - **Tag version**: _1.0_ para el plano de Estrategia, _2.0_ para el de Alcance, y así sucesivamente
    - **Release title**: título del plano, por ejemplo, _Plano de Estrategia_
    - En **Describe this release** podéis incluir comentarios sobre el borrador, como áreas que consideráis que requieren más trabajo, o cualquier otra anotación que queráis añadir a vuestra entrega
    - Clic en **Publish this release**
    - Enviar la URL de la siguiente página a la entrega correspondiente en ALUD
9. Actualiza tu copia local (sigue [las instrucciones](https://deustopweb2018.github.io/actualizar-fork) si las necesitas) para tener en tu ordenador la versión que habéis entregado como borrador.

## Registro de las reuniones presenciales del equipo base

Podéis organizar el trabajo fuera del aula como os parezca más apropiado, pero necesitaréis varias reuniones presenciales del equipo base. **Cada vez que os reunáis**, tenéis que recoger un acta y realizar la autoevaluación.

### Actas

:memo: La persona encargada de Secretaría recogerá en un acta durante la reunión los temas tratados, las decisiones tomadas, las tareas a realizar etc. Estas actas hay que incorporarlas al repositorio del proyecto. Para esto, la persona encargada de Secretaría deberá:

1. Asegúrate de que estás en tu branch de trabajo (`TUNOMBRE-TEMA`) con `git status` (si no lo estás, cámbiate con `git checkout TUNOMBRE-TEMA`)
2. Genera un documento en el directorio `actas-reuniones` de la unidad correspondiente, siguiendo las indicaciones en [el acta de ejemplo](1-estrategia/actas-reuniones/2018MMDD.md). Redacta el acta en ese documento (utilizando Sublime) y guárdalo
3. Vuelve a la terminal y
    - añade el archivo recién creado: `git add .`
    - haz commit: `git commit -m "Redacción del acta 2018MMDD.md"`
    - publícalo: `git push origin TUNOMBRE-TEMA`

### Autoevaluaciones

Cada vez que os reunáis con vuestro equipo base, todos tendréis que realizar las **autoevaluaciones** para todos los participantes. Las autoevaluaciones se recogen en una carpeta llamada `evaluaciones` dentro del directorio correspondiente a cada unidad. 

Para esto, **al finalizar cada reunión**:

1. En la terminal, accede a tu carpeta del repositorio y asegúrate de que estás en tu branch de trabajo (`TUNOMBRE-TEMA`) con `git status` (si no lo estás, cámbiate con `git checkout TUNOMBRE-TEMA`)
2. Abre la carpeta en tu Explorador de archivos (Windows) o Finder (Mac). Accede al directorio `evaluaciones` de la unidad en la que estemos trabajando. Haz una copia del archivo Excel que tienes en esa carpeta (`MiApellidoMiNombre-2018MMDD.xlsx`) y cámbiale el nombre para que indique tu nombre y la fecha correcta, por ejemplo, `BerasategiMiren-20181002.xlsx`
3. Abre el archivo recién creado y rellena en esa hoja de cálculo tus evaluaciones (para ti y el resto de miembros que han trabajado contigo en el equipo), siguiendo las indicaciones que encontrarás en el mismo documento, y guárdalo 
4. En la terminal, guarda, confirma y envía a la nube los cambios realizados:
    ```
    git add .
    git commit -m "Evaluar reunión del día 20181002"
    git push origin TUNOMBRE-TEMA
    ```


<!-- Previous branch approach

Cada vez que os reunáis en equipos base, todos tendréis que realizar la autoevaluación propia y la de los demás miembros del equipo. Para esto, **al finalizar la reunión**:

1. En la terminal, accede a tu copia del repositorio del proyecto y cámbiate al branch `evaluaciones`: `git checkout evaluaciones`
2. Abre la carpeta en tu Explorador de archivos (Windows) o Finder (Mac). Verás que ahora, en lugar de mostrar los contenidos del proyecto, solamente tienes un directorio `evaluaciones`. Abre el archivo Excel que tienes en esa carpeta (`MiApellidoMiNombre-2018MMDD.xlsx`)
3. Rellena en esa hoja de cálculo tus evaluaciones (para ti y el resto de miembros) de la reunión correspondiente, siguiendo las indicaciones que encontrarás en el mismo documento. Guárdalo modificando el nombre como corresponde, por ejemplo, `BerasategiMiren-20181002.xlsx`
4. En la terminal, guarda, confirma y envía a tu copia personal en la nube los cambios realizados
    ```
    git add .
    git commit -m "Evaluar reunión del día 20181002"
    git push origin evaluaciones
    ```
5. Vuelve a tu branch de trabajo para seguir generando el contenido que te corresponde en este borrador: `git checkout TUNOMBRE-TEMA`

Estas autoevaluaciones no necesitan incorporarse al repositorio central, por lo que no es necesario que crees un pull request para esto. Las recogeré del repositorio personal de cada estudiante.

-->