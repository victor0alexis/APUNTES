# *Notas GIT* 

## ⚠️ **Configuraciones Globales**
- Cambio nombre usuario (local)
> **git config --global user.name <**nuevo_nombre**>**
- Cambio email usuario (local)
> **git config --global user.email <**nuevo_email**>**
- Maximo 5 caracteres para identificacion de **commits** (necesario)
> **git config --global core.abbrev 5**



## ✅ **Rutas**
|   codigo       | Descripción               
|------------|---------------------------|
| **cd c:**   | Entrar Disco Duro             
| **cd Git** | Avanzar entre carpetas                  
| **cd ..**     | Retroceder en la ruta|    

## 🗂️ **Archivos**

1. ### 🔍 **Vizualizacion Contenido**

|   codigo       | Descripción               
|------------|---------------------------|
| **ls**    | Mostrar archivos dentro de la carpeta |
| **ls -a** | Mostrar archivos ocultos| 

2. ### 🔗 **Manipulacion archivos**

|   codigo       | Descripción               
|------------|---------------------------|
| **git clone <**ruta HTTPS**>**    | Clonar Repositorio Remoto a Repositorio Local |
| **mkdir <nombre_carpeta>**|Creacion Carpeta|
| **git rm <nombre_carpeta>**|Eliminacion Archivo|
| **git mv  <nombre_archivo>**|Cambiar nombre Carpeta|
| **git rm --cached <nombre_archivo>**|Remover archivo del --> <**area de preparacion**>|


3. ### 🩹 **Restauracion de Archivos**

|   codigo       | Descripción               
|------------|---------------------------|
| **git restore <nombre_archivo>**    | Restaurar archivo en el <**area local**> --> <**alojado en area de preparacion**> |
| **git checkout <nombre_archivo>**|Volver hacia atras, hasta la ultima vez que hiciste cambios <**commit**>|




## 🌐**Creacion Repositorio**

| codigo       | Descripción               | 
|------------|---------------------------|
| **git init**   | Iniacializar repositorio       
| **git status** | Estatus de los archivos                  
| **git add <nombre_archivo>**     | Area de local --> Area de preparacion|    
| **git add .**     | Otra manera|    
| **git commits -m "mensaje"**     | Confirmacion de Ejecucion|   
| **git commits -a**     | Otra manera|   
| **git push origin main**     | ⬆️ Repo local --> Repo remoto|    
| **git pull**     | ⬇️ Cambios de Repo remoto --> Repo local|    








## ➕ **Commits**

- **Mostar Commit Mejorado**
    - Agregando Alias.
    - Se incluye un Diagrama de Ramas
    - Se incluye hace cuanto tiempo se hizo el commit.
    > git log-mejorado
>  **git config --global alias.log-mejorado "log --oneline --graph --all --pretty=format:'%C(auto)%h%d %s %C(black)%C(bold)%cr'"**

1. ### **Visualizacion y Comparacion de commits**

| codigo       | Descripción               | 
|------------|---------------------------|
| **git log --oneline**   | Mostrar todos los commits, hasta el momento
| **git diff <**hash**> <**hash**>**   | Comparacion de Commits
| **git diff --name-only <**hash**> <**hash**>**   | Nombre de los archivos que cambiaron
| **git diff --word-diff <**hash**> <**hash**>**   | Mostrar Diferencia entre 2 commits


2. ### **Modificacion de commits**

| codigo       | Descripción               | 
|------------|---------------------------|
| **git commit --amend**   | Modificar nombre del **Ultimo Commit** (HEAD)
| **git rebase-i head~**    |      Modificar Cualquier commit hecho          |
| **git rebase --continue**   |     Restaurar ultimos commit           |



3. ### **Eliminacion de commits**
| codigo       | Descripción               | 
|------------|---------------------------|
| **git reset --soft <**hash**>**   |Eliminacion de Commits (mover a area de preparacion).
| **git reset --soft head~2**        |Mover el head (en este ejemplo: **eliminamos 2 hacia abajo**)            |





## 🌿 **Ramas**

|   codigo       | Descripción               | 
|------------|---------------------------|
| **git branch**   | Mostrar Ramas Creadas 
| **git branch <**NombreRama**>**   | Crear Rama 
| **git switch -c <**NombreRama**>**   | Crear Rama y pocisionarse en ella 
| **git switch <**NombreRama**>**   | Cambiar Rama 
| **git branch -m <**NombreRama**> <**NuevoNombre**>**   |  Modificar Nombre Rama 
| **git branch -d <**NombreRama**>**   | Eliminar Rama 
| **git merge <**NombreRama**>**   | Fusionar Rama, Posicionado en la rama en la que agregare el contenido
| **git reset --hard <**hash**>**   | Deshacer commit fusionado




## **Git ignore**

1. Crear archivo **.gitignore**

- Mostrar nombre de los archivos involucrados en el commit.
> git ls-tree -r --name-only <**hash**>

-