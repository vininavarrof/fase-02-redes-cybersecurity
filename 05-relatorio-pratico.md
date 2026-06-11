# 05 - Relatório Prático - Fase 02 Redes

Este é um modelo de relatório para registrar os testes feitos no laboratório.

---

## 1. Objetivo

O objetivo deste laboratório foi praticar comandos básicos de redes no Linux e entender conceitos como IP, rota, gateway, DNS, portas abertas, serviços e captura de tráfego.

---

## 2. Ambiente

```text
Sistema:
Máquina virtual:
Modo de rede:
Data do teste:
```

Exemplo:

```text
Sistema: Ubuntu Linux
Máquina virtual: VirtualBox
Modo de rede: NAT
Data do teste: preencher
```

---

## 3. Identificação do IP

Comando utilizado:

```bash
ip a
```

Resultado observado:

```text
Preencher aqui o IP encontrado
```

Interpretação:

```text
A máquina recebeu um endereço IP na interface de rede.
Esse IP identifica a máquina dentro da rede atual.
```

---

## 4. Verificação de rota e gateway

Comando utilizado:

```bash
ip route
```

Resultado observado:

```text
Preencher aqui a rota padrão e gateway
```

Interpretação:

```text
O gateway é a saída usada pela máquina para acessar outras redes, como a internet.
```

---

## 5. Teste de conectividade

Comando utilizado:

```bash
ping 8.8.8.8
```

Resultado observado:

```text
Preencher se respondeu ou não respondeu
```

Interpretação:

```text
Se houve resposta, a máquina possui conectividade com a internet usando IP.
```

---

## 6. Teste de DNS

Comandos utilizados:

```bash
ping google.com
dig google.com
nslookup google.com
```

Resultado observado:

```text
Preencher resultado
```

Interpretação:

```text
Se o nome google.com foi resolvido para um IP, o DNS está funcionando.
```

---

## 7. Teste HTTP/HTTPS

Comando utilizado:

```bash
curl -I https://google.com
```

Resultado observado:

```text
Preencher código HTTP e informações principais
```

Interpretação:

```text
O comando curl mostrou que a máquina conseguiu fazer uma requisição HTTPS.
```

---

## 8. Portas abertas

Comando utilizado:

```bash
ss -tulpn
```

Resultado observado:

```text
Preencher portas encontradas
```

Interpretação:

```text
As portas em LISTEN indicam serviços aguardando conexões.
```

---

## 9. Varredura local com nmap

Comando utilizado:

```bash
nmap 127.0.0.1
```

Resultado observado:

```text
Preencher portas encontradas
```

Interpretação:

```text
O nmap mostrou quais portas estavam abertas na própria máquina.
```

---

## 10. Captura de tráfego

Comando utilizado:

```bash
sudo tcpdump -i any
```

Resultado observado:

```text
Preencher tráfego observado
```

Interpretação:

```text
Foi possível visualizar pacotes passando pela máquina, como DNS, ICMP, HTTP ou HTTPS.
```

---

## 11. Conclusão

Neste laboratório, pratiquei comandos básicos de redes no Linux e entendi melhor como uma máquina se comunica.

Principais aprendizados:

- IP identifica a máquina
- Porta identifica o serviço
- DNS transforma nome em IP
- Gateway é a saída da rede
- TCP e UDP transportam dados
- Portas abertas indicam serviços expostos
- Ferramentas como ss, nmap e tcpdump ajudam na análise de rede

Esse conhecimento é essencial para evoluir em Segurança da Informação, SOC, Blue Team e Pentest em laboratório.
