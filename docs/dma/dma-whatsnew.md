---
title: Novedades de Data Migration Assistant (SQL Server) | Microsoft Docs
description: Obtenga información sobre las nuevas características de cada versión de Data Migration Assistant para SQL Server y Azure SQL Database.
ms.custom: ''
ms.date: 11/05/2019
ms.prod: sql
ms.prod_service: dma
ms.reviewer: ''
ms.technology: dma
ms.topic: conceptual
keywords: ''
helpviewer_keywords:
- Data Migration Assistant, new features
ms.assetid: ''
author: rajeshsetlem
ms.author: rajpo
ms.openlocfilehash: 11bbf0a39ed9a9bbaa19992f98e4e23d50d6fbe9
ms.sourcegitcommit: c7f40918dc3ecdb0ed2ef5c237a3996cb4cd268d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/05/2020
ms.locfileid: "91727764"
---
# <a name="whats-new-in-data-migration-assistant"></a>Novedades de Data Migration Assistant

En este artículo se enumeran las adiciones en cada versión de Data Migration Assistant.

## <a name="data-migration-assistant-v-52"></a>Data Migration Assistant v 5,2
La versión v 5.2 del Data Migration Assistant proporciona compatibilidad con:
- La carga de evaluaciones en Azure Migrate con compatibilidad con Azure Government y nubes nacionales (oferta soberano).  Esta característica permite evaluar la preparación de SQL Server la migración de datos a Azure SQL.
- Compatibilidad con la línea de comandos para cargar evaluaciones en Azure Migrate con compatibilidad con Azure Government y nubes nacionales.  Ahora puede automatizar completamente la carga de las evaluaciones en el proyecto de Azure Migrate para obtener un informe de disponibilidad consolidado de Azure SQL. 

## <a name="data-migration-assistant-v-50"></a>Data Migration Assistant v 5,0

La versión v 5.0 del Data Migration Assistant proporciona compatibilidad con:

- SQL Server 2019 para Windows y SQL Server 2019 para Linux como destinos para la evaluación y la actualización.
- Guardar y cargar evaluaciones, incluida la compatibilidad para guardar y cargar las evaluaciones creadas en versiones anteriores del Data Migration Assistant.
- Evaluación de proyectos de SQL Server Integration Services (SSIS) hospedados en paquetes SSISDB y SSIS hospedados en el almacén de paquetes. La Migration Assistant de base de datos detecta características no admitidas, parcialmente admitidas o desusadas y problemas de compatibilidad que se usan en los paquetes de origen y proporciona recomendaciones para ayudarle a solucionar esos problemas.
- Evaluar consultas SQL desde una aplicación externa, por ejemplo, consultas SQL en código fuente de C#. Los usuarios pueden usar el kit de herramientas de migración de acceso a datos para generar un informe JSON completo para las consultas SQL usadas en el código fuente de C# y, a continuación, cargar el informe en Data Migration Assistant.

Además, esta versión de Data Migration Assistant proporciona mejoras y correcciones de errores adicionales, y la herramienta se ha actualizado a .net 4.7.2.

## <a name="data-migration-assistant-v45"></a>Data Migration Assistant v 4.5

La versión v 4.5 de Data Migration Assistant proporciona compatibilidad para la evaluación de la migración de paquetes de SQL Server Integration Services (SSIS) hospedados en el sistema de archivos a Azure SQL Database o Instancia administrada de SQL.

## <a name="data-migration-assistant-v44"></a>Data Migration Assistant v 4.4

La versión v 4.4 de Data Migration Assistant proporciona compatibilidad para cargar evaluaciones en Azure Migrate.

## <a name="data-migration-assistant-v43"></a>Data Migration Assistant v 4.3

La versión v 4.3 de Data Migration Assistant proporciona compatibilidad con:

