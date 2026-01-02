# Proyecto Aurelion - Documentación

## 1. Tema
Este proyecto se basa en el análisis de datos provenientes de la Tienda Aurelion, un establecimiento ubicado en la provincia de Buenos Aires, dedicado a la venta de productos diversos.
El objetivo es identificar posibles problemáticas o patrones relevantes dentro de los datos, que permitan obtener información útil para la toma de decisiones.

---

## 2. Problema
Durante los primeros cuatro meses del año se observa una disminución significativa en las ventas, tanto en el monto total como en la cantidad de productos vendidos.
A partir del quinto mes, las ventas muestran un repunte considerable, lo que sugiere que esta caída inicial podría estar relacionada con factores estacionales o cambios en la demanda de ciertos productos según la época del año.

---

## 3. Solución
Implementar una estrategia de marketing por estación del año, con el objetivo de:
- Aumentar las ventas en los períodos de menor actividad.
- Promover productos con baja rotación durante los meses de menor demanda.
- Optimizar las inversiones publicitarias según el comportamiento de compra del cliente.
Para ello, se realizará un análisis de datos que permita identificar los productos más y menos vendidos en cada período.
El proceso se llevará a cabo mediante:
- Python, para la carga, limpieza y análisis exploratorio de los datos (ventas, productos y clientes).
- Power BI, para la visualización interactiva y la toma de decisiones informadas en base a métricas y tendencias.

---

## 4. Dataset de referencia
### Fuente:
Datos de ventas diarias de la **Tienda Aurelion**.

---

### Definición:
Conjunto de datos en formato Excel donde se lleva el registro correspondiente de clientes, productos y ventas.  

---

### Estructura, tipos y escala
 
#### Tabla: clientes
| Campo             | Tipo | Escala    |
|-------------------|------|-----------|
| id_cliente        | int  | Nominal   |
| nombres_apellidos | str  | Nominal   |
| email             | str  | Nominal   |
| ciudad            | str  | Nominal   |
| fecha_registro    | date | Intervalo |

#### Tabla: productos
| Campo           | Tipo | Escala  |
|-----------------|------|---------|
| id_producto     | int  | Nominal |
| nombre_producto | str  | Nominal |
| categoria       | str  | Nominal |
| precio_unitario | dec  | Razón   |

#### Tabla: ventas
| Campo       | Tipo | Escala    |
|-------------|------|-----------|
| id_venta    | int  | Nominal   |
| fecha_venta | date | Intervalo |
| id_cliente  | int  | Nominal   |
| medio_pago  | str  | Nominal   |

#### Tabla: detalle_ventas
| Campo           | Tipo | Escala  |
|-----------------|------|---------|
| id_venta        | int  | Nominal |
| id_producto     | int  | Nominal |
| cantidad        | int  | Razón   |
| precio_unitario | dec  | Razón   |
| importe         | dec  | Razón   |

---

## 5. Información, pasos, pseudocódigo y diagrama del programa

### Información del Programa
El programa en Python mostrará un menú interactivo en consola para consultar el contenido del archivo documentacion.md.

---

### Pasos y Pseudocódigo del Programa
	
INICIO

tema = 'Este proyecto se basa en el análisis de datos provenientes de la Tienda Aurelion, un establecimiento ubicado en la provincia de Buenos Aires, dedicado a la venta de productos diversos. El objetivo es identificar posibles problemáticas o patrones relevantes dentro de los datos,  que permitan obtener información útil para la toma de decisiones.'

problema = 'Durante los primeros cuatro meses del año se observa una disminución significativa en las ventas, tanto en el monto total como en la cantidad de productos vendidos. A partir del quinto mes, las ventas muestran un repunte considerable,  lo que sugiere que esta caída inicial podría estar relacionada con factores estacionales  o cambios en la demanda de ciertos productos según la época del año.'

solucion= 'Implementar una estrategia de marketing por estación del año, con el objetivo de:
- Aumentar las ventas en los períodos de menor actividad.
- Promover productos con baja rotación durante los meses de menor demanda.
- Optimizar las inversiones publicitarias según el comportamiento de compra del cliente.

Para ello, se realizará un análisis de datos que permita identificar los productos más 
y menos vendidos en cada período.

El proceso se llevará a cabo mediante:

- Python, para la carga, limpieza y análisis exploratorio de los datos (ventas, productos y clientes).
- Power BI, para la visualización interactiva y la toma de decisiones informadas en base a métricas 
y tendencias.'

fuente_de_datos = 'Datos de ventas diarias de la Tienda Aurelion.'

definicion_de_datos = 'Conjunto de datos en formato Excel con registros de clientes, productos y ventas.'

