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

## 📝 Script select SQL

Execute o seguinte script SQL no MySQL Workbench para criar a tabela `especies` e inserir os dados:

## 🐶 Atualiza o nome do animal de 'Pateta' para 'Goofy'
UPDATE animals a SET a.nome = 'Goofy' WHERE a.nome LIKE 'Pateta';

## 🐱 Altera o peso do Garfield para 10 kilogramas
UPDATE animals a SET a.Peso = 10 WHERE a.nome LIKE 'Garfield';

## 🐈 Altera a cor de todos os gatos para laranja
UPDATE animals a SET a.cor = 'laranja' WHERE a.raca LIKE 'Gato';

## 📏 Cria um campo altura para os animais
ALTER TABLE animals ADD COLUMN altura DECIMAL;

## 📝 Cria um campo observação para os animais
ALTER TABLE animals ADD COLUMN observacao VARCHAR(120);

## ⚖️ Remove todos os animais que pesam mais que 200 kilogramas
DELETE FROM animals a WHERE a.Peso > 200;

## 🔤 Remove todos os animais que o nome inicie com a letra 'C'
DELETE FROM animals a WHERE a.nome LIKE 'C%';

## 🎨 Remove o campo cor dos animais
ALTER TABLE animals DROP COLUMN cor;

## 📛 Aumenta o tamanho do campo nome dos animais para 80 caracteres
ALTER TABLE animals MODIFY COLUMN nome VARCHAR(80);

## 🐾 Remove todos os gatos e cachorros
DELETE FROM animals a WHERE a.raca LIKE 'Gato' OR a.raca LIKE 'Cachorro';

## 🎂 Remove o campo data de nascimento dos animais
ALTER TABLE animals DROP COLUMN dataNascimento;

## 🐕 Remove todos os animais
DELETE FROM animals a;

## 🗑️ Remove a tabela especies
DROP TABLE animals;
