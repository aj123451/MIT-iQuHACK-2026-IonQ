# ⚛️ MIT iQuHACK 2026 - IonQ Quantum Networking Challenge

Este repositorio contiene la solución desarrollada por el equipo de **Quantum Verse** para el reto propuesto por **IonQ** durante el **MIT iQuHACK 2026**, uno de los hackathons de computación cuántica más prestigiosos del mundo organizado por el Massachusetts Institute of Technology.

## 🎯 El Reto
El desafío consistía en un juego de estrategia competitivo estilo *Risk* basado en la física de redes cuánticas. El objetivo era conquistar nodos (ciudades) alrededor del mundo estableciendo enlaces de entrelazamiento cuántico. 

El problema principal era el **ruido cuántico**. Los pares de Bell "crudos" sufrían de baja fidelidad debido a la interferencia en la red (errores de bit y de fase). Para reclamar un enlace de alta dificultad, debíamos alcanzar una fidelidad de transmisión superior a **0.90**, todo ello gestionando un presupuesto muy estricto de recursos cuánticos.

## 🚀 Nuestra Solución: Destilación de Entrelazamiento (Entanglement Distillation)
Desarrollamos algoritmos de corrección de errores mediante protocolos adaptativos **LOCC** (Local Operations and Classical Communication). En lugar de depender de métodos estándar que consumen muchos recursos, diseñamos estrategias de alta eficiencia:

### 1. Estrategia "Protección de Fase" (2 Bell Pairs)
Un circuito altamente optimizado para enlaces con ruido predominante de Fase (Z). 
* Utilizamos puertas Hadamard y un par de sacrificio como "chivato" mediante puertas CNOT bilaterales.
* Si la medida del par de sacrificio indicaba paridad correcta (`flag = 0`), el par de destino colapsaba en un estado de alta pureza.
* **Resultado:** Conquista de nodos de Dificultad 3 (ej. Moscú) gastando la mitad de recursos que los equipos competidores.

### 2. Estrategia "El Tanque X+Z" (3 Bell Pairs)
Para nodos críticos donde el ruido era mixto o desconocido, implementamos un protocolo de limpieza completa.
* **Sacrificio Z:** Un par dedicado exclusivamente a detectar y filtrar errores de Fase.
* **Sacrificio X:** Un par dedicado a detectar y filtrar errores de Bit.
* **Resultado:** Al purificar el entrelazamiento en ambas bases de forma secuencial, garantizamos la captura de los nodos más valiosos del mapa (ej. Minsk, Kyiv) superando los umbrales de fidelidad más exigentes.

## 🛠️ Tecnologías Utilizadas
* **Python:** Para la lógica de enrutamiento, análisis de nodos y llamadas a la API del simulador.
* **Qiskit:** Diseño, construcción y simulación de los circuitos de destilación cuántica.
* **OpenQASM 3.0:** Exportación de los circuitos y lógica de control condicional clásica a nivel de hardware para su ejecución en la infraestructura de IonQ.

## 🏆 Logros Destacados
* **Optimización de Presupuesto:** Alcanzamos fidelidades >0.90 utilizando estrategias de 2 y 3 pares, maximizando nuestro "Claim Strength" global.
* **Expansión Estratégica:** Desarrollo de un script de análisis heurístico para identificar "Utility Qubits" y "Bonus Bell Pairs" en el grafo, permitiendo una expansión eficiente por el norte y este de Europa.

*Proyecto desarrollado durante el MIT iQuHACK (Enero 2026).*
