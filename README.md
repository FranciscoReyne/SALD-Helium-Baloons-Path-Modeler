# SALD-Helium-Baloons-Path-Modeler


<p align="center">
  
<img src="img.jpeg"  width="400"/>

</p>

Sistema para modelar en 3D el trayecto de un globo meteorológico con carga variable en Chile.

Para un sistema de modelado de trayectoria de globos meteorológicos de helio con carga pesada (300 kg), necesitarás:

## Herramientas recomendadas

1. **Software de modelado físico y simulación**:
   - **MATLAB/Simulink**: Excelente para modelado matemático de la aerodinámica
   - **Python** con bibliotecas científicas:
     - NumPy/SciPy para cálculos
     - Matplotlib/Plotly para visualización
     - PyTorch/TensorFlow si deseas incorporar aprendizaje automático

2. **Datos geoespaciales y meteorológicos**:
   - **GDAL/OGR** para procesamiento de datos geoespaciales
   - API de **Copernicus** o **ECMWF** para datos meteorológicos actualizados
   - **NASA POWER** para datos de radiación solar
   - **CR2** (Centro de Ciencia del Clima y la Resiliencia) para datos específicos de Chile

3. **Modelado 3D y visualización**:
   - **Cesium.js** o **Google Earth Engine** para visualización 3D sobre terreno real
   - **Blender** para visualizaciones de alta calidad (no tiempo real)
   - **Unity3D** o **Unreal Engine** si necesitas una interfaz interactiva

## Modelado recomendado

Para un modelado efectivo, recomendaría un enfoque por capas:

1. **Modelado físico base**:
   - Ecuaciones de sustentación para el globo considerando el volumen de helio
   - Efectos de la carga de 300 kg (variable) en la dinámica
   - Efectos de temperatura en la densidad del helio a diferentes altitudes

2. **Integración de datos meteorológicos**:
   - Modelado de vientos en diferentes capas atmosféricas de Chile
   - Consideración de corrientes de aire características de la geografía chilena (efecto cordillera)
   - Incorporación de gradientes térmicos verticales

3. **Características geográficas de Chile**:
   - Modelado del terreno (Cordillera de los Andes, valle central, costa)
   - Zonas de restricción de vuelo
   - Áreas pobladas para análisis de riesgo



-----------------------

# Disponibilidad de datos geoespaciales y meteorológicos Chile - modelado de trayectoria de globos meteorológicos:

## Datos Meteorológicos para Chile

1. **Centro de Ciencia del Clima y la Resiliencia (CR2)**
   - Disponibilidad: Alta
   - Ofrece series de tiempo históricas de temperatura, precipitación y viento para Chile
   - Acceso: Datos abiertos a través de su portal web (cr2.cl)
   - Resolución espacial: Variable, generalmente por estaciones meteorológicas

2. **Dirección Meteorológica de Chile (DMC)**
   - Disponibilidad: Alta
   - Proporciona datos meteorológicos actuales e históricos
   - Acceso: Algunos datos gratuitos, otros requieren suscripción
   - Resolución temporal: Horaria y diaria

3. **ERA5 (ECMWF)**
   - Disponibilidad: Alta
   - Reanálisis global que incluye Chile con excelente calidad
   - Datos de viento, temperatura, presión y humedad a múltiples niveles de altitud
   - Acceso: Gratuito a través de Copernicus Climate Data Store
   - Resolución espacial: 0.25° x 0.25° (aproximadamente 25-30 km)
   - Resolución vertical: 137 niveles desde superficie hasta 80 km de altura
   - Particularmente relevante para modelado de trayectoria de globos

4. **MERRA-2 (NASA)**
   - Disponibilidad: Alta
   - Reanálisis atmosférico global con buena cobertura de Chile
   - Acceso: Gratuito a través de NASA GES DISC
   - Resolución espacial: 0.5° x 0.625°

5. **Global Forecast System (GFS)**
   - Disponibilidad: Alta, actualizada 4 veces al día
   - Pronósticos globales útiles para planificación de lanzamientos
   - Acceso: Gratuito a través de NOAA
   - Resolución espacial: 0.25° (aproximadamente 25 km)
   - Resolución temporal: Hasta 16 días con intervalos de 3 horas

## Datos Geoespaciales para Chile

1. **IDE Chile (Infraestructura de Datos Geoespaciales)**
   - Disponibilidad: Alta
   - Plataforma oficial de datos geoespaciales de Chile
   - Incluye modelos digitales de elevación, límites administrativos, hidrografía
   - Acceso: Mayoritariamente gratuito

2. **SRTM (Shuttle Radar Topography Mission)**
   - Disponibilidad: Alta
   - Modelo de elevación digital global que cubre todo Chile
   - Acceso: Gratuito
   - Resolución espacial: 30m para Chile

3. **ASTER GDEM**
   - Disponibilidad: Alta
   - Modelo de elevación digital global con buena cobertura para Chile
   - Acceso: Gratuito
   - Resolución espacial: 30m

4. **Datos CONAF (Corporación Nacional Forestal)**
   - Disponibilidad: Media
   - Información sobre cobertura vegetal y áreas protegidas
   - Útil para identificar zonas de riesgo o restricción

## Consideraciones para tu proyecto

1. **Particularidades de Chile relevantes para modelado de globos**:
   - La presencia de la Cordillera de los Andes crea patrones de viento complejos
   - Existe gran variabilidad climática de norte a sur (desde desierto hasta zona austral)
   - Las corrientes en altura pueden ser significativamente diferentes a las superficiales

2. **Integraciones recomendadas**:
   - Combinar ERA5 para datos de viento en altura con modelos digitales de elevación SRTM
   - Utilizar datos de la DMC para validación de modelos en puntos específicos
   - Incorporar pronósticos GFS para planificación de lanzamientos

3. **APIs y servicios de acceso**:
   - Copernicus Climate Data Store API (para ERA5)
   - Python packages como xarray y netCDF4 para procesamiento de datos meteorológicos
   - GDAL/OGR para procesamiento de datos geoespaciales


SALUDOS :D !
