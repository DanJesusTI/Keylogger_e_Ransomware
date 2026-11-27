Malware Behavior Lab — Python (Keylogger & Ransomware)

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Status](https://img.shields.io/badge/Ambiente-Laborat%C3%B3rio%20Controlado-success)
![Focus](https://img.shields.io/badge/Foco-Estudo%20%26%20Detec%C3%A7%C3%A3o-critical)

Repositório dedicado ao estudo prático do funcionamento interno de duas ameaças comuns — **Keylogger** e **Ransomware** — desenvolvidas em Python de forma simplificada para compreensão de técnicas ofensivas e criação de estratégias de detecção defensiva (Blue Team).

**Aviso Legal (Disclaimer):** Todo o conteúdo deste repositório tem finalidade estritamente **educacional e de pesquisa em segurança da informação**. Os testes foram conduzidos exclusivamente em máquinas virtuais (VMs) isoladas e autorizadas. O uso destes scripts fora de ambientes controlados e sem autorização explícita é ilegal e de inteira responsabilidade de quem os executa.

---

Estrutura do Repositório

```text
├── Keylogger_email/       # Captura de teclas e exfiltração simulada via SMTP
├── Ransomware_local/      # Criptografia e descriptografia simétrica de arquivos de teste
├── requirements.txt       # Dependências externas do laboratório
└── README.md              # Documentação técnica e visão defensiva

As bibliotecas usadas foram:
- Python Documentation — https://docs.python.org/3/
- Cryptography (Fernet) — https://cryptography.io/
- pynput — https://pypi.org/project/pynput/
- pip - https://pip.pypa.io/en/stable/
- keyboard - https://pypi.org/project/keyboard/
