# README.md  
  
## Visão geral  
  
Este guia descreve de forma resumida como preparar o ambiente e executar a aplicação Flask utilizando Python, ambiente virtual e Redis.  
  
---  
  
# Passos para execução  
  
## 1. Atualizar o sistema  
  
```bash  
sudo apt update
```
Atualiza a lista de pacotes disponíveis nos repositórios do sistema.

----------

## 2. Instalar dependências do Python
```bash  
sudo apt install -y python3-full python3-venv python3-pip
```
Instala:

-   **python3-full**: distribuição completa do Python
    
-   **python3-venv**: permite criar ambientes virtuais
    
-   **python3-pip**: gerenciador de pacotes Python
    

----------

## 3. Criar ambiente virtual
```
python3 -m venv venv
```
Cria um ambiente isolado chamado **venv** para evitar conflitos de dependências.

----------

## 4. Ativar ambiente virtual
```
source venv/bin/activate
```
Ativa o ambiente virtual para que as bibliotecas sejam instaladas apenas no projeto.

----------

## 5. Instalar dependências do projeto
```
pip install -r requirements.txt
```
Instala todas as bibliotecas necessárias listadas no arquivo **requirements.txt**.

----------

## 6. Instalar Redis
```
sudo apt-get install redis
```
Instala o **Redis**, utilizado pela aplicação como armazenamento em memória ou cache.

----------

## 7. Configurar host do Redis
```
export  REDIS_HOST=127.0.0.1
```
Define a variável de ambiente indicando que o Redis está rodando localmente.

----------

## 8. Executar aplicação Flask
```
flask run --host=0.0.0.0
```
Inicia a aplicação Flask permitindo acesso pela rede.

Aplicação normalmente ficará disponível em:

http://localhost:5000
