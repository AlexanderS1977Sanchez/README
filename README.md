# 📱 Blog Notas

Aplicación móvil multiplataforma desarrollada con Flutter y Firebase Realtime Database para la gestión de notas en tiempo real.

---

# 📖 Descripción del Proyecto

**Blog Notas** es una aplicación creada con Flutter que permite registrar, almacenar y visualizar notas utilizando una base de datos en la nube mediante Firebase Realtime Database.

El objetivo principal del proyecto es demostrar la integración de Flutter con servicios backend de Firebase, permitiendo sincronización de datos en tiempo real sin necesidad de administrar servidores propios.

La aplicación está diseñada bajo una arquitectura simple y escalable, ideal para aprendizaje, prototipos y futuras ampliaciones funcionales.

---

# ✨ Características

- 📌 Creación de notas
- ☁️ Persistencia de datos en Firebase
- 🔄 Sincronización en tiempo real
- 📱 Compatibilidad multiplataforma
- ⚡ Interfaz rápida y ligera
- 🔥 Integración con Firebase SDK

---

# 🛠️ Tecnologías Utilizadas

| Tecnología | Descripción |
|---|---|
| Flutter | Framework UI multiplataforma desarrollado por Google |
| Dart | Lenguaje de programación utilizado por Flutter |
| Firebase Core | Inicialización y conexión con Firebase |
| Firebase Realtime Database | Base de datos NoSQL en tiempo real |
| Kotlin | Configuración Android |
| Gradle | Sistema de automatización de builds |

---

# 📂 Estructura del Proyecto

```plaintext
flutter-blog-notas/
│
├── android/                  # Configuración Android
├── ios/                      # Configuración iOS
├── lib/                      # Código fuente principal
│   └── main.dart             # Punto de entrada de la aplicación
├── web/                      # Configuración Web
├── windows/                  # Configuración Windows
├── test/                     # Pruebas
├── pubspec.yaml              # Dependencias del proyecto
├── analysis_options.yaml     # Reglas de análisis Dart
└── README.md                 # Documentación
```

---

# ⚙️ Requisitos Previos

Antes de ejecutar el proyecto asegúrate de tener instalado:

- Flutter SDK
- Dart SDK
- Android Studio
- Visual Studio Code (opcional)
- Java 17
- Android SDK

---

# 🚀 Instalación

## 1️⃣ Clonar el repositorio

```bash
git clone https://github.com/TU-USUARIO/flutter-blog-notas.git
```

---

## 2️⃣ Acceder al proyecto

```bash
cd flutter-blog-notas
```

---

## 3️⃣ Instalar dependencias

```bash
flutter pub get
```

---

# 🔥 Configuración Firebase

## 1️⃣ Crear proyecto Firebase

Acceder a:

https://console.firebase.google.com/

---

## 2️⃣ Registrar aplicación Android

Utilizar el siguiente identificador:

```plaintext
com.example.blog_notas
```

---

## 3️⃣ Descargar archivo de configuración

Descargar:

```plaintext
google-services.json
```

Ubicar archivo en:

```plaintext
android/app/
```

---

# 🌐 Permisos Android

Agregar permiso de internet en:

```plaintext
android/app/src/main/AndroidManifest.xml
```

Antes de la etiqueta `<application>`:

```xml
<uses-permission android:name="android.permission.INTERNET"/>
```

---

# ▶️ Ejecución del Proyecto

## Ejecutar aplicación

```bash
flutter run
```

---

## Verificar dispositivos disponibles

```bash
flutter devices
```

---

# 📦 Compilación APK

Generar APK Android:

```bash
flutter build apk
```

APK generado en:

```plaintext
build/app/outputs/flutter-apk/
```

---

# 🧹 Limpieza del Proyecto

```bash
flutter clean
```

---

# 🔗 Conexión con Firebase

La aplicación utiliza Firebase Realtime Database para almacenar y sincronizar información en tiempo real.

## Ejemplo de escritura

```dart
DatabaseReference ref = FirebaseDatabase.instance.ref("notas");

await ref.push().set({
  "titulo": "Mi Nota",
  "contenido": "Contenido ejemplo"
});
```

---

## Ejemplo de lectura

```dart
DatabaseReference ref = FirebaseDatabase.instance.ref("notas");

ref.onValue.listen((event) {
  final data = event.snapshot.value;
  print(data);
});
```

---

# 📌 Configuración SDK

Si existe incompatibilidad con la versión de Dart modificar:

```yaml
environment:
  sdk: ">=3.8.1 <4.0.0"
```

---

# 📱 Plataformas Compatibles

| Plataforma | Estado |
|---|---|
| Android | ✅ Compatible |
| iOS | ✅ Compatible |
| Web | ✅ Compatible |
| Windows | ✅ Compatible |

---

# 🔮 Mejoras Futuras

- 🔐 Firebase Authentication
- 🌙 Modo oscuro
- 🗑️ CRUD completo
- 🔔 Notificaciones Push
- 📊 Cloud Firestore
- 🧠 Arquitectura limpia
- ⚙️ Provider / Riverpod / Bloc

---

# 👨‍💻 Autor

** GRUPO  **  
Ingeniería en Sistemas de Información  
Universidad Central del Ecuador

---

# 📄 Licencia

Este proyecto se distribuye bajo la licencia MIT.

```text
MIT License

Copyright (c) 2026 

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files, to deal in the Software
without restriction, including without limitation the rights to use, copy,
modify, merge, publish, distribute, sublicense, and/or sell copies of the Software.
```
