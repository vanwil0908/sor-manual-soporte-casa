

- **Alumno:** Vanessa Wilczek
- **Bloque:** B0 — Prerrequisitos
- **Fase / ejercicio:** Fase 0.8
- **Fecha de inicio:** 23/10/2026
- **Fecha de entrega:** 23/10/2026

---

## 🎯 Qué se pedía

(Dos o tres líneas con tus palabras: qué había que conseguir.)
Debíamos de empezar una bóveda de 0 y crear sus carpetas respectivas, luego teníamos que hacer manuales y 3 commits, y finalmente cambiar de main a nuestro primer commit.
## ⌨️ Comandos y pasos importantes

- `comando` — para qué sirve.
git --version = Muestra la versión de Git instalada; no instala ni actualiza nada.

git config --global user.name = Muestra el nombre global que Git usará como autor; debe ser el tuyo.

git config --global user.email = Muestra el correo global del autor de los commits; debe ser el tuyo.

ls -l ~/.ssh/id_ed25519 ~/.ssh/id_ed25519.pub = Comprueba que existen los archivos de clave privada y pública; no muestra su contenido.

ssh -T git@github.com = Prueba la autenticación con GitHub. El saludo debe identificar tu usuario; no abre una shell ni sube archivos.

pwd = Muestra la carpeta actual. Contrasta su ruta con la indicada en este paso antes de seguir.

git init = Crea el repositorio local en la carpeta que acabas de comprobar.

git branch -M main = Establece main como nombre de la rama actual.

git status = Muestra la rama main, sin commits todavía, y los archivos iniciales sin seguimiento.

git remote add origin git@github.com:TU-USUARIO/sor-web-prestamo-portatiles-casa.git = Registra origin con la dirección SSH de tu repositorio vacío; todavía no envía archivos.

git remote -v = Muestra las direcciones de lectura y envío de los remotos; origin debe ser el de este proyecto.

git add . = Prepara todos los archivos no ignorados que hay bajo esta 
carpeta: en esta primera entrega, gitignore, bitácora y portada.

git commit -m = Guarda localmente una versión con los cambios preparados y el mensaje indicado.

git push -u origin main =  Sube main por primera vez a origin y configura su seguimiento para las siguientes subidas.

git diff -- = Compara la portada del disco con el índice: antes de prepararla verás la frase anterior con - y la nueva con +. No compara dos archivos diferentes.

git add web/index.html = Prepara únicamente el contenido actual del archivo indicado para el próximo commit; no sube nada.

git push = Envía los commits pendientes al remoto ya configurado. Comprueba que termina sin errores.

git status --short --untracked-files=all = Muestra el estado abreviado y enumera cada archivo sin seguimiento por su ruta completa, en lugar de agruparlos por carpetas. --short abrevia la salida; --untracked-
files=all despliega los nuevos.

git check-ignore -v web/videos/revision-01.mp4 web/videos/revision-02.mp4 = Indica, para cada ruta, el archivo de reglas, su número de línea y el patrón que la ignora. `-v` pide esos detalles.

git status --short --untracked-files=all = Muestra de nuevo qué está preparado y qué sigue sin preparar. Observa el archivo recién seleccionado.

git diff --cached --stat = Resume los cambios preparados en el índice: nombres y estadísticas. --cached selecciona lo preparado; --stat pide un resumen, no todas las líneas.

git log --oneline = Enumera los commits con código abreviado y mensaje, del más reciente al más antiguo. 

git switch --detach CODIGO_PRIMER_COMMIT = Cambia los archivos seguidos a la versión del commit indicado. --detach permite consultar ese commit sin situarte en una rama.

git switch main = Vuelve a la rama main, recuperando sus archivos seguidos.
## 🛠️ Qué he hecho

(Los pasos que has seguido. No copies el enunciado: cuenta lo que hiciste tú.)

