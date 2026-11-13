---
titulo: "Fabricación de Contramolde, Molde de Silicón y Figura de Yeso"
autor: "Andrea Paola Carmona Casiano"
---

# Fabricación de Contramolde, Molde de Silicón y Figura de Yeso

## Introducción
En esta práctica se describe el proceso completo de diseño y fabricación de un contramolde impreso en resina 3D, la elaboración de un molde de caucho de silicón a partir de dicho contramolde y, finalmente, la colada y acabado de piezas finales en yeso ("Patitos").

---

## 1. Fabricación del Contramolde

### 1.1 Modelo Base
El punto de partida fue el modelo tridimensional de la pieza base a reproducir.

![Patito og](./img_moldes/contramolde/patito_og.jpeg){ width=35% }

### 1.2 Modelado 3D en SolidWorks
1. **Conversión a Sólido:** Se descargó el modelo original en formato `.STL` y se importó en SolidWorks como objeto gráfico. Posterior a ello, se convirtió la malla a un cuerpo sólido editable.
2. **Diseño de la Caja de Contención:** Se generó el volumen cúbico exterior que servirá como contención para la colada de silicón.
3. **Mecanismo de Alineación (Pivotes/Bolitas):** Para asegurar que las dos mitades del contramolde encajen perfectamente sin desalineaciones, se añadieron ensambles de posicionamiento geométrico. Una mitad cuenta con salientes esféricas (machos) y la otra con sus contrapartes removidas/hundidas (hembras).

![Solid 1](./img_moldes/contramolde/solid_1.jpeg){ width=35% }
![Solid 2](./img_moldes/contramolde/solid_2.jpeg){ width=35% }


### 1.3 Acondicionamiento e Impresión en Bambu Lab Studio
Se exportaron los archivos desde SolidWorks en formato `.STL` para su preparación dimensional y de posición:

1. **Ajuste de Escala y Orientación:** Se importó el archivo base sin escalar para definir el tamaño adecuado y recostarlo sobre el plano de trabajo.
   
![Bambu Lab no escala](./img_moldes/contramolde/escala.jpeg){ width=35% }
![Bambu Lan escala](./img_moldes/contramolde/no%20escala.jpeg){ width=35% }

2. **Aplicación de Espejeado (Mirror):** En SolidWorks, ambas piezas del contramolde fueron creadas orientadas hacia el mismo sentido. Para lograr el ensamble de caras opuestas (izquierda y derecha), se aplicó la herramienta de espejeado (*Mirror*) dentro del software de preparación. Una vez alineados correctamente hacia sentidos opuestos, se exportó cada componente por separado haciendo clic derecho > *Exportar como STL*.

![Espejeado](./img_moldes/contramolde/espejeado.jpeg){ width=35% }

---

### 1.4 Preparación en Software para Impresión de Resina
Los archivos `.STL` espejeados se pasaron al software slicer específico para la impresora de resina **Sonic XL 2022 4K de Phrozen**.

> **Nota de Aclaración:** Las siguientes imágenes de visualización muestran el modelo previo a la corrección del espejeado. Dicho detalle se detectó y corrigió antes de la impresión final, por lo que las piezas se imprimieron correctamente y ensamblaron a la perfección.

#### Fundamentos del Posicionamiento y Angulación en Resina
En las impresoras 3D de resina (SLA/DLP), la impresión se realiza capa por capa jalando la pieza desde la película de la cubeta (FEP). Para minimizar la presión de succión (efecto ventosa) sobre la pieza y reducir marcas gruesas de soportes:
- Se orientaron las piezas a un ángulo aproximado sobre el plano (ajustado al tanteo).
- Se configuró una altura de elevación de soporte de **4 mm**.

![Plataforma 1](./img_moldes/contramolde/plataforma_1.jpeg){ width=35% }
![Plataforma 2](./img_moldes/contramolde/plataforma_2.jpeg){ width=35% }
![Plataforma 3](./img_moldes/contramolde/plataforma_3.jpeg){ width=35% }
![Plataforma 4](./img_moldes/contramolde/plataforma_4.jpeg){ width=35% }

