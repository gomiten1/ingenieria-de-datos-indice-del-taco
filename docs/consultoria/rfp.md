Equipo 2   
\# RFP:  El índice del Taco

**Cliente**: La TaquerIA Opus  
**Contacto**: Doña Ofelia Ruvalcaba, dueña \[[ofeliatumbada123@gmail.com](mailto:ofeliatumbada123@gmail.com)\]

**Equipo redactor**: 

* Arredondo Granados Gerardo — \[rol, ej. líder de proyecto\]   
*  García Ortega Fernanda — \[rol, ej. ingeniería de datos\]  
*  López Estrada Carlos — \[rol, ej. infraestructura y seguridad\]   
* Martínez Jiménez Alejandro — \[rol, ej. calidad de datos\]  
*   Ospino Mérida Emilio Sebastián — \[rol, ej. análisis y dashboard\] 

**Fecha de publicación**: 06/10/2026 

 **1\. Quiénes somos**  
\[3 a 5 líneas sobre el negocio: qué vendemos, dónde, cuántas personas somos.\]  
Somos La TaquerIA Opus, una taquería tradicional ubicada en la Ciudad de México especializada en tacos de suadero y pastor. Nuestro equipo consta de 5 personas operativas, atendiendo a decenas de clientes diariamente. Nos dedicamos a vender alimentos de alta calidad, pero actualmente enfrentamos fluctuaciones constantes en los precios de nuestros insumos sin claridad de si corresponden a la realidad del mercado. 

**2\. El problema**  
\[Qué nos duele hoy y qué pasa si no lo resolvemos. Usen las palabras del cliente.\]  
*"Mire, joven, yo lo que quiero saber es si me están viendo la cara. Don Beto me subió como un 30% este año y me dice que es porque todo subió. Y la verdad yo no sé si es cierto. Las otras taqueras de la cuadra me dicen que a ellas no les ha subido tanto, pero a lo mejor compran otra calidad... Con las recetas calculo mis costos, pero ya no me cuadra nada"*.

Actualmente llevamos las cuentas al tanteo y con cuentas en libreta que no nos dan certeza. Hace poco intentamos revisar esto con una ayuda externa, pero el cálculo se rompió y nos quedamos durante dos meses usando números desactualizados sin que nadie se diera cuenta.

Si no resolvemos esto, corremos el riesgo de fijar precios equivocados en la carta, perder dinero en cada taco que vendemos o pagarle de más a nuestros proveedores sin saberlo.

**3\. Qué necesitamos lograr**  
| |N1 | Saber cuánto cuesta cada taco (suadero y pastor) cada semana | Costo por taco en pesos y como índice base 100, disponible antes del lunes 9 am, en al menos 95% de las semanas.

| | N2 | Saber si el proveedor cobra caro o barato | Para cada insumo, diferencia en % contra el precio de mayoreo (SNIIM) y de menudeo (PROFECO), actualizada cada semana.  
 | | N3 | Saber qué insumo explica el aumento de costos | Ranking de insumos según cuánto aportaron al cambio del costo en el último trimestre; los 3 principales se muestran con su % de aportación.

 | | N4 | Comparar nuestro costo con la inflación | Gráfica del Índice del Taco contra la inflación general y la de alimentos (INEGI), con la misma base 100\.

| | N5 | Que nada falle en silencio | Si la actualización semanal falla o un dato es sospechoso, llega un correo de aviso en menos de 1 hora y queda registrado.

| | N6 | Poder confiar en los números | Los datos con errores se apartan y se reportan en lugar de usarse; cualquier semana se puede volver a calcular desde los datos originales con el mismo resultado.

 | | N7 | Entenderlo sin ser experta | Doña Ofelia responde las 4 preguntas del problema leyendo el tablero, sin ayuda, en menos de 5 minutos (prueba con el cliente).

| | N8 | Que otros negocios lo puedan usar | Otro negocio de comida puede usarlo cambiando solo su receta y precios de proveedor, siguiendo una guía escrita.

**4\. Qué NO queremos en este proyecto**

\- Un sistema de punto de venta, inventarios o facturación.   
\- Predicción de precios futuros o recomendaciones automáticas de precio de venta. \- Compras o negociación automática con el proveedor.   
\- Información en tiempo real: una actualización semanal es suficiente.  
 \- Otros tacos, otros productos u otras ciudades (solo suadero y pastor en la CDMX).  
 \- Una app móvil propia.   
