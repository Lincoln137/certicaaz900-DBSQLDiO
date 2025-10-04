# certicaaz900-DBSQLDiO
## BD SQL no portal Azure

O Azure SQL Database é o serviço de Banco de Dados Relacional como Serviço (PaaS) da Microsoft Azure.

***Passo a Passo:*** Criação de um Azure SQL Database (Banco de Dados Individual)
1. Acesso e Seleção do Serviço
Acesse o Portal: Entre em portal.azure.com com sua conta.

Pesquise: Na barra de pesquisa superior, digite "Azure SQL" e clique no serviço correspondente.

Criar Recurso: Na página do Azure SQL, clique em "+ Criar".

Escolha a Opção: Em "Opção de implantação SQL", selecione "Banco de Dados SQL" (SQL Database) e, em seguida, "Banco de dados individual" (Single database). Clique em "Criar".

2. Configuração de "Básico" (Basics)
Esta é a etapa central, onde você define a localização, o nome do BD e cria o servidor lógico.

Configuração	Detalhes	Ação
Detalhes do Projeto	Assinatura e Grupo de Recursos.	Selecione sua Assinatura e crie um Grupo de Recursos (ex: RG-Aplicacao-BD).
Detalhes do Banco de Dados	Nome do Banco de Dados.	Insira um nome para o seu BD (ex: MeuAppBD-Prod).
Servidor	O servidor lógico que hospedará o BD.	Clique em "Criar novo" e configure:
- Nome do Servidor: Deve ser exclusivo globalmente.	Ex: meuservidorsql12345
- Localização: Escolha a região mais próxima dos usuários.	Ex: Brazil South
- Credenciais: Defina o Logon do administrador do servidor (usuário) e uma Senha forte.	
Configuração de Capacidade	Nível de desempenho (custo e recursos).	Clique em "Configurar banco de dados" e escolha:
- Modelo de compra: DTU ou vCore (vCore é geralmente mais flexível).	
- Nível de serviço: Uso Geral é o mais comum.	
- vCores/Tamanho: Ajuste a quantidade de vCores e o armazenamento necessário.	

3. Configuração de Rede (Networking)
Defina como o BD será acessível:

Método de Conectividade:

Recomenda-se Ponto de extremidade privado (para máxima segurança).

Se precisar de acesso simples, escolha Ponto de extremidade público.

Regras de Firewall (Se Ponto Público):

Em "Permitir que os serviços e recursos do Azure acessem este servidor", escolha Sim se precisar de serviços como Azure Functions, Web Apps, etc.

Clique em "+ Adicionar endereço IP do cliente" para incluir seu IP atual, permitindo que você se conecte ao BD a partir de sua máquina local imediatamente.

4. Configurações Adicionais e Conclusão
Configurações Adicionais (Additional settings):

Em "Fonte de dados", escolha "Exemplo" para criar o BD com o esquema de amostra AdventureWorksLT (ótimo para testes), ou "Nenhuma" para um BD vazio.

Revisar + Criar:

Clique na guia "Revisar + Criar".

Verifique o resumo das configurações e o custo estimado.

Criar:

Clique em "Criar". A implantação levará alguns minutos.

Após a criação, você pode ir para o recurso implantado para obter o Nome do Servidor e gerenciar o Firewall e as Conexões.
