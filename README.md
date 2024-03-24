Integracion de un proyecto Android existente en RN usando Windows.

guia: https://reactnative.dev/docs/integration-with-existing-apps?language=java

Problemas más notorios:
En los settings de gradle; "repositoriesMode.set(RepositoriesMode.PREFER_SETTINGS)" Hay que cambiar la preferencia de FAIL a PREFER_SETTINGS


En build.gradle a nivel de app: 
compileOptions {
        sourceCompatibility JavaVersion.VERSION_17
        targetCompatibility JavaVersion.VERSION_17
    }
    kotlinOptions {
        jvmTarget = '17'
    }
    Debe de estar en la misma versión que lo del kotlintoolchain, el cual es la 17
