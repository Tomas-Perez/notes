# TP2

Aplicación de gestión de ventas y stock

Nuevas vías de venta, no solo sucursales

Módulo persona: totalmente independiente, reutilizable en nuevos proyectos  

Catálogo de productos para realizar una venta. Más funcionalidad a futuro.

- Combos, con precio especial
- Productos virtuales, sin stock físico

Stock manejado en distintos depósitos

Sugerencias a partir de un producto en concreto, de productos que pueden interesar comprar.

Categorías de productos.

El cliente puede comprar y elegir distintos tipos de retiro:

- En sucursal
- Envío a domicilio

Historial de compras para cada usuario

Factura de venta

Ticket de entrega de mercadería

Estado de facturación de la empresa

A futuro se desea realizar reportes:

- Por zona de venta
- Por vendedor
- Por fecha o rangos de fecha
- Por medios de pago
- Por tipo de operación
- etc

## Modulos

1. Catálogo
2. Facturación
3. Stock
4. Compras
5. Persona
6. Sugerencias

### Datos requeridos de productos por módulo

CatalogItem(Product, Description, Category)  
Category(ID, Name)  
Combo(Item[])  
SingleProduct(Product)  
CatalogEntry(Item, Price)
Product(Name, ID)

1. Catálogo: SingleProduct, Category, Combo (Name, ID, Price, Description, Category)
2. Facturación: SingleProduct, Combo, CatalogEntry (Name, ID, ID_Catalog, Price)
3. Stock: SingleProduct (Name, ID)
4. Compras: Product, SingleProduct, Combo, CatalogEntry (Name, ID, Price)
5. Persona
6. Sugerencias: SingleProduct, Category (Name, Category, ID)