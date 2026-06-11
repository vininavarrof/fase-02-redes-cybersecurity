# 02 - Comandos de Redes no Linux

Este arquivo reúne os comandos praticados na Fase 02 - Redes.

---

## 1. Ver IP da máquina

```bash
ip a
```

Esse comando mostra as interfaces de rede e os IPs configurados.

O que observar:

```text
lo        = interface local
enp0s3    = interface de rede da VM
inet      = endereço IPv4
```

---

## 2. Ver rotas e gateway

```bash
ip route
```

Exemplo de saída:

```text
default via 192.168.0.1 dev wlan0
```

Interpretação:

```text
default = rota padrão
via     = por onde o tráfego sai
dev     = interface usada
```

---

## 3. Testar conectividade

```bash
ping 8.8.8.8
```

Testa conexão com um IP externo.

```bash
ping google.com
```

Testa conexão usando DNS.

Se `ping 8.8.8.8` funciona, mas `ping google.com` não funciona, pode haver problema de DNS.

---

## 4. Ver caminho até um destino

```bash
traceroute google.com
```

Mostra os saltos até o destino.

Caso não tenha instalado:

```bash
sudo apt install traceroute -y
```

---

## 5. Consultar DNS com dig

```bash
dig google.com
```

Mostra informações DNS do domínio.

---

## 6. Consultar DNS com nslookup

```bash
nslookup google.com
```

Também consulta resolução de nomes.

---

## 7. Fazer requisição HTTP/HTTPS com curl

```bash
curl https://example.com
```

Mostra o conteúdo retornado pelo site.

Para ver apenas os cabeçalhos:

```bash
curl -I https://example.com
```

Códigos importantes:

```text
200 = OK
301 = Redirecionamento permanente
302 = Redirecionamento temporário
403 = Proibido
404 = Não encontrado
500 = Erro interno do servidor
```

---

## 8. Ver portas abertas e serviços

```bash
ss -tulpn
```

O que significa:

```text
-t = TCP
-u = UDP
-l = LISTEN
-p = processo
-n = não resolver nomes
```

Exemplo:

```text
tcp LISTEN 0 128 0.0.0.0:22
```

Interpretação:

```text
Existe um serviço escutando na porta 22 em todas as interfaces.
```

---

## 9. Ver serviço SSH

```bash
systemctl status ssh
```

Iniciar SSH:

```bash
sudo systemctl start ssh
```

Ativar SSH na inicialização:

```bash
sudo systemctl enable ssh
```

---

## 10. Mapear portas com nmap

Use apenas em laboratório próprio ou ambiente autorizado.

```bash
nmap 127.0.0.1
```

Também é possível testar o IP da própria VM:

```bash
nmap IP_DA_SUA_VM
```

Exemplo:

```bash
nmap 10.0.2.15
```

---

## 11. Capturar tráfego com tcpdump

```bash
sudo tcpdump -i any
```

Capturar DNS:

```bash
sudo tcpdump -i any port 53
```

Capturar HTTP/HTTPS:

```bash
sudo tcpdump -i any port 80 or port 443
```

---

## 12. Comandos para repetir e fixar

```bash
ip a
ip route
ping 8.8.8.8
ping google.com
dig google.com
nslookup google.com
curl -I https://google.com
ss -tulpn
nmap 127.0.0.1
sudo tcpdump -i any
```

---

## 13. Perguntas para treinar interpretação

Depois de rodar os comandos, tentar responder:

1. Qual é o IP da minha máquina?
2. Qual é meu gateway?
3. Minha máquina está resolvendo DNS?
4. Quais portas estão abertas?
5. Algum serviço está escutando em `0.0.0.0`?
6. Algum serviço está escutando apenas em `127.0.0.1`?
7. O que o `nmap` encontrou?
8. Que tráfego apareceu no `tcpdump`?
