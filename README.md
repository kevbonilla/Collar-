## Table of Contents
1. [General Info](#general-info)  
2. [Technologies](#technologies)  
3. [Installation](#installation)  
4. [FAQs](#faqs)  

---

### General Info
El **Collar Inteligente para Mascotas** es un dispositivo IoT diseñado para mejorar la calidad de vida y la seguridad de las mascotas. Este proyecto utiliza un microcontrolador ESP32 integrado con sensores biométricos, un módulo GPS y conectividad Wi-Fi para monitorear en tiempo real la salud y ubicación del animal. La información recopilada se envía a la plataforma **ThingSpeak** para su análisis y visualización.

**Estado del proyecto:** En desarrollo (prototipo funcional en pruebas).


---

## Technologies
Este proyecto utiliza las siguientes tecnologías y bibliotecas:  
* [ESP32](https://www.espressif.com): Microcontrolador principal  
* [ThingSpeak](https://thingspeak.com): Plataforma de almacenamiento y visualización de datos IoT  
* [DallasTemperature](https://github.com/milesburton/Arduino-Temperature-Control-Library): Lectura del sensor de temperatura DS18B20  
* [TinyGPS++](https://github.com/mikalhart/TinyGPSPlus): Procesamiento de datos GPS  
* [PulseSensor Playground](https://github.com/WorldFamousElectronics/PulseSensorPlayground): Biblioteca para el pulsómetro  
* [WiFiClient](https://www.arduino.cc/en/Reference/WiFi): Conexión a redes Wi-Fi  

---

## Installation
Sigue estos pasos para configurar el proyecto:

1. Clona el repositorio:  
   ```
   $ git clone https://github.com/usuario/collar-inteligente.git
   ```

2. Navega al directorio del proyecto:  
   ```
   $ cd ../path/to/the/file
   ```

3. Instala las bibliotecas necesarias desde el Administrador de Bibliotecas de Arduino:
   - **DallasTemperature**
   - **TinyGPS++**
   - **PulseSensor Playground**

4. Carga el código al ESP32 desde el IDE de Arduino.

5. Configura las credenciales Wi-Fi en el código:
   ```cpp
   const char* ssid = "tu_red_wifi";
   const char* password = "tu_contraseña";
   ```

6. Ajusta las credenciales de ThingSpeak:
   ```cpp
   unsigned long channelID = 123456;
   const char* WriteAPIKey = "TU_API_KEY";
   ```

---

## FAQs
**1. ¿Qué sensores se utilizan en el collar?**  
El collar incluye un sensor de temperatura (DS18B20), un pulsómetro y un módulo GPS (NEO-6M).  

**2. ¿Cómo puedo monitorear la información de mi mascota?**  
Los datos se envían en tiempo real a ThingSpeak, donde puedes visualizar la temperatura, frecuencia cardíaca y ubicación de tu mascota.  

**3. ¿Cuánto dura la batería del dispositivo?**  
El diseño actual optimiza el consumo energético, permitiendo un tiempo de uso de varios días dependiendo de la configuración y frecuencia de los envíos de datos.  

**4. ¿Qué hacer si el collar pierde conexión a Wi-Fi?**  
El collar intentará reconectarse automáticamente. Si esto no sucede, revisa la red Wi-Fi o reinicia el dispositivo.  

**5. ¿Puedo agregar más sensores?**  
Sí, el ESP32 tiene capacidad para integrar sensores adicionales. Sin embargo, debes asegurarte de no exceder los límites de corriente o memoria del microcontrolador.  
