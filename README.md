# Entrenador Personal Virtual

Una aplicación móvil desarrollada con React Native y Firebase que permite a los usuarios gestionar rutinas de ejercicio y registrar su progreso.

## 🚀 Características Implementadas (Primer Entregable)

### ✅ Autenticación de Usuarios
- **Registro de nuevos usuarios** con validación de email y contraseña
- **Inicio de sesión** con credenciales existentes
- **Gestión de estado de autenticación** usando Firebase Authentication
- **Navegación condicional** basada en el estado de autenticación

### ✅ Gestión de Rutinas
- **Visualización de rutinas predefinidas** almacenadas en Firestore
- **Lista de rutinas** con información detallada (nombre, descripción, duración, nivel)
- **Navegación a detalle de rutina** para ver ejercicios específicos

### ✅ Registro de Progreso
- **Visualización de ejercicios** con series, repeticiones y descripciones
- **Marcado de ejercicios completados** con persistencia en Firestore
- **Barra de progreso visual** que muestra el porcentaje completado
- **Interfaz diferenciada** para ejercicios completados vs pendientes

## 🛠️ Tecnologías Utilizadas

- **React Native** con Expo
- **Firebase Authentication** para gestión de usuarios
- **Firebase Firestore** para almacenamiento de datos
- **React Navigation** para navegación entre pantallas

## 📱 Estructura de la Aplicación

### Pantallas Principales
1. **LoginScreen** - Inicio de sesión de usuarios
2. **RegisterScreen** - Registro de nuevos usuarios
3. **HomeScreen** - Pantalla principal con navegación
4. **RoutinesScreen** - Lista de rutinas disponibles
5. **RoutineDetailScreen** - Detalle de rutina con ejercicios

### Componentes Clave
- **AuthContext** - Contexto para gestión de autenticación
- **firebaseConfig** - Configuración de Firebase
- **AppNavigator** - Navegación condicional basada en autenticación

## 🗄️ Estructura de Datos

### Rutinas (Firestore Collection: `routines`)
```javascript
{
  name: "Rutina Principiante",
  description: "Rutina ideal para personas que están comenzando",
  duration: 30,
  level: "Principiante",
  exercises: [
    {
      id: "ex1",
      name: "Flexiones",
      sets: 2,
      reps: 10,
      description: "Flexiones de pecho tradicionales"
    }
  ]
}
```

### Progreso (Firestore Collection: `progress`)
```javascript
{
  userId: "user_id",
  routineId: "routine_id", 
  exerciseId: "exercise_id",
  completedAt: timestamp
}
```

## 🚀 Instalación y Configuración

### Prerrequisitos
- Node.js (v18 o superior)
- npm o yarn
- Cuenta de Firebase

### Pasos de Instalación

1. **Clonar el repositorio**
```bash
git clone [url-del-repositorio]
cd VirtualPersonalTrainer
```

2. **Instalar dependencias**
```bash
yarn install
```

3. **Configurar Firebase**
- Crear un proyecto en Firebase Console
- Habilitar Authentication (Email/Password)
- Crear base de datos Firestore
- Copiar las credenciales a `firebaseConfig.js`

4. **Inicializar datos de ejemplo**
```bash
node scripts/initializeData.js
```

5. **Ejecutar la aplicación**
```bash
npm run web    # Para web
npm run android # Para Android
npm run ios    # Para iOS
```

## 📋 Funcionalidades Probadas

### ✅ Casos de Uso Completados
1. **Usuario se registra exitosamente** ✓
2. **Usuario inicia sesión correctamente** ✓
3. **Usuario ve lista de rutinas disponibles** ✓
4. **Usuario navega a detalle de rutina** ✓
5. **Usuario marca ejercicios como completados** ✓
6. **Progreso se guarda y persiste en Firestore** ✓
7. **Interfaz se actualiza en tiempo real** ✓

### 🎯 Criterios de Aceptación del Primer Entregable
- [x] Registro e inicio de sesión funcional
- [x] Selección de rutina predefinida
- [x] Registro manual de progreso
- [x] Interfaz de usuario intuitiva
- [x] Integración con Firebase

## 🔄 Próximas Funcionalidades (Entregables Futuros)

### Segundo Entregable
- Creación de rutinas personalizadas
- Temporizador para ejercicios
- Historial de entrenamientos

### Tercer Entregable
- Modo offline con sincronización
- Notificaciones push
- Estadísticas y gráficos de progreso

## 🧪 Testing

La aplicación ha sido probada en:
- ✅ Navegador web (desarrollo)
- ⏳ Android (pendiente)
- ⏳ iOS (pendiente)

## 👥 Equipo de Desarrollo

- **Desarrollador Principal**: [Nombre del estudiante]
- **Asignatura**: Programación Móvil
- **Institución**: [Nombre de la institución]

## 📄 Licencia

Este proyecto es desarrollado con fines académicos para la asignatura de Programación Móvil.

---

**Fecha de entrega**: [Fecha]
**Versión**: 1.0.0 (Primer Entregable)
