# Malware Behavior Lab — Python (Keylogger & Ransomware)

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Status](https://img.shields.io/badge/Ambiente-Laborat%C3%B3rio%20Controlado-success)
![Foco](https://img.shields.io/badge/Foco-Estudo%20e%20Detec%C3%A7%C3%A3o-red)

Repositório dedicado ao estudo prático do funcionamento interno de duas ameaças comuns — **Keylogger** e **Ransomware** — desenvolvidas em Python de forma simplificada para compreensão de técnicas ofensivas e criação de estratégias de detecção defensiva (Blue Team).

> **Aviso Legal (Disclaimer):** Todo o conteúdo deste repositório tem finalidade estritamente **educacional e de pesquisa em segurança da informação**. Os testes foram conduzidos exclusivamente em máquinas virtuais (VMs) isoladas e autorizadas. O uso destes scripts fora de ambientes controlados e sem autorização explícita é ilegal e de inteira responsabilidade de quem os executa.

---

## Estrutura do Repositório

```text
├── Keylogger_email/
│   └── keyloggeremail.py   # Captura de teclas e envio simulado via SMTP
├── Ransomware_local/
│   ├── criptografar.py     # Criptografia simétrica (Fernet) de arquivos de teste
│   └── descriptografar.py  # Restauração dos arquivos usando a chave gerada
├── requirements.txt        # Dependências externas do laboratório
└── README.md               # Documentação técnica e visão defensiva
```

---

## Bibliotecas Utilizadas

* [`cryptography` (Fernet)](https://cryptography.io/) — geração de chave simétrica, criptografia e descriptografia de arquivos.
* [`pynput`](https://pypi.org/project/pynput/) e [`keyboard`](https://pypi.org/project/keyboard/) — captura e monitoramento de eventos de teclado no ambiente de teste.
* [`smtplib`](https://docs.python.org/3/library/smtplib.html) — módulo nativo do Python usado no envio de logs via SMTP.

---

## Mapeamento MITRE ATT&CK e Detecção (Blue Team)

| Script | Tática MITRE | Técnica (ID) | Sinais de Detecção |
| :--- | :--- | :--- | :--- |
| `keyloggeremail.py` | Collection / Exfiltration | Keylogging (`T1056.001`) e Exfiltration Over Alternative Protocol (`T1048`) | Execução de `pythonw.exe` fora de diretórios padrão e conexões SMTP de saída (portas `587`/`465`) vindas de estações comuns. |
| `criptografar.py` | Impact | Data Encrypted for Impact (`T1486`) | Alta taxa de leitura/escrita em arquivos em curto espaço de tempo e criação de chave local em disco. |

---

## Autor

**Daniel Jesus Morais**
* GitHub: [@DanJesusTI](https://github.com/DanJesusTI)
