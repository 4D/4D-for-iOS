---
id: xcode
title: Xcode
---

## ¿Qué es Xcode?

Xcode es un entorno de desarrollo integrado(IDE) y un conjunto de herramientas de desarrollo para macOS que se utilizan para crear aplicaciones para iPad, iPod, iPhone y Mac.

## Descargar

Para descargar la última versión de Xcode vaya a la App Store.

<div style="text-align: center; margin-top: 20px; margin-bottom: 20px">
  <p>
    

<a class="button" href="macappstore://itunes.apple.com/app/id497799835?mt=12">Ver in Mac App Store </a>

  </p>
</div>

Los desarrolladores registrados pueden descargar las versiones previas y las versiones anteriores de la suite a través del sitio web de desarrolladores de Apple.

🔗 https://developer.apple.com/download/more/ 🔗 https://developer.apple.com/xcode/

## Tabla de comparación de versión

| Xcode  | Swift | iOS      | 4D   | MacOS   |
| ------ | ----- | -------- | ---- | ------- |
| 11     | 5.1   | iOS 13.0 | 18   | 10.14.4 |
| 10.2.1 | 5.0   | iOS 12.2 | 17R6 | 10.14.4 |
| 10.2   | 4.2.1 | iOS 12.2 | 17R5 | 10.14.3 |
| 10.1   | 4.2.1 | iOS 12   | 17R4 | 10.13.6 |
| 10.0   | 4.2   | iOS 12   | 17R3 | 10.13.6 |
| 9.4    | 4.1.2 | iOS 11.4 | 17R2 | 10.13.2 |
| 9.3.1  | 4.1   | iOS 11.3 | 17R2 | 10.13.2 |

### Utilización de 17R6 con macOS 10.14.3

4D 17R6 requiere Swift5.0 runtime. (ya instalado con macOS 10.14.4)

- Instale `Swift 5 Runtime Support for Command Line Tools` desde [More Downloads for Apple Developers](https://developer.apple.com/download/more/)

### Compatibilidad

Frameworks compiled with one version of Xcode could not be used with another version.

The current release of swift(5) has ABI stability but no Module Stability. This two condition are needed to ship pre-compiled libraries.

Please see the Swift blog for more details. https://swift.org/blog/abi-stability-and-more/