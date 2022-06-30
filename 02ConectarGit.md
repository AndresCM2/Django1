# Configuración git

1. **Para iniciar git lo primero que hay que hacer es ejecutar el siguiente comando.**
```
git init
```
2. **Cambiar de rama a `main`**
```
git branch -M main
```
3. **Crear archivo para ignorar el contenido al momento de conectar con Github**
```
touch .gitignore
```
4. **Incluir en este archivo la carpeta virutal**
```
venv/
```
5. **Creamos el correo y nombre de usuario con los siguientes comandos.**
```
git config --global user.email "py.andres.castao@gmail.com"
```
```
git config --global user.name "michaael andres"
```
6. **Con el siguiente comando validamos la configuración o creación de los nombres.**
```
git config --global -l
```
7. **Con el siguiente comando conectamos github**
```
git remote add origin https://github.com/AndresCM2/Django1.git
```
8. **Validar nombre**
```
git remote
```
9. **Validar conexiones**
```
git remote -v
```
10. **Crear una clave privada**
```
ssh-keygen -t rsa -b 4096 -C "xxxxxxxx@xxxxxx.com"
```
Al ejecutar este comando me solicita crear el nombre del archivo le doy enter.
me solicita la clave con la que voy a guardar el nombre del archivo y me pide confirmarla nuevamente de esta forma me genera en la ruta de mi usuario una carpeta .ssh con en nombre id_rsa y otra con el nombre id_rsa.pub.

Con el siguiente comando validamos que efectivamente fue creado la clave privada.

```
eval "$(ssh-agent -s)"
```

de esta forma copio mi archivo.pub en la siguiente ruta en github.

Ingresamos a setting de github, luego a SSH and GPG keys, le damos click a New SSH key pegamos  la clave en Key, le damos y un title y luego lo add (añadimos).

Vamos a github y copiamos en el enlace ssh generado para ejecutarlo en con el siguiente comando.
``` 
git remote set-url origin git@github.com:AndresCM2/Django1.git
```

11. **Jalar la conexión del repositorio Github**
```
git pull origin main 
```
12. **Forzar**
```
git pull origin main --allow-unrelated-histories
```
13. **Empujar información**
```
git push origin main
```
14. **Añadimos los cambios**
```
git add -A
```
15. **Generamos un commit**
```
git commit -m "conexión a git"
```
