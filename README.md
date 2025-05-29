✅ Contenido sugerido para README.md
markdown
Copiar
Editar
# ⛵ ansible-helm-install-k3s

Automatiza la instalación de Helm en el nodo controlador del clúster K3s utilizando Ansible.

Este playbook descarga e instala la versión deseada de Helm desde el sitio oficial, verificando que esté correctamente ubicado en `/usr/local/bin/helm`.

---

## 📦 Características

- Instala **Helm v3.17.3** (puedes cambiar la versión fácilmente).
- Automatización con **Ansible**.
- Instalación local en `localhost` o nodo controlador remoto.
- Compatible con cualquier distribución Linux.

---

## 🔧 Requisitos

- Ansible ≥ 2.10
- Acceso `sudo` en el nodo donde se ejecuta el playbook
- Conectividad a Internet

---

## 📁 Estructura

ansible-helm-install-k3s/
├── inventory/
│ └── hosts.ini
├── playbooks/
│ └── install_helm.yml

yaml
Copiar
Editar

---

## 🚀 Uso

### 1. Clonar el repositorio

```bash
git clone https://github.com/vhgalvez/ansible-helm-install-k3s.git
cd ansible-helm-install-k3s
2. Revisar el inventario
Asegúrate de tener configurado correctamente el archivo inventory/hosts.ini. Ejemplo para localhost:

ini
Copiar
Editar
[localhost]
127.0.0.1 ansible_connection=local
3. Ejecutar el playbook
bash
Copiar
Editar
sudo ansible-playbook -i inventory/hosts.ini playbooks/install_helm.yml
✅ Resultado esperado
El binario helm se instalará en:

bash
Copiar
Editar
/usr/local/bin/helm
Puedes verificarlo con:

bash
Copiar
Editar
helm version
🧠 Autor
Víctor Hugo Gálvez – GitHub

📄 Licencia
Este proyecto está licenciado bajo la MIT License

⭐️ ¿Te fue útil?
¡Dale una estrella al repositorio para apoyar el proyecto!