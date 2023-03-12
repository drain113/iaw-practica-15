# Práctica 15: IoT Dashboard - Sensores, MQTT, Telegraf, InfluxDB y Grafana.
<p align="center">
<img src="https://raw.githubusercontent.com/drain113/pictures/main/Fotos/Grafana_logo.svg.png" width="300">

<br>   <br/>  


# Índice

### [1. Funcionamiento](#funcionamiento)

### [2. Despliegue](#despliegue)

### [3. Conclusión](#conclusión)

<br> <br>  

# Funcionamiento
La práctica 15 consta de desplegar un servicio Web llamado **Grafana** donde podremos visualizar desde un panel de control con gráficos, los datos de un agente **Telegraf** que recoge valores en una base de datos **InfluxDB** sobre los mensajes de un MQTT, en este caso **mosquitto**.

La idea es recoger los valores de los sensores de las aulas de la clase y que estos envíen sus datos mediante mosquitto para recibirlos en nuestra web.



<br>

# Despliegue
Para desplegar la aplicación, simplemente habrá que utilizar Docker compose:

```docker-compose
docker compose up -d
```
Para eliminarla:
```docker-compose
docker compose down -v 
```
También podemos envíar datos al gráfico mediante
```
mosquitto_pub -h localhost -t iescelia/aula22/co2 -m "120"
```
# Conclusión

En definitiva, Docker simplifica el proceso de creación y gestión de aplicaciones, permitiendo que los desarrolladores se centren en la innovación y el desarrollo de nuevas características.  
<br>
-Guille  
<br>
 [![](https://preview.redd.it/enr7hhg3zku81.png?auto=webp&s=fc017e6a82f91cc81ab3dd7d0388ef57bfd72c30)](https://github.com/drain113)
