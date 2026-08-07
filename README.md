# Sistema de Ahorro de Energía con ESP32 - Light Sleep

## Descripción
Este proyecto implementa un sistema de gestión de energía en el ESP32 utilizando el modo **Light Sleep**. Simula una tarea activa durante 8 segundos y luego entra en reposo, pudiendo ser reactivado mediante un botón externo o un temporizador automático. El proyecto está diseñado para ejecutarse completamente en el simulador **Wokwi**.

## Funcionamiento
- **Modo Activo**: LED rojo (GPIO2) parpadea cada 500ms durante 8 segundos, simulando una tarea en ejecución.
- **Modo Reposo**: LED amarillo (GPIO4) se enciende fijo, indicando que el sistema está en Light Sleep.
- **Reactivación**: 
  - Botón externo en GPIO5 (presionar para despertar inmediatamente)
  - Temporizador automático (15 segundos)
- **Confirmación**: Al despertar, el LED amarillo parpadea 6 veces.

## Componentes en Wokwi
- 1 ESP32 DevKit V4
- 1 LED Rojo (GPIO2)
- 1 LED Amarillo (GPIO4)
- 2 Resistencias de 220Ω
- 1 Botón pulsador (GPIO5)
- 1 Resistencia de 10kΩ (pull-up)

## Instrucciones de Ejecución en Wokwi

### Opción 1: Desde el navegador
1. Abrir [Wokwi.com](https://wokwi.com)
2. Crear un nuevo proyecto con ESP32
3. Copiar el código `main.cpp` en el editor
4. Copiar el diagrama JSON en el archivo `diagram.json`
5. Hacer clic en "Start Simulation"

### Opción 2: Desde VS Code con PlatformIO
1. Clonar el repositorio:
```bash
git clone https://github.com/tu-usuario/ESP32-LightSleep-Demo.git
