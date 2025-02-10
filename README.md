![Thumb](https://github.com/yslanlopes12/Terminal-do-Kali-Linux-no-Windows/blob/main/thumb_kali_windows.webp)
# Rodando o Kali Linux no Windows de Forma Simples e Eficiente com WSL
   
   **O Kali Linux é uma das distribuições mais populares para cibersegurança e testes de intrusão, sendo amplamente utilizado por profissionais da área. No entanto, para quem está iniciando, rodar o Kali em uma máquina virtual (VM) pode ser trabalhoso e exigir um alto consumo de recursos do computador.**
   
   **Pensando nisso, uma solução eficiente e prática é utilizar o Windows Subsystem for Linux (WSL), que permite rodar distribuições Linux diretamente no Windows sem a necessidade de dual boot ou máquinas virtuais. Com essa abordagem, você pode ter um ambiente de testes funcional, integrado ao Windows e consumindo menos processamento.**

# Por que usar o WSL para rodar o Kali Linux?

🔹 **Menor consumo de recursos** – Não há necessidade de reservar memória RAM e CPU para uma máquina virtual.

🔹 **Integração com o Windows** – Acesso direto ao sistema de arquivos do Windows, facilitando a manipulação de arquivos.

🔹 **Facilidade de instalação** – O Kali pode ser instalado rapidamente via Microsoft Store ou terminal.

🔹 **Atualizações diretas** – Você pode manter o sistema atualizado com os repositórios oficiais da Offensive Security.

🔹 **Ideal para iniciantes** – Uma ótima forma de começar no mundo Linux sem comprometer seu sistema principal.

## **Pré-requisitos**

Antes de começar, certifique-se de que seu Windows está atualizado (Windows 10 versão 2004 ou superior, ou Windows 11).

Para verificar se é realmente é a versão adequada, clique em "WIN + R" para abrir o executar do seu windows, escreva "winver" e clique em "OK".
Deverá aparecer esta Janela:

![Janela](https://github.com/yslanlopes12/Terminal-do-Kali-Linux-no-Windows/blob/main/Janela.jpg)

# Passo a Passo para Instalar o Kali Linux no Windows com WSL

### **1. Ativar o WSL no Windows**
Abra o **PowerShell como Administrador** e execute o seguinte comando para ativar o WSL:
![powershell](https://github.com/yslanlopes12/Terminal-do-Kali-Linux-no-Windows/blob/main/powershell.png)

No terminal do powershell escreva:

```powershell
wsl --install
```

![wsl](https://github.com/yslanlopes12/Terminal-do-Kali-Linux-no-Windows/blob/main/imagem2.png)

Esse comando ativa automaticamente o suporte ao WSL e instala o Ubuntu como sistema padrão. Como queremos instalar o Kali Linux, vamos prosseguir com o próximo passo.

---

### **2. Instalar o Kali Linux no WSL**

Para instalar o Kali Linux no Windows, basta rodar:

```powershell
wsl --install -d kali-linux
```
![KALI](https://github.com/yslanlopes12/Terminal-do-Kali-Linux-no-Windows/blob/main/kali.jpg)

Esse comando baixará e instalará automaticamente o Kali Linux.

Caso tenha versões antigas do WSL instaladas, use o seguinte comando para garantir que o WSL 2 está ativado:

```powershell
wsl --set-default-version 2
```

---

### **3. Iniciar o Kali Linux**

Após a instalação, abra o terminal e inicie o Kali com:

```powershell
wsl -d kali-linux
```

![KALIuser](https://github.com/yslanlopes12/Terminal-do-Kali-Linux-no-Windows/blob/main/kali%20user.jpg)


Na primeira execução, será solicitado que você crie um usuário e senha.

Após isso, você pode seguir esses passos para que o kali seja seu terminal padrão(Só uma Sugestão é claro, mas se preferir você pode colocar o "Ubunto" por exemplo):

- Feche o terminal e abra novamente, vá em configurações e selecione o kali linux como o terminal padrão , salve e abra um novo terminal. Caso seu Sistema Operacional seja o "Windows 10", sugiro que baixe o "Terminal para Windows" na "Microsoft Store" para conseguir seguir estes passos.

exemplos: 

![KALIconfigue](https://github.com/yslanlopes12/Terminal-do-Kali-Linux-no-Windows/blob/main/configue.jpg)

![KALIpadrao](https://github.com/yslanlopes12/Terminal-do-Kali-Linux-no-Windows/blob/main/kali%20padr%C3%A3o.jpg)


---

### **4. Atualizar e Instalar Pacotes Essenciais**

Agora, vamos atualizar o Kali Linux e instalar pacotes essenciais:

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install -y kali-linux-default
```

Isso garantirá que todas as ferramentas principais do Kali estejam disponíveis.

---

### **EXTRAS!!! Definir o Kali como WSL Padrão (Opcional)**

Se deseja que o Kali Linux seja o ambiente padrão do WSL, execute:

```powershell
wsl --set-default kali-linux
```

Isso garantirá que, sempre que você rodar o `wsl`, o Kali será carregado.

---

### **Testando Ferramentas do Kali**

Agora que o Kali está instalado, podemos testar algumas ferramentas básicas:

```bash
nmap --version
metasploit-framework --version
hydra -h
aircrack-ng --help
```

Se os comandos retornarem as versões corretas, sua instalação foi um sucesso!

---

## **Conclusão**

Com o **WSL**, podemos rodar o **Kali Linux** de maneira eficiente e integrada ao Windows, sem a necessidade de máquinas virtuais ou dual boot. Isso facilita o aprendizado e possibilita o uso das ferramentas de cibersegurança de forma prática.

Se você gostou desse guia, deixe um ⭐ no repositório e compartilhe com a comunidade! 🚀

📌 **LINKEDIN:** [https://www.linkedin.com/in/yslanlopes/](https://www.linkedin.com/in/yslanlopes/)

🚀 **#Linux #Cibersegurança #WSL #KaliLinux #Pentest #GitHub #Hacking #Tecnologia #Inovação**

