from flask import Flask, jsonify

app = Flask(__name__)

# Dados de exemplo (pode ser substituído por um banco de dados)
projetos = [
    {"id": 1, "nome": "Projeto A", "descricao": "Descrição do Projeto A"},
    {"id": 2, "nome": "Projeto B", "descricao": "Descrição do Projeto B"},
]

# Rota para obter informações sobre todos os projetos
@app.route('/projetos', methods=['GET'])
def get_projetos():
    return jsonify(projetos)

if __name__ == '__main__':
