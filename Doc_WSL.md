# Iniciando a configuração do ambiente de desenvolvimento

## Índice
1. [Habilitar o WSL e a Plataforma de Maquina Virtual](#Habilitar-o-WS-e-a-Plataforma-de-Maquina-Virtual)
2. [Baixar o pacote de atualizacao do kernel do Linux](#Baixar-o-pacote-de-atualizacao-do-kernel-do-Linux)
3. [Instalar o Ubunto](#Instalar-o-Ubunto)
4. [Iniciando vitualizacao](#Iniciando-vitualizacao)
7. [Encerrando virtualizacao](#Encerrando-virtualizacao)



# 1 - Habilitar o WSL e a Plataforma de Maquina Virtual
Abra o powerShell como admninistrador e execute:
```
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

# 2 - Baixar o pacote de atualizacao do kernel do Linux
use os comandos:
```
wsl.exe --install
wsl.exe --update
```
feito isso defina o wsl 2 como padrão com o comando:
```
wsl --set-default-version 2
``` 
para ativar os recursos do Windows
```
control appwiz.cpl
``` 

# 3 - Instalar o Ubunto
para verificar a instalaçao use o comando: 
```
wsl -l -v
``` 

caso não tiver use o comando, para verificar a lista de distribuição:
```
wsl.exe --list --online
``` 
depois utilize o comando, para instalar a  distribuição escolhida:
``` 
wsl.exe --install <Distro>
```
feito a instalação reeinicie o computado e será necessario criar nome de usuario e senha para o ambiente linux

# 4 - Iniciando vitualizacao 
use o comando, que ira iniciar a virtualização:
```
wsl -d Ubuntu -u (nome_usuario)
```

Utilize alguns scripts prontos para atualizar o sistema:
```
curl -O (Url do scritp em formato Raw)
```

use o comando:
```
sudo chmod +x ./setup_sources.sh
```

executa:
```
./setup_sources.sh
```

use esses mesmos comandos para o script do Vscode

se usar o comando: ``` code . ``` ira iniciar o vscode na virtualização 

# 5 - Import
Para fazer o Import:
```
wsl --import (nome-nova-maquina)(caminho + qual-pasta-vai-guardar-no-disco)(caminho + nome-arquivo-exportado)
```
exemplo: 
wsl --import contatica a:\wsl\contatica a:\wsl\template.tar


# 6 - Export

Para fazer o Export: 
```
wsl --export Ubuntu (pasta-de-destino)(nome-para-o-arquivo)
```
exemplo:
wsl --export Ubuntu c:\wsl\template.tar

# 7 - Encerrando virtualizacao 
utilize o comando, para sair da virtualização:
```
exit
```

Para encerrar utilize:
```
wsl --shutdown
``` 