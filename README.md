# 🛠️ Cybersecurity Cheatsheet

Um guia rápido com comandos e dicas de ferramentas essenciais para cibersegurança.  
> 📌 Útil para estudo, laboratórios e consultas rápidas.

---

## 🌐 Nmap (Network Mapper)
Mapeamento de hosts e portas.

```bash
# Descobrir hosts ativos na rede
nmap -sn 192.168.1.0/24

# Escanear portas comuns
nmap -F 192.168.1.10

# Escanear todas as portas com detecção de serviço e SO
nmap -p- -sV -O 192.168.1.10

# Escanear portas específicas
nmap -p 22,80,443 192.168.1.10
```

## 🧭 Gobuster
Força bruta de diretórios e arquivos web.

```bash
# Scan de diretórios usando wordlist padrão
gobuster dir -u http://site.com -w /usr/share/wordlists/dirb/common.txt
```

## 📡 Wireshark / tcpdump
Captura e análise de pacotes.

```bash
# Capturar pacotes na interface eth0 (tcpdump)
sudo tcpdump -i eth0

# Filtrar apenas pacotes HTTP
tcpdump -i eth0 port 80

# No Wireshark: usar filtros como http, dns, tcp.port==443
```

## 🛡️ Metasploit
Framework para testes de penetração.

```bash
# Iniciar console
msfconsole

# Buscar exploit
search vsftpd

# Usar exploit
use exploit/unix/ftp/vsftpd_234_backdoor
```

## 🔑 Hydra
Força bruta de senhas em serviços.

```bash
# Testar FTP
hydra -l usuario -P wordlist.txt ftp://192.168.1.10

# Testar SSH
hydra -l root -P wordlist.txt ssh://192.168.1.10
```

---

## 🧪 Dicas Extras

 - Sempre pratique em ambientes controlados (máquinas virtuais, labs como TryHackMe ou HackTheBox).

 - Nunca escaneie ou ataque sistemas sem autorização.

 - Documente seus testes e resultados.

## 📚 Recursos de Estudo

 - [OWASP Top 10](https://owasp.org/www-project-top-ten/)
 - [Guia de Nmap](https://nmap.org/book/inst-windows.html)
 - [TryHackMe](https://tryhackme.com)
 - [Hack The Box](https://hackthebox.com)