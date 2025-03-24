# Api Doação de Livros

Essa é uma API simples feita com Flask e com SQLite3 para fins de estudo na escola Vai Na Web, ela permite cadastrar e listar livros doados.

## Como rodar o projeto

1. Faça o clone do repositório:
```bash
git clone <URL_DO_REPOSITORIO>
cd nome-do-projeto
```

2. Crie um ambiente virtual (obrigatório):
```bash
python -m venv venv
source venv/Scripts/activate
```
3. Instale as dependências
```bash
pip install -r requeriments.txt
```

4. Inicie o servidor:
```bash
python app.py
```

> A api está disponivel em http: http://127.0.0.1:5000/

## Endpoints

### POST/doar

Endpoint para cadastrar um novo livro.

**Formato de envio dos dados**

```json
{
    "titulo":"Dragões de Eter",
    "categoria":"Fantasia",
    "autor":"Raphael Draccon",
    "image_url":"https://exemplo.com"
}
```

**Resposta 201 (Created)**:
```json
{
    "mensagem":"Livro cadastrado com sucesso"
}
```

---

### GET/livros

Retorna todos os livros cadastrados em nossa API

**Respota (200)**:
```json
{
    "id":"1",
    "titulo":"Dragões de Eter",
    "categoria":"Fantasia",
    "autor":"Raphael Draccon",
    "image_url":"https://exemplo.com"
}
```