---

### 1.5 Preparación del Material e Impresora 3D

1. **Configuración de Parámetros:**
   - La impresora **Sonic XL 2022 4K** se precalentó a una temperatura controlada de **30 °C**.
   - Se transfirió el archivo cortado a la impresora mediante una memoria USB a través del menú `Print File`.

![Impresora](./img_moldes/contramolde/impresora.jpeg){ width=35% }
![Impresora abierta](./img_moldes/contramolde/impresora_abier.jpeg){ width=35% } <br>

[*Programacion de la impresora*](./img_moldes/contramolde/programar_impresora.mp4) <br>

2. **Carga de Resina:**
   - Se utilizó resina **JAYO Water Washable Standard Solid Gray**.
   - Se vertió el sobrante del contenedor y se agitó ligeramente para eliminar posibles grumos o sedimentación antes del arranque.

![Resina 1](./img_moldes/contramolde/resina_1.jpeg){ width=35% }
![Resina 2](./img_moldes/contramolde/resina_2.jpeg){ width=35% }
![Resina 3](./img_moldes/contramolde/resina_3.jpeg){ width=35% }

---

### 1.6 Impresión y Limpieza (Lavado)
El tiempo total estimado de impresión fue de aproximadamente 4 a 5 horas debido al tamaño compacto de la pieza.

![Impreso 1](./img_moldes/contramolde/impreso_1.jpeg){ width=35% }
![Impreso 2](./img_moldes/contramolde/impreso_2.jpeg){ width=35% }
![Impreso 3](./img_moldes/contramolde/impreso_3.jpeg){ width=35% }
![Impreso 4](./img_moldes/contramolde/impreso_4.jpeg){ width=35% }

#### Proceso de Lavado
Las piezas recién impresas contienen resina líquida sin curar en la superficie, la cual es tóxica e irritante. Por ello, deben someterse a un baño en lavadora ultrasónica o de agitación.

- **Solución utilizada:** Alcohol Isopropílico concentrado.
- **Procedimiento:** Se sumergieron las piezas y se programó el ciclo de lavado.


![Lavado 1](./img_moldes/contramolde/lavado_1.jpeg){ width=35% }
![Lavado 2](./img_moldes/contramolde/lavado_1.jpeg){ width=35% } <br>

[*Lavado de las piezazs*](./img_moldes/contramolde/washing.mp4) <br>


---

### 1.7 Post-procesado: Retiro de Soportes, Lijado y Curado

1. **Retiro de Soportes:** Con el uso obligatorio de guantes de protección, se retiraron manualmente las estructuras de soporte asistidas con herramientas cortantes.

![Soportes 1](./img_moldes/contramolde/soportes_1.jpeg){ width=35% }
![Soportes 2](./img_moldes/contramolde/soportes_2.jpeg){ width=35% }
![Sin soportes](./img_moldes/contramolde/sin_soportes.jpeg){ width=35% }

2. **Lijado Exterior:** Debido a la adherencia de los soportes, la cara inferior presentó rugosidad. Se utilizó una **lima/lija al agua** para aplanar la superficie externa. Dado que esta zona corresponde únicamente a la carcasa exterior del contramolde, la textura rugosa no compromete la geometría interior del molde final.

3. **Curado UV:**
   - Las piezas se introdujeron en la cámara de curado **Elegoo Mercury / Infinity**.
   - Se aplicó luz ultravioleta durante **10 minutos** para polimerizar la resina completamente, eliminar la sensación pegajosa y lograr la rigidez mecánica final necesaria para sostener la colada de silicón.

![Curado 1](./img_moldes/contramolde/curado_1.jpeg){ width=35% }
![Curado 2](./img_moldes/contramolde/curado_2.jpeg){ width=35% }
![Curado 3](./img_moldes/contramolde/curando.jpeg){ width=35% }
![Contramolde](./img_moldes/contramolde/contramolde.jpeg){ width=35% }

---

## 2. Fabricación del Molde de Caucho de Silicón

