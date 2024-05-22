<p align="left">
  <img src="https://semanadelcannabis.cayetano.edu.pe/assets/img/logo-upch.png" width="150">
  <h1 align="center">Módulo 4: Servidores virtuales</h1>
</p>

# Descripción del módulo

Las actividades de este módulo incluyen actividades prácticas donde creará una instancia EC2, adjuntará una clave de acceso, accederá a la instancia mediante la consola de comandos y creará un sitio web sencillo y lo alojará en la instancia de EC2 mediante un bucket de Amazon Simple Storage Service (Amazon S3).


# Terminologia
- **Amazon Elastic Compute Cloud(Amazon EC2)**:Servicio que ofrece capacidad informatica escalable en la nube.Alquilar una pc ne la nube
- **Amazon Simple Storage Service (Amazon S3)**:Servicion que almacena datos en la nube
- **Sistema de nombres de dominio (DNS)**: Sistema de nomenlatura para computadoras , dispositivos y recursos conectados a una red
- **Bucket de Amazon Simple Storage Service (Amazon S3)**:Un contenedor de objetos en amazon S3
- **Política**:Objeto de AWS que cuando se asocia a una identidad o recurso define sus permisos.Se evaluan cuando se realiza una solicitud
- **Nombre de dominio**:Etiqueta que identifica una red de computadoras bajo control centralizado
- **Amazon Route 53**:Servicio web DNS de AWS
- **Nube privada virtual (VPC)**:red vitual dedicada a su cuenta AWS.Esta infraestructra esta aislada de forma logica de otras redes virtuales de la nube de AWS.Util para proteger datos y administrar permisos de acceso
- **Notación de objetos JavaScript (JSON)**:Sintaxis para almacenar datos
- **Sitio web dinámico**:Sitio web que cambia segun la interacciones del usuario 
- **Sitio web estatico**:Un sitio web que no cambia segun las interaccioones del usuario

# Laboratorio 1


![image](https://github.com/JoseCuevaRamos/Redes_Actividades_Jose_cueva/assets/150297438/595eb6aa-0210-405f-9483-0432f5296b5d)



![image](https://github.com/JoseCuevaRamos/Redes_Actividades_Jose_cueva/assets/150297438/38601809-5006-4275-a53a-217cdec77471)

![image](https://github.com/JoseCuevaRamos/Redes_Actividades_Jose_cueva/assets/150297438/899c5eee-7adf-46cd-88a8-4ebf47391acf)

# Laboratorio 2

![image](https://github.com/JoseCuevaRamos/Redes_Actividades_Jose_cueva/assets/150297438/1be575d5-1923-43dc-a4a2-a154bd4d1507)

![image](https://github.com/JoseCuevaRamos/Redes_Actividades_Jose_cueva/assets/150297438/068c3324-763b-4020-a9fe-a8dd227adedc)

![image](https://github.com/JoseCuevaRamos/Redes_Actividades_Jose_cueva/assets/150297438/f7f91e1d-0096-4948-9843-c9359ac3b03e)

![image](https://github.com/JoseCuevaRamos/Redes_Actividades_Jose_cueva/assets/150297438/a1d34020-7448-47fb-a316-ab1292c06a64)

# Conceptos del laboratorio :

## public adress
A public address means that the instance can be reached from the internet. Each instance that receives a public IP address is also given an external DNS hostname; for example, ec2-xxx-xxx-xxx-xxx.compute-1.amazonaws.com. AWS resolves an external DNS hostname to the public IP address of the instance when communication comes from outside its VPC. When communication comes from inside its VPC, the DNS hostname is resolved to the private IPv4 address.

## vockey 

The vockey key pair you selected will allow you to connect to this instance via SSH after it has launched. Although you will not need to do that in this lab, it is still required to identify an existing key pair, or create a new one, when you launch an instance.

- Listas de control de acceso: ACL(habilitadas y no habilitadas)
- punto de enlace
