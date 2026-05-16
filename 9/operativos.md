20:58 15/05/2026
ServDBDE
- por recomendación/convención cualquier cosa que no sea el SO va en la unidad D
- D:\deprecated\SO
- cuando es software licenciado, no se carga al momento de crear la VM (se deja vacio)
- W Server 22 64bit
- 4gb ram
- 2 cpus
- EFI bootea por firmware (no activar)
- hard disk drive
	VHD/VHDX
	vmdk *UTILIZADO* + reservar completamente
- configurar
	general > portapapeles & drag and drop 
(bidireccional)
	sistema > óptica+disco duro activo, red 3ero
	pantalla > 
	almacenamiweto > azulito disk a choose file
	<img width="572" height="317" alt="image" src="https://github.com/user-attachments/assets/07db705d-7e74-4d0e-83c4-dd377b0e5798" />
	red > 
		con la NAT solo tienes internet
		adaptador puente todo, se puede poder ip similar *CAMBIAR A ESTO*
		<img width="689" height="281" alt="image" src="https://github.com/user-attachments/assets/c778366f-ac3a-417f-a725-184dc0a85483" />
  		4697BB = identifica la tarjeta de red, un programa puede estar pegado a una direccion fisica de RED
  	carpeta compartida, aparecen como una nueva uniidad / como un
  	<img width="777" height="357" alt="image" src="https://github.com/user-attachments/assets/eadfe9a2-d8b9-4d5d-afca-1960a0c434d7" />
- esquemas de particion
  GPT
  	programas actuales, para mas de 2TBm sistema con firmware UEFI
  MBR
  	hasta 2TB, W7 o W10 linux heradod
- licencia wndiws
  standard = hasta 2VMs, entorno fisico o baja densidad, mejor costo, replicar en fisico?? 
  datacenter = en la nube, para +12 VMs,
* alta disponibilidad, live migration,   "el sistema no muere"
  *** configurar live migration para hacer la tesis de Dacia. Podrias necesitar licencias para el Azure, con el ssh????
- CAL = Client Access License
  	UserCAL = para cuando hay mas empleados
  	DeviceCAL = solo el quipo tiene licencia, como para turnos rotativos
- tipos de licencia
  OEM = el sitema operativo esta del firmware / preinstalado de fabrica
  RETAIL = fisico, clave que te dan, tienda fisica / clave independiente del hardware, se puede usar 1 equipo conectado a la vez
  VOLUMEN / CSP = para organizaciones
  * licencias por procesador, o por nucleos. Caracteristicas del servidor, y al ser asesorado por los que saben, tendras las licencias adecuadas
- para desblioquaer
  <img width="504" height="195" alt="image" src="https://github.com/user-attachments/assets/b409ae7a-f927-43c3-ba12-c8c9a77b428f" />
- para que aparezcan <img width="468" height="309" alt="image" src="https://github.com/user-attachments/assets/9ba3f97b-b8bd-4bd1-bb2c-7e30921601aa" />
<img width="533" height="300" alt="image" src="https://github.com/user-attachments/assets/b1fe8524-6fc1-4914-9be6-581e909f0a42" />
- para redimiensionar <img width="382" height="198" alt="image" src="https://github.com/user-attachments/assets/1eed19b0-0296-4134-8c56-78f80af58846" />
para apagar unnplanned
  HYPER V
- SAN almacenamiento de disco en red / los SAN grandes se parewcen a servidores
- SAN y NAS = fibra canal. NAS en ethernet las es lenta SAN ES POR FIBRA ALTA VELOCIDAD
- 
  		
  
  

*** virtualizadores aparte de VirtualBox

--------------

* VMware al ser comprado ya no se usa tanto de manera gratuita
* vmdk es bueno para migraciones, si necesitas migrar de hard disk drive
* que es Split? +2+2??
	limite 50GB
* archivo virtual, se puede cambiar de carcasa de servidor, ya que toda su información se puede pasar con el archivo virtual
* 