\- Leer automáticamente nuestros chats de WhatsApp. 

**5\. Datos que tenemos y datos que faltan**

| Dato | Formato hoy | Confiabilidad |
| ----- | ----- | ----- |
| Precios del proveedor | Mensajes de WhatsApp, sin formato fijo, con unidades mezcladas (kilo, pieza, paquete) | Baja: hay errores de captura y cambios sin aviso |
| Receta estándar (gramos de carne, tortillas, salsa, etc. por taco) | En papel / de memoria \[ajustar\] | Media: varía según quién prepara |
| Ventas | Libreta o caja \[ajustar\] | Media |

Para este proyecto se usarán datos internos sintéticos, generados de forma reproducible, que imiten estos formatos.

**Datos públicos a usar:** PROFECO (precios al menudeo), SNIIM (precios de mayoreo en centrales de abasto), INEGI (inflación general y de alimentos) y Banxico (indicadores económicos de apoyo).

**Dudas:**

* ¿Cada fuente se publica cuando dice y siempre en el mismo formato?  
* ¿Los productos públicos corresponden a nuestros insumos? (ej. "suadero" o "carne al pastor" pueden no aparecer tal cual y habrá que usar el corte más parecido).  
* ¿Cómo convertir todas las unidades a una sola (kilo, pieza) sin errores?  
* ¿Qué hacer cuando una fuente se retrasa o trae huecos?

**6\. Restricciones**

* **Presupuesto máximo:** \$\[monto\] MXN \[ajustar\]  
* **Plazo:** entrega final el \[dd/mm/2026\], fin del semestre \[ajustar\]  
* **Costo de operación mensual máximo:** \$300 MXN en la nube \[ajustar\], con alertas de gasto desde el primer día  
* **Seguridad y privacidad:** no pueden quedar expuestos nuestras ventas, el nombre y teléfono del proveedor, sus mensajes ni nuestros precios de compra exactos. El tablero público solo muestra índices y comparaciones. Cada parte del sistema solo debe tener los permisos que necesita.  
* **Quién lo va a usar:** Doña Ofelia, sin conocimientos técnicos; usa principalmente el celular y el correo.  
* **Otras restricciones:**  
  * Debe funcionar en AWS y sin servidores encendidos todo el tiempo.  
  * Toda la infraestructura debe poder volver a crearse automáticamente (infraestructura como código).  
  * Correr el proceso dos veces sobre la misma semana no debe duplicar ni alterar resultados.

**7\. Qué esperamos recibir**

* Un tablero de control (Dashboard) público y simple que le responda a Doña Ofelia cuánto cuesta producir cada taco y si su proveedor está caro o barato.  
* Un sistema automático e independiente (Pipeline Batch Serverless) que procese los datos cada semana sin intervención humana.  
* Mecanismo de alertas por correo que avise de inmediato si algo falla o si los precios vienen con errores.  
* Infraestructura como código (Terraform) para poder recrear todo el sistema con un solo comando.  
* Documentación de negocio y técnica clara: Repositorio en GitHub con README, Diccionario de Datos, Registros de Decisiones de Arquitectura (ADRs), Manual de Operación (Runbook) y Reporte de Costos

**8\. Cómo evaluaremos las propuestas**

| Criterio | Peso (suma 100\) |
| ----- | ----- |
| Responde a nuestras necesidades (N1 a N8) | 30 |
| Calidad del plan y tiempos | 20 |
| Manejo de riesgos (fuentes caídas, datos malos, fallas) | 15 |
| Costo total y costo de operación mensual | 15 |
| Claridad para un usuario no técnico | 10 |
| Facilidad para replicarlo en otro negocio | 10 |

**9\. Qué debe incluir su propuesta**

* SOW con alcance y fuera de alcance explícitos.  
* Calendario con entregas parciales y fechas.  
* Equipo propuesto y rol de cada integrante.  
* Supuestos (ej. disponibilidad de las fuentes públicas, equivalencia de productos).  
* Riesgos identificados y cómo los mitigarán.  
* Precio total y estimación del costo mensual de operación.  
* Cómo demostrarán que se cumple cada necesidad de la sección 3\.

**10\. Calendario del proceso**

* Fecha límite para preguntas: 10/10/2026   
* Fecha límite para entregar propuestas: 16/10/2026   
* Fecha de decisión: 20/10/2026 