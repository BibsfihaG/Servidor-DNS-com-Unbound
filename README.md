# 🌐 Servidor DNS Recursivo e Autoritativo Local com Unbound

Repositório contendo a configuração do **Unbound DNS** para resolução de nomes em um ambiente com **múltiplas sub-redes** (dual-homed), incluindo suporte a zonas locais estáticas e aliases (CNAME).

---

## 🛠️ Tecnologias e Ferramentas
* **Linux / Debian / Ubuntu**
* **Unbound DNS Server**

---

## 📐 Topologia / Cenário
O servidor foi configurado para atender consultas DNS de duas redes distintas, com controle de acesso rigoroso e registros customizados:

* **Rede A:** `172.31.0.0/16` (Zona: `dns.teste.local`)
* **Rede B:** `192.168.1.0/24` (Zona: `android.local`)
* **Loopback:** `127.0.0.0/8`

---

## ⚙️ Principais Funcionalidades Configurações

* Escuta em todas as interfaces de rede (`interface: 0.0.0.0`).
* Restrições de segurança via `access-control`.
* Definição de zonas locais estáticas (`local-zone`).
* Mapeamento de registros do tipo **A** e **CNAME** (`local-data`).
