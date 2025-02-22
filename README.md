# Configuração de Servidor PostgreSQL para Produção

Este projeto foi desenvolvido para configurar um servidor PostgreSQL em ambiente de produção. O objetivo é garantir que o banco de dados esteja configurado corretamente com as permissões e ajustes necessários para um funcionamento seguro e eficiente.

## Estrutura do Projeto

### Arquivo: `addlines.yaml`
O arquivo `addlines.yaml` é um modelo para adicionar linhas a arquivos de configuração do servidor. Ele pode ser utilizado para realizar ajustes como a criação de permissões de disco, modificações em configurações de segurança e outros ajustes necessários para a operação do PostgreSQL.

### Como Utilizar
1. Edite o arquivo `addlines.yaml`, preenchendo as informações conforme a necessidade.
2. Execute o processo de configuração para que as linhas sejam aplicadas nos arquivos corretos.

### Arquivo: `cpremotefile.yaml`
O arquivo `cpremotefile.yaml` é utilizado para copiar arquivos de uma máquina remota, que esteja na mesma rede, para a máquina onde estamos realizando a configuração. Caso seja necessário, essa playbook pode ser invocada para esse propósito.

**Detalhe importante:** A máquina de origem do arquivo precisa ter um sistema operacional Linux para que o processo funcione corretamente.

### Arquivo: `createuser.yaml`
O arquivo `createuser.yaml` tem o objetivo de criar um novo usuário no sistema. Além disso, ele configura as permissões necessárias para que esse usuário possa acessar o sistema via SSH e escalar permissões para o usuário root sem precisar digitar a senha.

Este projeto pode ser expandido para incluir outras configurações essenciais ao PostgreSQL, garantindo um ambiente seguro e otimizado para produção.
