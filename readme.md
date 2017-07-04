# Practica01
### Alumno: Luis Rosales
##### Preguntas y Respuestas de la Práctica.

- **¿Qué comando utilizaste en el paso 11? ¿Por qué?**

  El comando **git reset** permite movilizar el **HEAD** a un **commit** en particular. Luego, se utiliza el *modificador* **--hard** para descartar los cambios en el **working area** ya que por defecto el comando **reset** no descarta los mismos. Por último, se usa el posicionador relativo **HEAD~1** que nos sitúa en el **commit** anterior del ramal.

    ```bash
    git reset --hard HEAD~1
    ```

- **¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?**

  Se usaron dos comandos, el primero:

  ```bash
  git reflog
  ```
  Este comando mostró una lista de **commits** por donde hemos pasado, de esa lista pudimos identificar que el **commit** con hash **54c4107** era el que estabamos buscando.

  Luego utilizamos el comando:

  ```bash
  git reset --hard <commit>
  ```

- **El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?**

  El **merge** realizado no causó **conflictos** debido a que el **ramal styled** estaba por delante del **ramal master** y porque el **ramal master** no tenía ningún **commit** adicional que tuviese modificaciones en las mismas líneas de los archivos modificados en los commits del **ramal styled**.  

- **El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?**
  Si, el **merge** causa conflicto ya que ambos **ramales** tienen **commits** con avances a partir de un **commit** en commún en las mismas líneas del archivo **git-nuestro.md**.

- **El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?**
  No, ya que no hubo avances en el **ramal master** después del **commit** en común. Por lo tanto, aunque las modificaciones en el archivo **git-nuestro.md** coinciden en las mismas líneas que las del fichero del **ramal master** estas sobreescriben al archivo en el **ramal master**.
- **¿Qué comando o comandos utilizaste en el paso 25?**
  ```bash
  git config alias.graph "log --pretty=oneline --decorate --graph"
  git graph
  ```
- **El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?**
  Si, ya que el archivo **git-nuestro.md** no tuvo modificaciones desde el commit en común con la rama **title**.  
- **¿Qué comando o comandos utilizaste en el paso 27?**
  ```bash
    git reset HEAD~1
    ```
- **¿Qué comando o comandos utilizaste en el paso 28?**
  ```bash
    git checkout -- git-nuestro.md
    ```
- **¿Qué comando o comandos utilizaste en el paso 29?**
  ```bash
    git branch -D title
    ```
- **¿Qué comando o comandos utilizaste en el paso 30?**
  ```bash
  git reflog
  git reset --hard <commit>
  ```
- **¿Qué comando o comandos usaste en el paso 32?**
  ```bash
  git log
  git reset --hard <commit>
  ```
- **¿Qué comando o comandos usaste en el punto 33?**
  ```bash
  git reflog
  git reset --hard <commit>
  ```
