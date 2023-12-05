# Configuración inicial
En un primer lugar necesitamos instalar los paquetes necesarios

> sudo apt install ansible

## **Importante abrir primero una conexión antes con los dispositivos para intercambio de claves.**

## Explicación
Una vez lo tenemos configurado se puede ejecutar comandos directamente desde la línea de comandos, pero yo uso dos archivos (**hosts** y **deployments**).

En un archivo hosts.ini ponemos algo parecido a esto, con todos los dispositivos que queremos usar, en este caso un AP:

```python
[AP_CISCO]
 AP57 ansible_host=10.99.99.20 ansible_user=ansible ansible_ssh_pass=ansible ansible_network_os=ios
```

Luego tenemos los archivos donde pondremos la configuración que serán de extensión yaml. 

Y siempre de cabecera, el nombre y el nombre del conjunto de hosts, en este caso **AP_CISCO**:

``` yaml
- name: Configurar AP Cisco
   hosts: AP_CISCO
```

