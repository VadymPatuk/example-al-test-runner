name: 🌟 Solicitar nueva característica
description: Reportar un fallo relacionado con funcionamiento de app
labels: [ "Nueva caracteristica"]
body:
  - type: textarea
    id: request-text
    attributes:
      label: Descripción breve de solicitud
      description: Proporciona una descripción clara y concisa del fallo
    validations:
      required: true
  - type: textarea
    id: expected-behavior
    attributes:
      label: Comportamiento esperado
      description: Proporciona una descripción clara y concisa de lo que esperabas que ocurriera.
    validations:
      required: false
  - type: dropdown
    id: module
    attributes:
      label: Módulos afectados
      description: Seleccione módulos afectados
      multiple: true
      options:
        - Báscula
        - Fichero
        - Impresora
        - Repetidor
        - FTP
    validations:
      required: false      
  - type: textarea
    id: steps-reproduce
    attributes:
      label: Pasos para reproducir
      description: Pasos para reproducir el comportamiento
      placeholder: |
        1. Ir a '...'
        2. Hacer clic en '....'
        3. Desplazarse hacia '....'
        4. Ver error
    validations:
      required: true
  - type: input
    id: wintc-version
    attributes:
      label: Versión de app
      description: Indica versión de app
      placeholder: "24.11.24.687"
    validations:
      required: true
  - type: input
    id: os-version
    attributes:
      label: Versión de Windows
      placeholder: "Windows 11"
    validations:
      required: true
  - type: input
    id: customer
    attributes:
      label: Nombre del cliente donde ha ocurrido error
      description: Indique 0 si es interno (LIDER).
      placeholder: "Sport Lifestyle"
    validations:
      required: true
  - type: textarea
    id: stacktrace
    attributes:
      label: Log de error "Stack trace"
      description: Copia trazablidad si dispone de log error registrado en **Visor de eventos**
      render: shell
    validations:
      required: false      
