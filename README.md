
![alt text](https://travis-ci.org/jandrei/exemplo-liquibase.svg?branch=master "Build with Travis-ci.org")

# exemplo-liquibase
exemplos de execução de projeto com liquibase e maven, criando versões de banco e fazendo rollback.

é um simples projeto maven java com configurações necesárias para executar alterações com liquibase na versão 3.1.1 em diversos bancos.

# Execução para ambiente de desenvolvimento
Goals:liquibase:update -Dliquibase_context_name=desenv -Pliquibase-update

# Execução para ambiente de homologação
liquibase:update -Dliquibase_context_name=hml -Pliquibase-update

# Execução para ambiente de produção
liquibase:update -Dliquibase_context_name=prod -Pliquibase-update

# Execução para rollback de uma versão ou várias
liquibase:rollback -Dliquibase_context_name=desenv -Dliquibase.rollbackTag=versao1 -Pliquibase-update

sendo que versao1 é a tag setada no início de cada arquivo de versão, com isso consigo fazer rollback de qualquer versão do projeto.