- Recomendaciones de SKU para Azure SQL Instancia administrada basadas en la evaluación de la carga de trabajo.
- RDS SQL Server como origen para las evaluaciones.
- Evaluaciones de trabajos del agente para Azure SQL Instancia administrada como destino.
- La capacidad de omitir determinadas reglas de evaluación; la lista de códigos de error especificada en la propiedad ' ignoreErrorCodes ' configurada en DMA no se mostrará en los resultados de la evaluación de DMA.
- Evaluación de consultas de T-SQL en los pasos de la actividad de trabajo y proporcionar las recomendaciones adecuadas
- Evaluaciones de eventos extendidos (versión preliminar pública).

Además, esta versión de DMA proporciona un rendimiento mejorado para controlar un gran número de objetos de esquema en bases de datos, así como correcciones de errores relacionados con:

- Procedimientos compilados con compilación nativa, en algunos casos.
- Esquemas de base de datos complicados.

## <a name="data-migration-assistant-v42"></a>Data Migration Assistant v 4.2

La versión v 4.2 de Data Migration Assistant proporciona compatibilidad con la línea de comandos para la evaluación de la preparación de destino para una o varias instancias del servidor al migrar de SQL Server local a una Instancia administrada de SQL. Los clientes ahora pueden utilizar la línea de comandos de Data Migration Assistant para recopilar metadatos sobre el esquema de la base de datos, detectar los bloqueadores y obtener información sobre las características parcialmente compatibles o no admitidas que afectan a la migración a una Instancia administrada de SQL. Después, los resultados se pueden representar mediante el Power BI plantilla proporcionada.

## <a name="data-migration-assistant-v41"></a>Data Migration Assistant v 4.1

La versión v 4.1 de Data Migration Assistant incorpora compatibilidad para la evaluación completa de las bases de datos locales de SQL Server que migran a SQL Instancia administrada.

El flujo de trabajo de evaluación le ayuda a detectar los siguientes problemas, lo que puede afectar a la migración a SQL Instancia administrada:

- **Características no admitidas o parcialmente admitidas**. Data Migration Assistant evalúa la base de datos de SQL Server de origen para las características en uso que se admiten parcialmente o no se admiten en el Instancia administrada de SQL de destino. A continuación, la herramienta proporciona un conjunto completo de recomendaciones, enfoques alternativos disponibles en Azure y mitigando los pasos para que los clientes puedan tener en cuenta esta información al planear sus proyectos de migración.

- **Problemas de compatibilidad**. Data Migration Assistant también identifica problemas de compatibilidad relacionados con las siguientes áreas:

  - Cambios importantes: los objetos de esquema específicos que pueden romper la funcionalidad de migración a la base de datos de destino.  Se recomienda corregir estos objetos de esquema después de la migración de la base de datos.
  - Cambios de comportamiento: los objetos de esquema que se indican pueden seguir funcionando, pero pueden presentar un comportamiento diferente, por ejemplo, una degradación del rendimiento.
  - Problemas informativos: estos objetos no afectarán a la migración, pero pueden haber quedado en desuso de las versiones de SQL Server de características.

