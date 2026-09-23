# Requerimientos y observaciones del sistema

## 1. Base de datos de insumos

- **Importar base de datos:** agregar un botón para importar una base de datos general que el cliente quizás ya tenga construida en Excel o en su programa anterior. Sin esta opción, el usuario tiene que registrar todo a mano.
- **Confirmación al guardar:** al crear un insumo o al abrir uno existente para modificarlo, el botón **Guardar** no muestra ninguna alerta que confirme el guardado.

## 2. Receta estándar

- **Búsqueda de insumos:** al crear la receta estándar y agregar los insumos del producto, aparece una lista desplegable. Lo ideal sería poder **buscar el producto** o **digitar el código interno**.
- **Filtrar el listado:** en ese listado no deberían aparecer los platos ya configurados, **solo los insumos**.

## 3. SKU

- Los SKU deben ser **numéricos**, **incrementarse automáticamente** y **no repetirse**.
- Esta regla aplica para **todos los productos**.

## 4. Base de datos de productos

### 4.1 Tipos de producto

Debe haber dos tipos de producto:

| Tipo | Descripción | Ejemplos |
|------|-------------|----------|
| **Receta** | Platos preparados para la venta | Platos del menú |
| **Producto terminado** | Productos que no se preparan pero se venden al cliente | Gaseosas, cerveza, licor, agua, refrescos |

> **Problema actual:** hoy todo producto nuevo se crea como receta, pero no todos los productos son recetas.

### 4.2 Crear producto

- Al pulsar **Agregar producto**, se debe poder elegir entre **Crear producto** o **Crear receta**.
- Falta el campo **Código de barras** para los productos terminados (gaseosas, licores, agua, etc.).

### 4.3 Importación

- Agregar un botón **Importar** para subir la base de datos si el cliente ya la tiene.
- Ofrecer una **plantilla descargable** con los campos de la base de datos del programa, para que el archivo importado los respete.

### 4.4 Impuestos (IVA e Impoconsumo)

- El IVA y el Impoconsumo deben ir en **campos separados** que contengan la misma información:
  - **Impuesto a cargo** (obligatorio)
  - **Impuesto a cargo 2** (opcional)
- Motivo: algunos productos se venden con IVA y otros con Impoconsumo.

## 5. Categorías

Para diferenciar los productos terminados de los insumos **sin crear dos bases de datos**, se propone asignar los productos a categorías:

- Agregar la opción de **crear categorías**.
- Al crear un producto, elegir la categoría ya creada desde una **lista desplegable**, para no escribir nombres repetidos.

## 6. Registro de compras

### Preguntas

1. ¿Se pueden agregar el **NIT** y el **nombre del proveedor** al registrar las compras de insumos?

### Requerimientos

- El registro de compras también debe permitir registrar los **productos terminados** (agua, gaseosa, etc.), y esas compras deben **sumarse al inventario disponible para la venta**.
- ¿Se puede pasar el registro de compras a un **formulario**?
- Los registros de compra deben poder **modificarse** para corregir errores.

---

## Resumen de pendientes

- [ ] Botón para importar la base de datos de insumos
- [ ] Alerta de confirmación al guardar insumos (crear y editar)
- [ ] Buscador por nombre o código interno en la receta estándar
- [ ] Mostrar solo insumos (no platos) en la receta estándar
- [ ] SKU numérico, autoincremental y único para todos los productos
- [ ] Dos tipos de producto: Receta y Producto terminado
- [ ] Opción "Crear producto" / "Crear receta" al agregar producto
- [ ] Campo de código de barras para productos terminados
- [ ] Botón para importar productos + plantilla descargable
- [ ] Campos separados: Impuesto a cargo e Impuesto a cargo 2 (opcional)
- [ ] Gestión de categorías con selección por lista desplegable
- [ ] NIT y nombre del proveedor en compras
- [ ] Compras de productos terminados que alimenten el inventario de venta
- [ ] Registro de compras mediante formulario
- [ ] Edición de registros de compra
