https://app.capacities.io/home/4bfe725f-95c1-4696-9e6e-68950f70b238
<hr/>
<details>
<summary><b>plantilla</b></summary>
  
  - item

</details>

  ```java
  ```

<hr/>
<details>
<summary><b>18:32 13/05/2026</b></summary>
  
  - item
  - package name = pe.edu.unu.compmov
  - API 34, android 14

  #### agregar dependencias
  build.gradle.kts (Module :app)
  ```java
    dependencies {    
        implementation(libs.appcompat)
        implementation(libs.material)
        implementation(libs.activity)
        implementation(libs.constraintlayout)
    
        //    aqui
    
        testImplementation(libs.junit)
        androidTestImplementation(libs.ext.junit)
        androidTestImplementation(libs.espresso.core)
    }
  ```
  #### permisos
  AndroidManifest.xml
  ```xml
  <?xml version="1.0" encoding="utf-8"?>
  <manifest xmlns:android="http://schemas.android.com/apk/res/android"
      xmlns:tools="http://schemas.android.com/tools">
      <!-- aqui -->
      <application
          android:allowBackup="true"
          android:dataExtractionRules="@xml/data_extraction_rules"
  ```
<img width="533" height="314" alt="image" src="https://github.com/user-attachments/assets/a74a8c59-9d60-4556-a6d6-0a6c1a9db79c" />

</details>


<hr/>
<details>
<summary><b>18:35 20/05/2026</b></summary>

  #### actividad
  - actividad = interaccion
  - rol = punto de entrada, pila de actividades (de tipo LIFO), gestion de recursos (destruye actividades en segundo plano para liberar memoria si fuera necesario)
  <img width="513" height="663" alt="image" src="https://github.com/user-attachments/assets/6af123fa-9a50-4d68-aa66-9b630680e23a" />

  #### callback
  - `onCreate()` = solo una vez, al iniciar los componentes
  - `onStart()` = visible para el usuario, listo para el primer plano, pero aun no se hace uso
  - `onPause()` = guarda datos para saber donde se ha quedado, pausar animaciones. Debe ser muy rapido
  - `onStop()` = se debe liberar recursos, sobretodo los pesados
  - `onDestroy()` = limpieza total, para que no quede memoria ocupada. Se llama antes que desaparezca completamente

  #### buenas practicas
  - debajo de compile options en build-gradle.tls, y suncronizar
    ```java
    buildFeatures = {viewBinding = true}
    ```
  - main 
    ```java
    class MainActivity : AppCompatActivity() {
    
        private lateinit var binding: ActivityMainBinding
    
        override fun onCreate(savedInstanceState: Bundle?) {
            super.onCreate(savedInstanceState)
            enableEdgeToEdge()
    //        setContentView(R.layout.activity_main)
            binding = ActivityMainBinding.inflate(layoutInflater)
            setContentView(binding.root)
            ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main)) { v, insets ->
                val systemBars = insets.getInsets(WindowInsetsCompat.Type.systemBars())
                v.setPadding(systemBars.left, systemBars.top, systemBars.right, systemBars.bottom)
                insets
            }
        }
    }
    ```
  
  #### agregar audio
  - res > androind resource diurectory algo > raw (archivos)
  ```java
    private var mediaPlayer: MediaPlayer? = null
  ```
  ```java
    override fun onStart() {
        super.onStart()
        Log.i("LifeCycle", "onStart()")
        mediaPlayer = MediaPlayer.create(this, R.raw.gallo)
    }
  ```
  ```java
    override fun onResume() {
        super.onResume()
        Log.i("LifeCycle", "onResume()")
        mediaPlayer?.start()
    }
  ```

  #### agregar second activity
  <img width="918" height="639" alt="image" src="https://github.com/user-attachments/assets/438b0577-d1f6-467a-bac8-6f70dc28ff49" />
</details>


<hr/>
<details>
<summary><b>18:37 1/07/2026</b></summary>
  
  - quitar sonido al minimizar
    ```java
    override fun onStop() {
        super.onStop()
        mediaPlayer?.stop()
    }
    ```
  - para tener donde se quedo
      ```java
    private var position: Int = 0
    ``` - 
    ```java
    override fun onPause() {
        super.onPause()
        mediaPlayer?.let { player ->
            player.pause()
            position = player.currentPosition
        }
    }
    ```
      on resume
    ```java
    mediaPlayer?.seekTo(position)
    ```
    <hr/>

  ### calculadora
    <img width="647" height="477" alt="image" src="https://github.com/user-attachments/assets/7a866d5d-12ce-4ff1-bc3b-768a4fd143ab" />

  - activity.xml
    ```java
    <?xml version="1.0" encoding="utf-8"?>
    <LinearLayout
        xmlns:android="http://schemas.android.com/apk/res/android"
        xmlns:app="http://schemas.android.com/apk/res-auto"
        xmlns:tools="http://schemas.android.com/tools"
        android:id="@+id/main"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        tools:context=".MainActivity"
        android:orientation="vertical"
        >
    </LinearLayout>
    ```
  - ss
  - wwww
  - w
    

    ```java
    mediaPlayer?.seekTo(position)
    ```
</details>