Una vez completada la evaluación, use nuestro [Azure Database Migration Service](https://azure.microsoft.com/services/database-migration/) (DMS) para realizar la migración de las bases de datos de SQL Server a SQL instancia administrada.  DMS admite migraciones de bases de datos [sin conexión](/azure/dms/tutorial-sql-server-to-managed-instance) (de un solo uso) y [en línea](/azure/dms/tutorial-sql-server-managed-instance-online) (tiempo de inactividad mínimo) a SQL instancia administrada.

## <a name="data-migration-assistant-v40"></a>Data Migration Assistant v 4.0

La versión v 4.0 de Data Migration Assistant presenta la característica de recomendaciones de SKU Azure SQL Database, que permite a los usuarios identificar la SKU de Azure SQL Database mínima recomendada en función de los contadores de rendimiento recopilados de los equipos que hospedan las bases de datos. Esta característica proporciona recomendaciones relacionadas con el plan de tarifa, el nivel de proceso y el tamaño máximo de los datos, así como el costo estimado al mes. También ofrece la posibilidad de aprovisionar todas las bases de datos en Azure de forma masiva.

> [!NOTE]
> Actualmente, esta funcionalidad solo está disponible a través de la interfaz de la línea de comandos (CLI).

Para obtener más información, consulte el artículo [identificación de la SKU de Azure SQL Database adecuada para la base de datos local](dma-sku-recommend-sql-db.md).

## <a name="data-migration-assistant-v36"></a>Data Migration Assistant v 3.6

La versión v 3.6 de Data Migration Assistant presenta "corrección automática" para los objetos de esquema que se ven afectados por los bloqueadores de migración más comunes.

Esta versión proporciona AutoFix para los siguientes problemas de bloqueo de migración y comportamiento:

- Los objetos de esquema que utilizan la sintaxis de combinación incompleta.
- Los objetos de esquema que utilizan la instrucción RAISEERROR heredada.
- Instrucciones SQL que utilizan un literal de tipo order by.

Data Migration Assistant realiza la conversión automática de esquemas para los objetos afectados por los problemas enumerados y solicita confirmación al usuario antes de continuar con la conversión del esquema. Los usuarios pueden revisar los cambios sugeridos en el código y aceptar o rechazar todas las conversiones de cualquier objeto de base de datos determinado.

Data Migration Assistant usa la tecnología de síntesis de programa de Microsoft (PROSE) para sugerir correcciones de código. Más información sobre [PROSE](https://microsoft.github.io/prose/).

## <a name="data-migration-assistant-v35"></a>Data Migration Assistant v 3.5

La versión v 3.5 de Data Migration Assistant incluye las siguientes adiciones:

- Mejoras significativas en el rendimiento para la migración a Azure SQL Database (las pruebas comparativas indican que el proceso es cuatro veces más rápido que con versiones anteriores de Data Migration Assistant).
- La superficie de memoria se optimiza aún más para mejorar la estabilidad del flujo de trabajo de migración.
- La capacidad de omitir las evaluaciones durante el esquema y las migraciones de datos (si ya ha realizado la evaluación y ha solucionado todos los objetos de esquema de interrupción antes de la migración).
- Una corrección para solucionar un problema con la herramienta que se bloquea cuando se proporciona una ruta de acceso de recurso compartido de red no válida para los archivos de copia de seguridad, al realizar una actualización de una versión heredada de SQL Server local a una versión posterior o a SQL Server en máquinas virtuales de Azure.

## <a name="data-migration-assistant-v34"></a>Data Migration Assistant v 3.4

La versión 3.4 de Data Migration Assistant incluye las siguientes adiciones:

- Compatibilidad con SQL Server 2017 como origen para las migraciones a Azure SQL Database.
- Mejoras en la estabilidad, el rendimiento y la corrección de la regla de evaluación.

## <a name="data-migration-assistant-v33"></a>Data Migration Assistant v 3.3

La versión v 3.3 de Data Migration Assistant habilita la migración de una instancia de SQL Server local a la nueva versión de SQL Server 2017, tanto en Windows como en Linux. Aunque el flujo de trabajo general de migración para Windows y Linux es el mismo, el cambio a SQL Server 2017 para Linux requiere un par de consideraciones adicionales.

### <a name="specifying-the-back-up-path"></a>Especificación de la ruta de acceso de copia de seguridad

Linux y Windows usan distintos formatos de ruta de acceso. Como resultado, la migración a SQL Server 2017 en Linux requiere que el usuario proporcione las versiones de Windows y Linux de la ruta de acceso a la ubicación del archivo físico. Puede proporcionar ambas versiones de la ruta de acceso de maneras diferentes, en función de la ubicación del archivo físico.
Si el archivo de copia de seguridad físico se encuentra en un equipo que ejecuta:

- Linux, use un recurso compartido de "Samba" para compartir el archivo con otros equipos de la red.
- Windows, use el comando ' mnt ' para montar el recurso compartido en el equipo que ejecuta Linux.

> [!NOTE]
> Los detalles sobre el uso de un recurso compartido de "Samba" o el comando "mnt" quedan fuera del ámbito de este artículo.

### <a name="migrating-windows-logins"></a>Migrar inicios de sesión de Windows

Aunque la migración de inicios de sesión de Active Directory (AD) es oficialmente compatible con SQL Server 2017 en Linux, requiere una configuración adicional para funcionar correctamente. Consulte el artículo [Active Directory la autenticación con SQL Server en Linux](../linux/sql-server-linux-active-directory-authentication.md) para obtener información detallada sobre la configuración de inicios de sesión de Active Directory en SQL Server 2017 en Linux. Después de realizar la configuración necesaria, se completa la instalación y puede migrar los inicios de sesión de Active Directory como de costumbre. La autenticación de SQL estándar funciona según lo previsto sin necesidad de ninguna configuración adicional.

## <a name="data-migration-assistant-v32"></a>Data Migration Assistant v 3.2

La versión v 3.2 de Data Migration Assistant incluye las siguientes adiciones:

- La migración de esquemas y datos se habilita desde las bases de datos locales de SQL Server para Azure SQL Database con un nuevo flujo de trabajo de migración.
- Durante la migración de esquemas a Azure SQL Database, los scripts de DMA de los objetos de base de datos de origen proporcionan instrucciones sobre cómo corregir los posibles problemas de compatibilidad y, a continuación, se implementa el esquema en Azure.

## <a name="data-migration-assistant-v31"></a>Data Migration Assistant v 3.1

La versión v 3.1 de Data Migration Assistant incluye las siguientes adiciones:

- Recomendaciones de evaluación mejoradas para Azure SQL Database en cuanto a las intercalaciones de base de datos, el uso de procedimientos almacenados del sistema no admitidos y objetos CLR.
- Instrucciones de evaluación de los niveles de compatibilidad 130, 120, 110 y 100 al migrar a Azure SQL Database.

## <a name="data-migration-assistant-v30"></a>Data Migration Assistant v 3.0

La versión v 3.0 de Data Migration Assistant amplía la evaluación de Azure SQL Database para proporcionar recomendaciones completas que le ayuden a solucionar problemas relacionados con:

- Problemas de bloqueo de la migración.
- Características y funciones parciales o no admitidas.

## <a name="data-migration-assistant-v21"></a>Data Migration Assistant v 2.1

La versión v 2.1 de Data Migration Assistant incluye las siguientes adiciones:

- Compatibilidad de la línea de comandos para ejecutar evaluaciones en modo desatendido, lo que ayuda a ejecutar evaluaciones a escala. Para obtener detalles adicionales, consulte el artículo [ejecución de Data Migration Assistant desde la línea de comandos](dma-commandline.md).
- Mejoras de rendimiento cuando los usuarios inician y cierran DMA.
- La capacidad de configurar el tiempo de espera de conexión SQL. Para obtener detalles adicionales, consulte los [valores de configuración del artículo para obtener Data Migration Assistant](dma-configurationsettings.md).

## <a name="data-migration-assistant-v20"></a>Data Migration Assistant v 2.0

La versión v 2.0 de Data Migration Assistant incluye recomendaciones de características de stretch Database mejoradas para proporcionar tablas con prioridades adecuadas que maximicen el ahorro de almacenamiento.

## <a name="data-migration-assistant-v10"></a>Data Migration Assistant v 1.0

La versión v 1.0 de Data Migration Assistant es la versión inicial y proporciona:

- Detección de problemas que pueden afectar a una actualización a una versión local de SQL Server. Los hallazgos se describen como problemas de compatibilidad y se clasifican en las siguientes áreas:
  - Últimos cambios
  - Cambios de comportamiento
  - Características en desuso
- Detección de nuevas características en la plataforma de SQL Server de destino en la que se puede beneficiar la base de datos después de una actualización. Los hallazgos se describen como recomendaciones de características y se clasifican en las siguientes áreas:
  - Rendimiento
  - Seguridad
  - Storage
- Experiencia de usuario moderna para realizar evaluaciones.

## <a name="see-also"></a>Consulte también

[Información general de Data Migration Assistant](../dma/dma-overview.md)