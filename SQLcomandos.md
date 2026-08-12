```sql
-- Criação da tabela
CREATE TABLE produtos (
    codigo INT PRIMARY KEY,
    descricao VARCHAR(255) NOT NULL,
    preco DECIMAL(16,2) NOT NULL,
    ativo BOOLEAN NOT NULL,
    data_cadastro TIMESTAMP NOT NULL
);

-- Alterações na estrutura da tabela
ALTER TABLE produtos DROP COLUMN data_cadastro;

ALTER TABLE produtos ALTER COLUMN preco DROP NOT NULL;

-- Exclusão da tabela
DROP TABLE produtos;

-- Inserção de dados
INSERT INTO produtos (
    codigo, 
    descricao, 
    preco, 
    data_cadastro, 
    ativo
) VALUES (
    1, 
    'PlacaVideoNvidia', 
    3000.00, 
    NOW(), 
    TRUE
);

-- Consulta de dados
SELECT descricao FROM produtos;
```
