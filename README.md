# Ejemplo de JWE en Java

Este ejemplo encripta el texto plano "The true sign of intelligence is not knowledge but imagination." para un destinatario utilizando JSON Web Encryption (JWE) en Java.

## Descripción

El proceso implica la creación de un JSON Web Token (JWT) en formato JWE que cifra el texto plano utilizando un algoritmo de cifrado y una clave pública del destinatario.

### Pasos

1. **Encabezado Protegido JWE:**
   - Se declara el encabezado protegido JWE con características específicas.
   - Se codifica en BASE64URL(UTF8(JWE Protected Header)).

2. **Proceso de Encriptación:**
   - Generación de Content Encryption Key (CEK).
   - Encriptación del CEK con la clave pública del destinatario utilizando RSAES-OAEP.
   - Codificación en BASE64URL de la JWE Encrypted Key.
   - Generación de JWE Initialization Vector y codificación en BASE64URL.
   - Establecimiento de datos de cifrado adicionales y realización de un cifrado autenticado en el texto plano utilizando AES GCM.
   - Codificación en BASE64URL del texto cifrado y la etiqueta de autenticación.

### Representación Final del JWE

eyJhbGciOiJSU0EtT0FFUCIsImVuYyI6IkEyNTZHQ00ifQ.
OKOawDo13gRp2ojaHV7LFpZcgV7T6DVZKTyKOMTYUmKoTCVJRgckCL9kiMT03JGe
ipsEdY3mx_etLbbWSrFr05kLzcSr4qKAq7YN7e9jwQRb23nfa6c9d-StnImGyFDb
Sv04uVuxIp5Zms1gNxKKK2Da14B8S4rzVRltdYwam_lDp5XnZAYpQdb76FdIKLaV
mqgfwX7XWRxv2322i-vDxRfqNzo_tETKzpVLzfiwQyeyPGLBIO56YJ7eObdv0je8
1860ppamavo35UgoRdbYaBcoh9QcfylQr66oc6vFWXRcZ_ZT2LawVCWTIy3brGPi
6UklfCpIMfIjf7iGdXKHzg.
48V1_ALb6US04U3b.
5eym8TW_c8SuK0ltJ3rpYIzOeDQz7TALvtu6UG9oMo4vpzs9tX_EFShS8iB7j6ji
SdiwkIr3ajwQzaBtQD_A.
XFBoMYUZodetZdvTiFvSkQ


Consulta la documentación adjunta para detalles completos sobre cómo generar este JWE en Java. Revisa el archivo de implementación en Java disponible en este repositorio para el código detallado.

Para más ejemplos y detalles, consulta la sección de ejemplos adicionales en la documentación.

---

**Nota:** El contenido de este README proporciona una descripción general del proceso. Se recomienda seguir la documentación y el código fuente en el repositorio para obtener instrucciones detalladas y precisas.
