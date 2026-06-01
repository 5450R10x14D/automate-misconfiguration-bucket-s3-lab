# exploit_misconfiguration_bucket_s3_lab
Script PoC en python3 que automatiza la explotación de una máquina de vulnmachine.com, una plataforma de aprendizaje de ciberseguridad

# Exploit PoC: VulnMachines S3 Misconfiguration
Automatizar la explotación de una mala configuración en un bucket de Amazon S3 dentro del laboratorio de **[misconfiguration bucket]**, permitiendo el acceso inicial al entorno.

---

## Requisitos e Instalación
### 1. Se requiere crear una cuenta en AWS
Regístrese o inicie sesión en la consola oficial de AWS

Vaya al servicio **IAM** (Identity and Access Management) para crear un usuario o acceda a su usuario actual

Asigne permisos (police) **AmazonS3ReadOnlyAccess**, luego en la pestaña "security credentials" generar el **Access Key ID** y **Secret Access Key**

### 2. Entorno virtual
Recomiendo crear un entorno virtual e instalar las herramientas y dependencias dentro del entorno

```bash
sudo apt install -y python3-virtualenv
```

```bash
virtualenv venv
```

```bash
source venv/bin/activate
```

```bash
pip install colorama
```

```bash
pip install awscli
```

### 3. Configurar AWS CLI
Ejecute el comando aws configure en su terminal para vincular sus credenciales

```bash
aws configure
```

Ingresar el Access Key ID, Secret Access Key, la región de AWS (ej: us-east-1) y el formato de salida (ej: json)

Cambiar el nombre de usuario "default" por el nombre de usuario IAM creado anteriormente editando el archivo ~/.aws/credentials y ~/.aws/configure

verifique la conexión con aws sts get-caller-identity.

```bash
aws sts get-caller-identity
```

---

## Modo de Uso

```bash
python3 PoC_exploit.py
```