### 2.1 Cálculo del Volumen de Mezcla
Para determinar el volumen requerido dentro de las cavidades del contramolde:
1. Se llenó la cavidad del contramolde con agua hasta el nivel máximo.
2. Se vertió el agua en un vaso medidor y se marcó la altura alcanzada.

### 2.2 Preparación del Silicón y Catalizado
Para obtener la flexibilidad adecuada y evitar imperfecciones por viscosidad:
1. **Base de Silicón:** Se utilizó caucho de silicón que equivalía al **80%** del volumen total calculado.
2. **Diluyente:** Se añadió un **20% de diluyente para silicón** para reducir la viscosidad de la mezcla, permitiendo que el material fluya por todos los detalles del contramolde y libere atrapamientos de aire fácilmente.
3. **Catalización:** Una vez homogenizada la mezcla sin presencia de burbujas visibles, se integró el catalizador a la proporción indicada por el fabricante para activar la vulcanización. <br>

**Materiales** <br>
![Silicon](./img_moldes/molde/silicon.jpeg){ width=35% }
![Diluyente](./img_moldes/molde/diluyente_silicon.jpeg){ width=35% }
![Catalizador](./img_moldes/molde/catalizador.jpeg){ width=35% } <br>

**Proceso** <br>
![Mezcla 1](./img_moldes/molde/mezcla_1.jpeg){ width=35% }
![Mezcla 2](./img_moldes/molde/mezcla_2.jpeg){ width=35% } <br>

**Molde** <br>
![Molde](./img_moldes/molde/molde.jpeg){ width=35% }
---

## 3. Fabricación de la Figura de Yeso

### 3.1 Proporciones y Dosificación
Para la elaboración del producto final se utilizó **Yeso tipo MDC Dental**:
- **Yeso:** 50 gramos (pesados en báscula digital).
- **Agua:** 10 mililitros.

![Desengrasante](./img_moldes/figura/desengrasante.jpeg){ width=35% }
![Yeso](./img_moldes/figura/yeso.jpeg){ width=35% }

### 3.2 Acondicionamiento del Molde
Se aplicó sobre las cavidades internas del molde un **spray desengrasante eliminador de tensión superficial**. Este producto rompe la tensión del fluido permitiendo que la mezcla de yeso moje completamente la superficie del silicón y prevenga la formación de microburbujas en los relieves de la cara de la figura.

### 3.3 Mezclado y Colada de Yeso
1. **Mezclado al Vacío:** La mezcla de agua y yeso se procesó en una **mezcladora al vacío** por **1 minuto**, eliminando por completo los oclusiones de aire internas.
2. **Detallado Inicial:** Con ayuda de una espátula pequeña, se aplicó yeso en los detalles finos y grietas pequeñas del molde abierto antes de cerrarlo.
3. **Cierre y Vibración:** Se ensamblaron las dos mitades del molde sujetándolas con **3 ligas elásticas** para garantizar una presión constante. El llenado final se realizó sobre una **mesa vibradora de laboratorio**, permitiendo expulsar las burbujas residuales hacia la superficie superior durante el vertido.

![Cosas](./img_moldes/figura/cosas.jpeg){ width=35% } <br>

[*Mezcladora al vacio*](./img_moldes/figura/mezcla.mp4) <br>

![Proceso 1](./img_moldes/figura/proceso_1.jpeg){ width=35% }
![Proceso 2](./img_moldes/figura/proceso_2.jpeg){ width=35% }

### 3.4 Desmolde y Acabado Final
Al desmoldar, las piezas de yeso recién fraguadas presentaban pequeñas rebabas en la línea de partición y diminutas oclusiones.

- **Detallado y Retoque:** Con una herramienta de pulido de grano fino se rebajaron las imperfecciones y se pulieron los bordes.
- Se fabricaron un total de **5 patitos de yeso**, logrando un acabado liso, uniforme y sin presencia de cavidades por aire.

![Casi final](./img_moldes/figura/casi_final.jpeg){ width=35% } <br>
![Final](./img_moldes/figura/final.jpeg){ width=35% }

[**Descargar Archivos del Contramolde (.ZIP)**](./ZIPS/Contramolde.zip)
