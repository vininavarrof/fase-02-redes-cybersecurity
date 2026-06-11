# Fase 02 - Redes para Cybersecurity

Este repositório registra meus estudos da **Fase 02 - Redes**, dentro da minha trilha de aprendizado em **Cybersecurity**.

Depois de estudar fundamentos de Linux e terminal, avancei para redes de computadores, entendendo como máquinas se comunicam, como serviços ficam disponíveis e como analisar conexões de forma prática.

---

## Objetivo da fase

O objetivo desta fase é entender os principais fundamentos de redes usados em Segurança da Informação, Blue Team, SOC e Pentest em laboratório.

Nesta etapa estudei:

- IP
- Portas
- TCP e UDP
- DNS
- HTTP e HTTPS
- SSH
- DHCP
- NAT
- Sub-redes
- Firewall
- Comandos básicos de diagnóstico de rede no Linux

---

## O que aprendi

Aprendi que rede não é apenas "internet funcionando".

Por trás de cada site acessado, conexão remota ou serviço aberto, existem vários elementos trabalhando juntos:

```text
IP -> Rota -> Gateway -> DNS -> Porta -> Protocolo -> Serviço -> Resposta
```

Também entendi que, na área de Cybersecurity, redes são fundamentais para identificar:

- Serviços expostos
- Portas abertas
- Tráfego suspeito
- Falhas de configuração
- Caminhos de comunicação
- Possíveis pontos de ataque
- Regras de firewall
- Comportamento de máquinas na rede

---

## Comandos praticados

Alguns comandos estudados nesta fase:

```bash
ip a
ip route
ping
traceroute
dig
nslookup
curl
ss -tulpn
nmap
tcpdump
```

Esses comandos ajudam a verificar IPs, rotas, DNS, portas abertas, serviços ativos e tráfego de rede.

---

## Estrutura do repositório

```text
fase-02-redes-cybersecurity/
│
├── README.md
├── docs/
│   ├── 01-conceitos.md
│   ├── 02-comandos.md
│   ├── 03-laboratorio.md
│   ├── 04-checklist.md
│   └── 05-relatorio-pratico.md
│
├── assets/
│   └── diagrama-rede-lab.md
│
├── .gitignore
└── LICENSE
```

---

## Observação ética

Todos os comandos e testes deste repositório devem ser praticados apenas em:

- Meu próprio computador
- Minha máquina virtual
- Minha rede local autorizada
- Laboratórios de estudo
- Plataformas de treino como TryHackMe, Hack The Box e similares

Este material é voltado para aprendizado defensivo, fundamentos de redes e evolução profissional em Segurança da Informação.

---

## Próximos passos

- Repetir os comandos até entender os resultados
- Desenhar minha rede de laboratório
- Criar pequenos relatórios de análise
- Estudar logs e tráfego de rede
- Avançar para fundamentos de SOC e Blue Team

---

## Autor

Estudos de Cybersecurity em andamento.

Foco atual:

- Linux
- Redes
- Segurança da Informação
- SOC
- Blue Team
- Pentest em laboratório