estructura_fuente_de_datos ='
ESTRUCTURA, TIPOS Y ESCALA DE LA FUENTE DE DATOS:

Tabla: clientes
| Campo             | Tipo | Escala    |
|-------------------|------|-----------|
| id_cliente        | int  | Nominal   |
| nombres_apellidos | str  | Nominal   |
| email             | str  | Nominal   |
| ciudad            | str  | Nominal   |
| fecha_registro    | date | Intervalo |

 Tabla: productos
| Campo           | Tipo | Escala  |
|-----------------|------|---------|
| id_producto     | int  | Nominal |
| nombre_producto | str  | Nominal |
| categoria       | str  | Nominal |
| precio_unitario | dec  | Razón   |

Tabla: ventas
| Campo       | Tipo | Escala    |
|-------------|------|-----------|
| id_venta    | int  | Nominal   |
| fecha_venta | date | Intervalo |
| id_cliente  | int  | Nominal   |
| medio_pago  | str  | Nominal   |

Tabla: detalle_ventas
| Campo           | Tipo | Escala  |
|-----------------|------|---------|
| id_venta        | int  | Nominal |
| id_producto     | int  | Nominal |
| cantidad        | int  | Razón   |
| precio_unitario | dec  | Razón   |
| importe         | dec  | Razón   |

'

informacion_del_programa ='El programa en Python mostrará un menú interactivo en consola  para consultar el contenido del archivo documentacion.md.'

pasos_y_pseudocodigo_del_programa = '

INICIO

tema = 'Este proyecto se basa en el análisis de datos provenientes de la Tienda Aurelion, un establecimiento ubicado en la provincia de Buenos Aires, dedicado a la venta de productos diversos. El objetivo es identificar posibles problemáticas o patrones relevantes dentro de los datos,  que permitan obtener información útil para la toma de decisiones.'

problema = 'Durante los primeros cuatro meses del año se observa una disminución significativa en las ventas, tanto en el monto total como en la cantidad de productos vendidos. A partir del quinto mes, las ventas muestran un repunte considerable,  lo que sugiere que esta caída inicial podría estar relacionada con factores estacionales  o cambios en la demanda de ciertos productos según la época del año.'

solucion= 'Implementar una estrategia de marketing por estación del año, con el objetivo de:
- Aumentar las ventas en los períodos de menor actividad.
- Promover productos con baja rotación durante los meses de menor demanda.
- Optimizar las inversiones publicitarias según el comportamiento de compra del cliente.

Para ello, se realizará un análisis de datos que permita identificar los productos más 
y menos vendidos en cada período.

El proceso se llevará a cabo mediante:

- Python, para la carga, limpieza y análisis exploratorio de los datos (ventas, productos y clientes).
- Power BI, para la visualización interactiva y la toma de decisiones informadas en base a métricas 
y tendencias.'

fuente_de_datos = 'Datos de ventas diarias de la Tienda Aurelion.'

definicion_de_datos = 'Conjunto de datos en formato Excel con registros de clientes, productos y ventas.'

estructura_fuente_de_datos ='
ESTRUCTURA, TIPOS Y ESCALA DE LA FUENTE DE DATOS:

Tabla: clientes
| Campo             | Tipo | Escala    |
|-------------------|------|-----------|
| id_cliente        | int  | Nominal   |
| nombres_apellidos | str  | Nominal   |
| email             | str  | Nominal   |
| ciudad            | str  | Nominal   |
| fecha_registro    | date | Intervalo |

 Tabla: productos
| Campo           | Tipo | Escala  |
|-----------------|------|---------|
| id_producto     | int  | Nominal |
| nombre_producto | str  | Nominal |
| categoria       | str  | Nominal |
| precio_unitario | dec  | Razón   |

Tabla: ventas
| Campo       | Tipo | Escala    |
|-------------|------|-----------|
| id_venta    | int  | Nominal   |
| fecha_venta | date | Intervalo |
| id_cliente  | int  | Nominal   |
| medio_pago  | str  | Nominal   |

Tabla: detalle_ventas
| Campo           | Tipo | Escala  |
|-----------------|------|---------|
| id_venta        | int  | Nominal |
| id_producto     | int  | Nominal |
| cantidad        | int  | Razón   |
| precio_unitario | dec  | Razón   |
| importe         | dec  | Razón   |

'

informacion_del_programa ='El programa en Python mostrará un menú interactivo en consola  para consultar el contenido del archivo documentacion.md.'

pasos_y_pseudocodigo_del_programa = '

'

diagrama_de_flujo_del_programa = 'El diagarma de flujo lo puede visualizar accediendo a la imagen llamada “ Menu_Interactivo_Tienda_Aurelion.png”'

