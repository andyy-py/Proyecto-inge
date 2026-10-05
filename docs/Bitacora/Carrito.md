---
titulo: "Diseño y Manufactura Láser: Carrito F1"
autor: "Tu Nombre"
---

# Carrito F1 — Modelado CAD, Corte Láser y Ensamble

En este proyecto se abordó el flujo completo de desarrollo de un producto físico en MDF de 3 mm: desde el análisis de un modelo de referencia visual, el modelado 3D parametrizado en SolidWorks, la preparación de vectores DXF, la manufactura digital en corte láser hasta el ensamble físico y control de tolerancias.

---

## 1. Planificación, Referencia y Estructura de Archivos

Para el desarrollo del vehículo, se tomó como base una imagen de referencia visual. Se midieron las proporciones geométricas de cada componente para trasladar y reconstruir el modelo desde cero en **SolidWorks**.

- **Estandarización de espesor:** Todas las piezas se extruyeron a **3 mm**, adaptándose al grosor real de la lámina de MDF.
- **Gestión digital:** Cada componente se guardó de forma individual como archivo de pieza (`.SLDPRT`).
- **Uso de simetrías:** Las piezas dobles (como laterales y deflectores) se diseñaron utilizando la operación de simetría en el mismo archivo para asegurar precisión dimensional y optimizar tiempo.

![Estructura de la carpeta de archivos y piezas](./img_f1/archivos.png){ width=50% } 
![Modelado de pieza individual en SolidWorks](./img_f1/pieza.png){ width=50% }
![Modelado de pieza con simetria en SolidWorks](./img_f1/simetria.png){ width=50% }

---

## 2. Ensamble Digital y Preparación en SolidWorks

Antes de realizar el corte físico, se creó un archivo de **Ensamble 3D** para validar la coherencia geométrica de los encajes tipo rompecabezas (*press-fit*).

- **Mantenimiento de duplicados:** Para las piezas simétricas, se duplicaron e insertaron en el entorno de ensamble digital.
- **Mecanismo del volante:** Se modeló el subensamble articulado del volante mediante un tope mecánico que permite su rotación libre sin desprenderse de la columna de dirección.
- **Bisagra viva:** Al ser un elemento flexible, no se modeló en el ensamble 3D comprimido, sino que se preparó vectorialmente para su flexión tras el corte.

![Ensamble Digital 3D en SolidWorks](./img_f1/ensamble.png){ width=50% } 
![Detalle del mecanismo del volante](./img_f1/volante.png){ width=50% }

---

## 3. Exportación a DXF y Configuración de Corte Láser

Una vez verificado el ensamble 3D, se trasladaron las geometrías a un plano 2D (`.SLDDRW`) y se exportaron en formato **.DXF** (*Drawing Exchange Format*).

El archivo `.DXF` se cargó en el software **Falcon Design Space** para ser procesado en una cortadora **Creality Falcon A1** con un área de trabajo de **381 mm x 305 mm**.

### Parámetros de Corte
| Parámetro | Valor Configurado |
| :--- | :--- |
| **Material** | MDF de $3\text{ mm}$ |
| **Área de trabajo** | $381 \times 305\text{ mm}$ |
| **Velocidad de corte** | $25\text{ mm/s}$ ($1500\text{ mm/min}$) |
| **Potencia del láser** | $40\%$ |
| **Tipo de operación** | Corte vectorial lineal (*Vector Cut*) |

![Plano 2D en formato DXF](./img_f1/dxf.png){ width=50% } 
![Interfaz de Falcon Design Space y corte en proceso](./img_f1/corte.png){ width=50% }
![Foto del corte laser, maquina1](./img_f1/maquina1.png){ width=50% }
![Foto del corte laser, maquina2](./img_f1/maquina2.png){ width=50% }
![MDF cortado](./img_f1/mdf.png){ width=50% }

<br>
!!! note "Aclaración sobre la distribución en el software de corte" <br>
    El layout mostrado en la interfaz del software de corte no es idéntico visualmente al archivo `.DXF` original de dibujo. Esto se debe a que, al momento de mandar a cortar, se duplicaron e independizaron varias piezas en la mesa de trabajo (como las 16 capas de las llantas) y se reacomodaron de forma óptima para aprovechar mejor el área útil del MDF de 3 mm. La geometría de cada pieza sigue siendo exactamente la misma.

---

## 4. Secuencia de Ensamble Físico

El armado del monoplaza siguió un orden modular para asegurar la rigidez del chasis:

1. **Chasis base y ejes:** Montaje de la base central (**P9**) con los laterales (**P12**), acoplando previamente las ruedas centrales (**P20**, **P21**) y paneles decorativos (**P8**).
2. **Instalación del volante:** Colocación del subensamble articulado del volante con sus soportes (**P16**).
3. **Bisagra viva y cubierta:** Colocación de los soportes transversales (**P6**) y la tapa superior (**P17**).
4. **Alerón y habitáculo:** Ensamble de la cola trasera (**P18**, **P7**, **P10**), seguido del asiento (**P15**) y soportes del habitáculo (**P1**).
5. **Frontal y ruedas externas:** Acople de la nariz (**P19**), deflectores (**P11**), ensamble de los 16 discos de llantas (**P23**) con tapones (**P24**) y paneles laterales de cierre (**P22**).

![Proceso](./img_f1/armado1.png){ width=50% } 
![Proceso](./img_f1/armado2.png){ width=50% }
![Proceso](./img_f1/armado3.png){ width=50% } 
![Proceso](./img_f1/armado4.png){ width=50% }
![Proceso](./img_f1/armado5.png){ width=50% } 
![Proceso](./img_f1/armado6.png){ width=50% }
![Proceso](./img_f1/armado7.png){ width=50% } 
![Proceso](./img_f1/armado8.png){ width=50% }
![Proceso](./img_f1/armado9.png){ width=50% } 
![Proceso](./img_f1/armado10.png){ width=50% }
![Proceso](./img_f1/armado11.png){ width=50% } 
![Proceso](./img_f1/armado12.png){ width=50% }

---

## 5. Control de Calidad y Resolución de Problemas

- **Ajuste dimensional de encaje:** Durante el ensamble físico se presentó una ligera interferencia ($\approx 1\text{ mm}$) entre la cubierta superior (**P17**) y la ranura del lateral (**P12**).
- **Solución técnica:** Se realizó un ajuste mecánico manual limando levemente el conector de la pieza **P12**. Esto permitió un encaje firme a presión sin comprometer la integridad del MDF ni la estética general.

![Vehículo terminado F1](./img_f1/final.png){ width=50% }

---

## 6. Archivos del Proyecto

Puedes descargar la carpeta comprimida con todos los archivos fuente utilizados para este proyecto (piezas 3D, ensamble, planos 2D y archivos DXF para corte):

📥 [**Descargar Archivos del Proyecto (.ZIP)**](./ZIPS/Carrito.zip)