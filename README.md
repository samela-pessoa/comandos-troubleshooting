# Comandos para Troubleshooting

Este documento contém uma lista de comandos úteis para diagnosticar e resolver problemas em diferentes áreas, como redes, sistema operacional, aplicações, banco de dados e nuvem. Use esta referência para solucionar problemas de forma eficiente.

---

## **1. Redes**
### **1.1 Diagnóstico de Conexões**
- **Verificar conectividade com um host (ping):**
  ```bash
  ping <endereço IP ou domínio>
  ```
- **Rastrear rota até um host (traceroute/tracert):**
  - Linux:
    ```bash
    traceroute <endereço IP ou domínio>
    ```
  - Windows:
    ```cmd
    tracert <endereço IP ou domínio>
    ```
- **Exibir tabelas de roteamento:**
  - Linux:
    ```bash
    route -n
    ```
  - Windows:
    ```cmd
    route print
    ```

### **1.2 Teste de Portas**
- **Verificar portas abertas em um host (nmap):**
  ```bash
  nmap -p <porta> <endereço IP>
  ```
- **Checar se uma porta está escutando (telnet):**
  ```bash
  telnet <endereço IP> <porta>
  ```
- **Teste de portas com netcat:**
  ```bash
  nc -zv <endereço IP> <porta>
  ```
- **Debug de URLs com curl:**
  ```bash
  curl -I <URL>
  ```
- **Testar requisição HTTP:**
  ```bash
  curl -X GET <URL> -H "Authorization: Bearer <token>"
  ```
---

## **2. Sistema Operacional**
### **2.1 Uso de Recursos**
- **Monitorar uso de CPU e memória:**
  - Linux:
    ```bash
    top
    ```
  - Windows:
    ```cmd
    tasklist
    ```
- **Listar processos em execução:**
  - Linux:
    ```bash
    ps aux
    ```
  - Windows:
    ```cmd
    tasklist
    ```

### **2.2 Logs do Sistema**
- **Visualizar logs do sistema:**
  - Linux:
    ```bash
    tail -f /var/log/syslog
    ```
  - Windows:
    - Acessar o Visualizador de Eventos:
      ```cmd
      eventvwr
      ```

---

## **3. Aplicações**
### **3.1 Serviços**
- **Verificar status de serviços:**
  - Linux:
    ```bash
    systemctl status <nome_do_serviço>
    ```
  - Windows:
    ```cmd
    sc query <nome_do_serviço>
    ```

- **Iniciar ou parar serviços:**
  - Linux:
    ```bash
    systemctl start|stop <nome_do_serviço>
    ```
  - Windows:
    ```cmd
    net start|stop <nome_do_serviço>
    ```

### **3.2 Rede de Aplicações**
- **Verificar conexões ativas:**
  - Linux:
    ```bash
    netstat -tunlp
    ```
  - Windows:
    ```cmd
    netstat -ano
    ```
---

Este README serve como um guia de referência rápida. Adicione mais comandos conforme necessário para se adequar aos seus cenários de troubleshooting!
