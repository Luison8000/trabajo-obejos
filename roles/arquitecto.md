

#  Arquitecto 

##  Objetivo
Definir contratos, asegurar integraciones.

---

##  Responsabilidades

1. Definir JSON oficiales
2. Validar reglas globales
3. Diseñar flujo entre servicios
4. Crear diagramas:
   - Secuencia
   - Clases
   - Wireframes UI

---

##  Reglas Globales

 Producto digital ➜ envío SIEMPRE 0.00  
 Producto digital NO puede tener peso  
 Dron solo si peso < 2kg  
 Cascade delete SOLO en ItemsOrden  
 Cliente NO se borra con la orden  

---

## Flujo del Sistema

Usuario  
 API Gateway  
 Servicio Órdenes  
 Servicio Catálogo  
 Servicio Logística  
 Respuesta final

---

##  Contratos Internos

### Órdenes ➜ Catálogo
GET /productos/{id}

### Órdenes ➜ Logística

```json
{
  "tipoProducto": "FISICO",
  "pesoKg": 1.3,
  "direccionDestino": "León, Guanajuato, México"
}
