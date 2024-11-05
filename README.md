# My Dependencies for Kotlin

### In the project's build.gradle.kts
```kotlin
    //...

    // KSP
    id("com.google.devtools.ksp") version "1.9.0-1.0.13"
```
In the module's build.gradle.kts

```kotlin
plugins {
    //...

    //Dagger Hilt
    id("kotlin-kapt")

    // KPS
    id("com.google.devtools.ksp")
}
dependencies {
    //...

    //Dagger Hilt
    implementation(libs.hilt.android)
    ksp(libs.hilt.android.compiler)

    // Coroutines
    implementation(libs.androidx.lifecycle.runtime.ktx)

    // ROOM
    implementation(libs.room.runtime)
    ksp(libs.androidx.room.compiler)
}

```
