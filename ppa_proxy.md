# Agregar PPA a través del proxy de fing:

Al parecer al configurar el proxy a apt no es suficiente. Es necesario seguir los siguientes pasos:



Editar .bashrc agregando las lineas:

```
export http_proxy=http://proxy.fing.edu.uy:3128/ 
export https_proxy=https://proxy.fing.edu.uy:3128/
```

Luego reiniciarla o correr

```
source .bashrc
```

Modificar /etc/sudoers agregando la linea Defaults env_keep="https_proxy"

Finalmente se agrega la repo con

```
sudo -E add-apt-repository ppa:the_ppa_you_want_to_add
```

Fuente: [https://askubuntu.com/questions/212132/i-cant-add-ppa-repository-behind-the-proxy](https://askubuntu.com/questions/212132/i-cant-add-ppa-repository-behind-the-proxy)
