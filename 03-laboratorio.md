# 03 - Laboratório Prático de Redes

Este arquivo descreve um laboratório simples para praticar redes no Linux.

---

## Ambiente usado

Exemplo de ambiente:

```text
Sistema principal: Windows
Virtualização: VirtualBox
Máquina virtual: Ubuntu Linux
Rede da VM: NAT ou Bridge
Objetivo: praticar comandos de rede de forma segura
```

---

## Etapa 1 - Identificar IP da VM

Comando:

```bash
ip a
```

Anotar:

```text
Interface:
IP:
Máscara:
```

Exemplo:

```text
Interface: enp0s3
IP: 10.0.2.15
Máscara: /24
```

---

## Etapa 2 - Ver rota padrão

Comando:

```bash
ip route
```

Anotar:

```text
Gateway:
Interface usada:
```

Exemplo:

```text
default via 10.0.2.2 dev enp0s3
```

---

## Etapa 3 - Testar internet por IP

Comando:

```bash
ping 8.8.8.8
```

Resultado esperado:

```text
Receber respostas do IP 8.8.8.8
```

Se funcionar, existe conectividade com a internet.

---

## Etapa 4 - Testar DNS

Comando:

```bash
ping google.com
```

Se funcionar, a máquina está resolvendo nomes.

Também testar:

```bash
dig google.com
nslookup google.com
```

---

## Etapa 5 - Testar HTTP/HTTPS

Comando:

```bash
curl -I https://google.com
```

Observar:

```text
Código HTTP
Servidor
Redirecionamentos
Tipo de conteúdo
```

---

## Etapa 6 - Ver portas abertas

Comando:

```bash
ss -tulpn
```

Anotar:

```text
Porta:
Protocolo:
Endereço local:
Processo:
```

Exemplo:

```text
Porta: 22
Protocolo: TCP
Endereço: 0.0.0.0
Serviço: SSH
```

---

## Etapa 7 - Mapear a própria máquina

Comando:

```bash
nmap 127.0.0.1
```

Depois, testar o IP da VM:

```bash
nmap IP_DA_VM
```

Exemplo:

```bash
nmap 10.0.2.15
```

Anotar as portas encontradas.

---

## Etapa 8 - Capturar tráfego

Comando:

```bash
sudo tcpdump -i any
```

Em outro terminal, executar:

```bash
ping google.com
curl -I https://google.com
dig google.com
```

Observar no `tcpdump`:

```text
IP de origem
IP de destino
Porta
Protocolo
Tipo de tráfego
```

---

## Etapa 9 - Desenhar a rede

Modelo:

```text
[Meu PC Windows]
        |
        | VirtualBox
        |
[VM Ubuntu - 10.0.2.15]
        |
        | Gateway/NAT - 10.0.2.2
        |
[Internet]
        |
[google.com]
```

---

## Etapa 10 - Conclusão do laboratório

Responder:

1. Qual IP minha VM recebeu?
2. Qual é o gateway?
3. O DNS funcionou?
4. Quais portas estavam abertas?
5. Algum serviço estava exposto?
6. O `nmap` mostrou o mesmo que o `ss`?
7. O `tcpdump` mostrou tráfego de DNS, ping ou HTTPS?
8. O que eu aprendi com esse teste?
