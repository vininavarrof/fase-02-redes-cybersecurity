# Diagrama Simples da Rede de Laboratório

Modelo básico para representar a rede usada nos estudos.

```text
+----------------------+
| Meu computador       |
| Windows              |
+----------+-----------+
           |
           | VirtualBox
           |
+----------v-----------+
| VM Ubuntu            |
| IP: 10.0.2.15        |
| Interface: enp0s3    |
+----------+-----------+
           |
           | NAT / Gateway
           |
+----------v-----------+
| Roteador / Internet  |
+----------+-----------+
           |
           |
+----------v-----------+
| Servidores externos  |
| Ex: google.com       |
+----------------------+
```

---

## Explicação

- O computador físico executa o VirtualBox.
- A VM Ubuntu recebe um IP virtual.
- O gateway permite que a VM acesse a internet.
- O DNS transforma nomes como `google.com` em IP.
- O tráfego passa pela rota padrão até chegar ao destino.

---

## Campos para preencher

```text
IP do PC:
IP da VM:
Gateway da VM:
DNS usado:
Modo de rede da VM:
```
