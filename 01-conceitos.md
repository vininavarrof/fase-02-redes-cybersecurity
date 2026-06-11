# 01 - Conceitos de Redes

Este arquivo contém os principais conceitos estudados na Fase 02 - Redes.

---

## 1. Rede

Rede é a comunicação entre dispositivos.

Exemplos:

- Computador conversando com roteador
- Celular acessando a internet
- Máquina virtual acessando um site
- Servidor respondendo uma requisição

Em Cybersecurity, entender redes é importante porque muitos ataques, acessos, serviços e logs passam por comunicação de rede.

---

## 2. IP

IP é o endereço de uma máquina na rede.

Exemplos:

```text
192.168.0.10
10.0.2.15
8.8.8.8
127.0.0.1
```

O IP identifica de onde vem ou para onde vai uma comunicação.

### Exemplo simples

```text
IP da máquina = endereço
Porta = entrada do serviço
Protocolo = regra da comunicação
```

---

## 3. 127.0.0.1

O IP `127.0.0.1` significa a própria máquina.

Também é chamado de `localhost`.

Exemplo:

```bash
ping 127.0.0.1
```

Esse comando testa a comunicação interna da própria máquina.

---

## 4. 0.0.0.0

Quando um serviço escuta em `0.0.0.0`, significa que ele está ouvindo em todas as interfaces de rede disponíveis.

Exemplo:

```text
0.0.0.0:22
```

Isso pode indicar que o SSH está aceitando conexões pela rede.

---

## 5. Porta

A porta identifica o serviço dentro da máquina.

Exemplos:

```text
22   = SSH
53   = DNS
80   = HTTP
443  = HTTPS
3306 = MySQL
5432 = PostgreSQL
```

O IP identifica a máquina.  
A porta identifica o serviço.

Exemplo:

```text
192.168.0.10:22
```

Significa: máquina `192.168.0.10`, serviço na porta `22`.

---

## 6. TCP

TCP é um protocolo de transporte confiável.

Ele cria uma conexão, confirma entrega e organiza os pacotes.

Usado em:

- SSH
- HTTP
- HTTPS
- FTP
- SMTP

Resumo:

```text
TCP = mais confiável, mais controlado, orientado à conexão
```

---

## 7. UDP

UDP é mais rápido, mas não garante entrega da mesma forma que o TCP.

Usado em:

- DNS
- Streaming
- Jogos online
- Chamadas de voz
- Chamadas de vídeo

Resumo:

```text
UDP = mais rápido, mais simples, sem conexão fixa
```

---

## 8. DNS

DNS transforma nomes em IPs.

Exemplo:

```text
google.com -> endereço IP
```

Comandos úteis:

```bash
dig google.com
nslookup google.com
```

Em Segurança da Informação, DNS é importante porque muitos ataques usam domínios falsos, phishing, redirecionamentos e comunicação com servidores maliciosos.

---

## 9. HTTP e HTTPS

HTTP e HTTPS são protocolos usados para acessar sites.

```text
HTTP  = porta 80
HTTPS = porta 443
```

HTTPS usa criptografia, mas isso não significa automaticamente que o site é confiável.

Um site de golpe também pode usar HTTPS.

---

## 10. SSH

SSH é usado para acesso remoto seguro.

Porta comum:

```text
22
```

Exemplo:

```bash
ssh usuario@192.168.0.10
```

Em Segurança, é importante verificar se o SSH está exposto, quem pode acessar e se existem tentativas suspeitas de login.

---

## 11. DHCP

DHCP entrega IP automaticamente para dispositivos na rede.

Exemplo:

```text
Celular entra no Wi-Fi
Roteador entrega um IP automaticamente
```

Sem DHCP, seria necessário configurar IP, máscara, gateway e DNS manualmente.

---

## 12. NAT

NAT permite que vários dispositivos da rede local acessem a internet usando um IP público.

Exemplo:

```text
PC:       192.168.0.10
Celular:  192.168.0.11
TV:       192.168.0.12
```

Para a internet, todos podem sair pelo mesmo IP público.

Em máquinas virtuais, o NAT é muito comum.

---

## 13. Sub-rede

Sub-rede define quais IPs estão no mesmo grupo de rede.

Exemplo:

```text
192.168.0.10/24
```

Normalmente, `/24` indica uma rede como:

```text
192.168.0.1 até 192.168.0.254
```

---

## 14. Gateway

Gateway é a saída da rede local para outras redes.

Geralmente é o roteador.

Comando para ver rota/gateway:

```bash
ip route
```

Exemplo:

```text
default via 192.168.0.1
```

Isso significa que o tráfego para fora da rede vai passar pelo gateway `192.168.0.1`.

---

## 15. Firewall

Firewall controla o que pode entrar e sair da rede ou da máquina.

Ele pode permitir ou bloquear conexões com base em:

- IP
- Porta
- Protocolo
- Origem
- Destino
- Aplicação

Exemplo de ideia:

```text
Permitir porta 22 apenas para IP autorizado
Bloquear porta 3306 para acesso externo
Permitir portas 80 e 443
```

Firewall é uma camada essencial de proteção.
