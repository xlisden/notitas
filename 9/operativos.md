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
* alta disponibilidad, live migration,   "el siustema no muere"
  *** configurar live migration para hacer la tesis de Dacia

  		
  
  

*** virtualizadores aparte de VirtualBox

--------------

* VMware al ser comprado ya no se usa tanto de manera gratuita
* vmdk es bueno para migraciones, si necesitas migrar de hard disk drive
* que es Split? +2+2??
	limite 50GB
* archivo virtual, se puede cambiar de carcasa de servidor, ya que toda su información se puede pasar con el archivo virtual
* 
