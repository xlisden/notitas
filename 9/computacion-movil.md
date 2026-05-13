<hr/>
<details>
<summary><b>plantilla</b></summary>
  
  - item

</details>

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

</details>