Yo empecé primero leyendo el PDF, seguí todos los pasos 1 por 1, primero comprobé que tenía Git disponible, que fuera mi identidad y que mi SSH funcionara. A continuación empecé con la bóveda, cree sus carpetas correspondidas y las notas que se necesitabas dentro de las carpetas, en una de ellas hice un .gitignore en git bash, para que no me aparezcan archivos con ciertas extensiones. Luego, hice el primer manual de soporte y un equipo sin conexión que se pide y luego me asegure de hacer la ruta y el primer git init. Proseguí con hacer el repositorio en Github, asegurándome de que copie el SSH público. A continuación hice el primer commit y push de esa página, y luego en el siguiente apartado me pidieron cambiarla y tuve que volver a hacer un commit y push, luego tuve que crear impresora que no imprime y equipo sin sonido y cambiar una cosa del README.md, y comprobar que con un git status cambie algo. Después tuve que comprobar porque los videos quedaban fuera, una vez hice eso prepare los manuales que cambie, revisando la selección completa, lo guarde y lo subí, me asegure de que la entrega fue terminada. Finalmente se me pidió que localizase la primera entrega y entrara en ella para comprobar que los archivos desaparecían y luego de volver al main, los archivos volvían.

## 🚩 Qué me ha fallado y cómo lo he resuelto

(El mensaje de error LITERAL y qué hiciste. Si no falló nada, escribe "nada"
— pero piénsalo dos veces antes.)
Me daba fallos al escribir un add ... simplemente por que escribí mal la ruta, me di cuenta más tarde.
También al cambiar de main al primer commit, me dio un fallo diciendo que no podía volver a main, me daban fallos las carpetas y tuve que hacer un add en los archivos y ya me dejo cambiar a main.
## 🤔 Respuestas a las preguntas

1. ¿Por qué Git se inicializa solo en 01_Proyecto y la grabación queda fuera?
Si haces git init en la raíz de la bóveda, estarías mezclando absolutamente todo en un único repositorio. Al hacerlo dentro de 01_Proyecto, limitas el control de versiones exclusivamente a esa carpeta.

2. ¿Qué muestran status y diff antes de preparar la corrección del procedimiento? Cita la instrucción anterior y la nueva.
Al ser un archivo nuevo y no rastreado (untracked), git status lo detecta en el directorio, pero git diff solo compara diferencias entre archivos que ya forman parte del seguimiento (tracked) del repositorio.

3. ¿Por qué un archivo nuevo aparece en status pero no en el diff de README.md?
Porque al ser un archivo nuevo y no rastreado, git status lo detecta en la carpeta, pero git diff README.md solo compara los cambios dentro de un archivo que ya forma parte del seguimiento del repositorio, ignorando los ficheros que aún no han sido añadidos por primera vez.

4. ¿Qué preparas con cada add y qué compruebas con diff --cached antes del commit?
Con cada add preparas y seleccionas los cambios pasándolos al área de preparación staging area y con git diff cached compruebas exactamente qué modificaciones han quedado listas y guardadas temporalmente para ser consolidadas en el próximo commit.

5. ¿Qué demuestra check-ignore y qué comprobaste además para saber que los clips existen?
Check ignore demuestra qué regla de exclusión descarta un archivo determinado y para saber que los clips existen se verificó su presencia física directamente en la carpeta del ordenador.

6. ¿Qué diferencias concretas observaste en el manual del primer commit y qué recuperaste al volver a main?
En el primer commit el manual estaba incompleto o en su versión inicial sin los cambios posteriores y al volver a main recuperaste la versión más actualizada y final del documento junto con todos los archivos creados en entregas posteriores.

7. ¿Qué aporta un historial cuando dos técnicos necesitan conocer el procedimiento vigente?
El historial aporta una fuente única de verdad que permite a ambos técnicos verificar los cambios realizados a lo largo del tiempo, consultar cuándo y por qué se actualizó una norma y asegurarse de estar aplicando exactamente la versión oficial vigente sin confusión ni datos obsoletos.

8. ¿Por qué commit y push son acciones diferentes y qué miraste en GitHub?
Commit guarda los cambios localmente en tu ordenador, mientras que push los sube al repositorio remoto en internet, y en GitHub miraste que todo se hubiera publicado correctamente online.

9. ¿Qué pasos repetirías para corregir otra instrucción y cuáles se hicieron una sola vez?
Para corregir otra instrucción repetirías editar el archivo, prepararlo con add y guardarlo con commit, mientras que la configuración inicial de git, el git init y enlazar el repositorio remoto con GitHub se hicieron una sola vez.
## 🔗 Enlaces

- **Vídeo de esta fase:** https://youtu.be/SeXHQjPlBOw
- **Playlist:** https://www.youtube.com/playlist?list=PLDqLfKHKutRs

## 💭 Dudas / a repasar

- La verdad todo me ha quedado claro, solo tengo que tener cuidado con las extensiones y con como escribo.