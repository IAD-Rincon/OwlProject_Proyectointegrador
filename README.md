# [Ruteros: sin paradas]

Prototipo del Proyecto Integrador de Sistemas Interactivos (UPGCH, 5.° semestre, grupo A1).
Juego de conducción de una combi en Unity.

## Integrantes y roles

| Integrante | Rol |
|---|---|
| Josue Daniel Sanchez Montoya | Modelado 3D (entorno y objetos) |
| Miguel Alejandro Gordillo Gordillo | Dirección de proyecto, desarrollo web, diseño UI y documentación |
| Mauricio Gomez Archundia | Programación (Unity) |
| Juan Pedro Coutiño Trujillo | Modelado 3D y composición musical |
| Maximiliano Coronel Huerta | Ilustración artística y diseño de interfaz |

## Motor

- Unity 6000.6.8f1 (URP)
- Plataforma del build: Windows 64-bit

## Cómo ejecutar el build

1. Descarga el archivo `.zip` desde la sección **Releases** de este repositorio.
2. Descomprime la carpeta completa (no ejecutes el `.exe` desde dentro del .zip).
3. Abre `Ruteros sin paradas.exe` (en la build v0.1 se llama `My project.exe`).
4. Si Windows muestra el aviso azul de SmartScreen, da clic en *Más información > Ejecutar de todas formas* (el build no está firmado).

## Controles

| Acción | Tecla |
|---|---|
| Acelerar | W / ↑ |
| Frenar / reversa | S / ↓ |
| Girar izquierda / derecha | A, D / ← → |
| Freno de mano | Espacio |

## Estado actual

**Funciona:**
- Movimiento de la combi con aceleración, frenado e inercia; el giro depende de la velocidad.
- Cámara en tercera persona con FOV dinámico que no atraviesa paredes.
- Velocímetro en pantalla (km/h).
- Cielo HDRI de atardecer, niebla y post-proceso (ACES, bloom, corrección de color).
- Colisiones con calles, pasos de cebra y banquetas.

**Falta:**
- Mapa completo del recorrido.
- Colocar en la escena los autos ya modelados (Tsurus, Vochos, Rams) y darles colliders, igual que a la señalización.

## Estructura del proyecto

```
Assets/
├── Materials/     materiales (Cielo_Atardecer = skybox)
├── Modelos/       .fbx de la combi, autos, calles y señalización
├── Referencias/   imágenes de referencia (no van en la build)
├── Scenes/        Ruta.unity (escena principal)
├── Scripts/       CombiController, CamaraSigueCombi, VelocimetroHUD
├── Settings/      URP y perfil de post-proceso
└── Texturas/      HDRI y texturas
```

> Antes de clonar, instalen Git LFS (`git lfs install`). Los modelos, texturas e imágenes se guardan con LFS.
