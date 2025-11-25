# **Azure Arc Demo – README**

## 📌 **Descripción**

Este proyecto contiene un **script automatizado** y una **guía de arquitectura** para realizar una demo completa de **Azure Arc** con integración multicloud y gobernanza centralizada mediante **Azure Entra ID**.

Incluye:

*   Onboarding de **servidores Windows/Linux**.
*   Conexión de clústeres **AKS, EKS y GKE**.
*   Configuración de **Azure Policy**, **Log Analytics** y **GitOps (Flux v2)**.
*   Delegación entre tenants con **Azure Lighthouse**.
*   Seguridad con **RBAC** y **Defender for Cloud**.

***

## ✅ **Requisitos Previos**

*   **Azure CLI** instalado:
    ```bash
    curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash
    ```
*   Acceso a:
    *   **Tenant A y Tenant B** (para servidores y AKS).
    *   **Tenant Central** (para políticas y Log Analytics).
    *   Credenciales para **AWS** y **GCP** (para EKS y GKE).
*   Roles:
    *   `Owner` o `Contributor` en las suscripciones.
    *   Permisos para delegación con **Azure Lighthouse**.

***

## ✅ **Arquitectura**

    [Azure Portal]
        ├── Tenant A: Servidor Windows + AKS
        ├── Tenant B: Servidor Linux
        ├── AWS: EKS Cluster
        ├── GCP: GKE Cluster
        └── Tenant Central: Log Analytics + Policy

***

## ✅ **Flujo de la Demo**

1.  **Autenticación y registro de proveedores**.
2.  **Delegación con Azure Lighthouse**.
3.  **Onboarding de servidores** (Windows/Linux).
4.  **Onboarding de clústeres Kubernetes** (AKS, EKS, GKE).
5.  **Aplicación de políticas y RBAC**.
6.  **Creación de Log Analytics Workspace**.
7.  **Configuración de GitOps con Flux v2**.
8.  **Validación y monitorización**.

***

## ✅ **Uso del Script**

1.  Clonar el repositorio:
    ```bash
    git clone <repo-url>
    cd azure-arc-demo
    ```
2.  Dar permisos de ejecución:
    ```bash
    chmod +x azure_arc_demo.sh
    ```
3.  Ejecutar:
    ```bash
    ./azure_arc_demo.sh
    ```

***

## ✅ **Seguridad y Cumplimiento**

*   Activar **MFA** para todas las cuentas.
*   Asignar roles mediante **RBAC**.
*   Habilitar **Defender for Cloud** en todos los recursos.
*   Aplicar **Azure Policy** para baseline de seguridad.

***

## ✅ **Recursos Adicionales**

*   <https://learn.microsoft.com/azure/azure-arc/>
*   <https://learn.microsoft.com/azure/lighthouse/>
*   <https://learn.microsoft.com/azure/azure-arc/kubernetes/conceptual-gitops-flux2>

***

¿Quieres que **genere este README.md directamente como una página interactiva (Page)** para que puedas editarlo y añadir diagramas, o prefieres que lo **exporte junto con el script en un ZIP listo para descargar**?
