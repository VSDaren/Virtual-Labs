# Virtual-Labs
Repositorio donde se recopilan máquinas virtuales de Linux para la identificación de tráfico en redes
El laboratorio está compuesto por dos máquinas virtuales conectadas a través de una red interna aislada en VirtualBox, garantizando un entorno seguro para capturas de red sin afectar el tráfico físico

Hipervisor: Oracle VM VirtualBox
Red Interna: LAB-CIA

1. Nodo de Auditoría (Atacante)
   OS: Kali Linux
   Rol: Ejecución de pruebas de red, escaneo de puertos y auditoría activa.
   Credenciales: 'usuario: atacante' | 'password: 12345'

2. Nodo Objetivo (Víctima)
   OS: Debian 13 (Trixie)
   Rol: Servidor Objetivo y analisis de paquetes
   Herramientas preconfiguradas destacadas:
     Snort3: Configurado para inspección de tráfico (Nota: La versión de Snort utilizada se compiló desde su código fuente ya que la versión estandarizada no se encuentra en los repositorios de Debian Trixie, por lo que se debe tener a consideración para la configuración posterior.
     Suricata: Configurado como motor de detección de intrusiones para el analisis de red y monitoreo de amenazas

Instrucciones para el despliegue de los entornos:
  Para poder utilizar el entorno sin la necesidad de tener que instalar y configurar las herramientas descargue las imágenes exportadas.

  ### Enlaces de descarga (Archivos .ova)
1. Kali Linux (LAB-CIA.ova) - 7.01GB | [Enlace de descarga]
2. Debian Trixie Linux (Debian.ova) - 6.62GB | [Enlace de descarga]

   ### Instrucciones de importación
1. Descargue las imágenes .ova proporcionadas en la sección de descargas más arriba.
2. Ejecute Virtualbox y vaya a la sección Archivo > Importar Servicio Virtualizado.
3. Seleccione los archivos .ova y haga clic en 'Siguiente'
4. (Opcional) Si su equipo cuenta con limitaciones de memoria puede ajustar la cantidad asignada a cada máquina, aunque lo recomendable es que ambas tengan por lo menos 2GB de memoria asignada.
5. Haga clic en 'Terminar'.
6. Antes de iniciar las máquinas virtuales, verifique que dentro de las configuraciones de red de ambas máquinas estén conectadas a la misma red interna ('LAB-CIA').
