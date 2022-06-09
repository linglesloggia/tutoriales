- Editar .bashrc agregando las lineas:

export http_proxy=http://proxy.fing.edu.uy:3128/
export https_proxy=https://proxy.fing.edu.uy:3128/

Luego darle source .bashrc

Modificar /etc/sudoers agregando la linea Defaults env_keep="https_proxy"

Finalmente se agrega la repo con

sudo -E add-apt-repository ppa:the_ppa_you_want_to_add


Fuente: https://askubuntu.com/questions/212132/i-cant-add-ppa-repository-behind-the-proxy
