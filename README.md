# My Dependencies for Kotlin

### In the project's build.gradle.kts
```kotlin
//Dagger hilt
id("com.google.dagger.hilt.android") version "2.48" apply false
```
In the module's build.gradle.kts

```kotlin
plugins {
    //...
    //Dagger Hilt
    id("com.google.dagger.hilt.android")
    id("kotlin-kapt")
}
dependencies {
    // ROOM
    implementation(libs.androidx.room.runtime)
    annotationProcessor(libs.androidx.room.compiler)
    kapt(libs.androidx.room.compiler)
    implementation(libs.androidx.room.ktx)

    // Coroutines
    implementation(libs.androidx.lifecycle.runtime.ktx.v262)

    // Dagger Hilt
    implementation( libs.hilt.android)
    kapt (libs.hilt.android.compiler.v248)
    implementation( libs.dagger)
}

```
