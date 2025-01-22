# api-patentes-chile
Obtiene información de un vehículo a partir de su patente para Chile, utilizando la API de [Boostr Chile](https://api.boostr.cl/).

# Requerimientos
Debes contar con una API KEY gratuita para probar, la puedes obtener en [https://api.boostr.cl/patente](https://api.boostr.cl/patente).

# Documentación
- https://docs.boostr.cl/reference/car-plate

## Ejemplo de uso
El servicio acepta peticiones `GET`, a continuación tienes un ejemplo de uso:

```
curl --request GET \
     --url https://api.boostr.cl/vehicle/BCYT91.json \
     --header 'X-API-KEY: <TU_API_KEY>' \
     --header 'accept: application/json'
```

No olvides reemplazar `<TU_API_KEY>` por el API KEY que te fue entregado.

Con esta simple petición puedes obtener información completa y actualizada del vehículo sólamente utilizando su patente. Imagina todos los casos de usos que puedes dar, integrándola a tus procesos te sirve para validar información ingresada en formularios web, para talleres confirmar información del vehículo y eviter los cientos de errores comunes de tipe (ikmagínate cuando tienes que escribir el VIN), puedes integrarlo a tus cámaras lectores de patente, manejar control de quien ingresa o sale, etc.

## ¿Qué información puedo obtener?
Todo depende del plan que tengas contratado, pero con la versión gratuita ya puedes acceder a un buen pack de información:

- Dígito verificador
- Marca
- Modelo
- Año
- Tipo de vehículo
- Número de motor
- Nombre y RUT del propietario

Pero contratando uno de los planes vigentes, además puedes obtener:

- VIN
- Color
- Tipo de Bencina
- Kilometraje
- Fabricante
- País y región de procedencia
- Cantidad de puertas
- Versión
- Tamaño del motor
- Tipo de transmisión
- Código SII
- Tasación Fiscal

## Otros servicios
Además [https://api.boostr.cl/patente](https://api.boostr.cl/patente) cuenta con más servicios, estos son:

| Servicio                     | Descripción                                                                    | Documentación                                                     |
|------------------------------|--------------------------------------------------------------------------------|-------------------------------------------------------------------|
| Multas                       | Obtiene todas las multas de tránsito directamente desde el Registro Civil      | https://docs.boostr.cl/reference/car-traffic-tickets              |
| Revisión Técnica             | Conoce si el vehículo tiene su revisión técnica al día y el mes debe renovar.  | https://docs.boostr.cl/reference/car-inspection                   |
| Transporte público y escolar | Permite saber si una patente pertenece a una transporte público o bus escolar. | https://docs.boostr.cl/reference/car-public_transportation        |
| SOAP                         | Información sobre el SOAP asociado a la patente.                               | https://docs.boostr.cl/reference/car-soap                         |
| Pasos por pórticos sin TAG   | Evita Multas! Descubre si pasaste por algun pórtico si un TAG vigente.         | https://docs.boostr.cl/reference/car-check_crossings_without_tags |
| Deuda total TAG              | Controla los gastos de tu flota, con tu RUT descubre tu deuda TAG.             | https://docs.boostr.cl/reference/car-tag                          |