lista_de_opciones_validas=["1","2","3","4","5","6","7","8","9","10"]

opciones_menu_interactivo = '
=== ¡BIENVENIDO AL MENÚ INTERACTIVO! ===
Seleccione una opción para ver la información correspondiente:
1. Ver Tema
2. Ver Problema
3. Ver Solución
4. Ver Fuente de Datos
5. Ver Definición de Datos
6. Ver Estructura, tipos y Escala de los Datos
7. Ver Información del Programa
8. Ver Pasos y Pseudocódigo del Programa
9. Ver Diagrama de Flujo del Programa
10. Salir
'

Repetir hasta que opcion == 10
 	Escribir opciones_menu_interactivo
 	Leer opción
 		Si opción in lista_de_opciones_validas
 			Si opcion=1 Entonces
 				Escribir tema
 			SiNo
 				Si opcion=2 Entonces
 					Escribir problema
 				SiNo
 					Si opcion=3 Entonces
 						Escribir solucion
 					SiNo
 						Si opcion=4 Entonces
 							Escribir fuente_de_datos
 						SiNo
 							Si opcion=5 Entonces
 								Escribir definicion_de_datos
 							SiNo
 								Si opcion=6 Entonces
 									Escribir estructura_fuente_de_datos
 								SiNo
 									Si opcion=7 Entonces
 										Escribir informacion_del_programa
 									SiNo
 										Si opcion=8 Entonces
 											Escribir pasos_y_pseudocodigo_del_programa
 										SiNo
 											Si opcion=9 Entonces
 												Escribir diagrama_de_flujo_del_programa
 											SiNo
 												Si opcion=10 Entonces
 													Escribir 'Saliendo del sistema... ¡Gracias por usar Tienda Aurelion!'
 												SiNo
 													Escribir 'Opción no válida. Debe ingresar un número del 1 al 10.'
 												FinSi
 											FinSi
 										FinSi
 									FinSi
 								FinSi
 							FinSi
 						FinSi
 					FinSi
 				FinSi
 			FinSi
 		SiNo
 			Escribir ‘Opción no válida. Debe ingresar un número del 1 al 10.'
 		FinSi


'

diagrama_de_flujo_del_programa = 'El diagarma de flujo lo puede visualizar accediendo a la imagen llamada “ Menu_Interactivo_Tienda_Aurelion.png”'

lista_de_opciones_validas=["1","2","3","4","5","6","7","8","9","10"]

opciones_menu_interactivo = '
=== ¡BIENVENIDO AL MENÚ INTERACTIVO! ===
Seleccione una opción para ver la información correspondiente:
1. Ver Tema
2. Ver Problema
3. Ver Solución
4. Ver Fuente de Datos
5. Ver Definición de Datos
6. Ver Estructura, tipos y Escala de los Datos
7. Ver Información del Programa
8. Ver Pasos y Pseudocódigo del Programa
9. Ver Diagrama de Flujo del Programa
10. Salir
'

Repetir hasta que opcion == 10
	Escribir opciones_menu_interactivo
	Leer opción
		Si opción in lista_de_opciones_validas
			Si opcion=1 Entonces
				Escribir tema
			SiNo
				Si opcion=2 Entonces
					Escribir problema
				SiNo
					Si opcion=3 Entonces
						Escribir solucion
					SiNo
						Si opcion=4 Entonces
							Escribir fuente_de_datos
						SiNo
							Si opcion=5 Entonces
								Escribir definicion_de_datos
							SiNo
								Si opcion=6 Entonces
									Escribir estructura_fuente_de_datos
								SiNo
									Si opcion=7 Entonces
										Escribir informacion_del_programa
									SiNo
										Si opcion=8 Entonces
											Escribir pasos_y_pseudocodigo_del_programa
										SiNo
											Si opcion=9 Entonces
												Escribir diagrama_de_flujo_del_programa
											SiNo
												Si opcion=10 Entonces
													Escribir 'Saliendo del sistema... ¡Gracias por usar Tienda Aurelion!'
												SiNo
													Escribir 'Opción no válida. Debe ingresar un número del 1 al 10.'
												FinSi
											FinSi
										FinSi
									FinSi
								FinSi
							FinSi
						FinSi
					FinSi
				FinSi
			FinSi
		SiNo 
			Escribir ‘Opción no válida. Debe ingresar un número del 1 al 10.'
		FinSi


---

### Diagrama de Flujo del Programa

El diagrama representa el flujo general del programa, y puede ser visualizado en la imagen llamada “Menu_Interactivo_Tienda_Aurelion.png”
