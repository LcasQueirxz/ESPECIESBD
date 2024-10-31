# Banco de Dados de Espécies

## 📋 Pré-requisitos

Para rodar este projeto, você precisará de:

- **MySQL**: Um servidor MySQL instalado e configurado.
- **MySQL Workbench** (ou qualquer outro cliente MySQL de sua preferência).

## 🔧 Como instalar o software

1. **Instale o MySQL**:
   - Baixe e instale o MySQL a partir do site oficial.
   - Siga as instruções de instalação e configure o servidor MySQL.

2. **Instale o MySQL Workbench**:
   - Baixe e instale o MySQL Workbench a partir do site oficial.

3. **Configuração do Banco de Dados**:
   - Abra o MySQL Workbench e conecte-se ao seu servidor MySQL.
   - Selecione ou crie um banco de dados onde você deseja criar a tabela `especies`.
   - Execute o seguinte comando para selecionar o banco de dados:
     ```sql
     USE nome_do_seu_banco_de_dados;
     ```

## 📝 Script SQL

Execute o seguinte script SQL no MySQL Workbench para criar a tabela `especies` e inserir os dados:

```sql
DROP TABLE IF EXISTS especies;

CREATE TABLE especies (
  id INT NOT NULL AUTO_INCREMENT,
  nome VARCHAR(100) DEFAULT NULL,
  raca VARCHAR(100) DEFAULT NULL,
  cor VARCHAR(20) DEFAULT NULL,
  peso DECIMAL(10,2) DEFAULT NULL,
  dataNascimento DATE DEFAULT NULL,
  PRIMARY KEY (id)
);

INSERT INTO especies (nome, raca, cor, peso, dataNascimento) VALUES
    ('Groofy', 'Cachorro', 'preto', 40.50, '2020-01-01'),
    ('boot', 'Cachorro', 'cinza', 29.30, '2019-02-15'),
    ('scobby', 'Cachorro', 'branco e preto', 37.40, '2018-03-20'),
    ('toto', 'Cachorro', 'preto', 17.10, '2017-04-25'),
    ('bolinha', 'Gato', 'marrom', 27.50, '2016-05-30'),
    ('cacau', 'Gato', 'preto', 36.30, '2015-06-10'),
    ('princesa', 'Gato', 'amarelo', 35.50, '2014-07-15'),
    ('jorginho', 'Cachorro', 'marrom', 25.40, '2013-08-20'),
    ('bolota', 'Cachorro', 'preto', 40.20, '2012-09-25'),
    ('caju', 'Gato', 'bege', 10.30, '2011-10-30'),
    ('caramelo', 'Gato', 'caramelo', 25.50, '2010-11-05'),
    ('Garfield', 'Gato', 'laranja', 10.30, '2009-12-10');
