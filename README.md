# Entregável 1

O código abaixo cria e popula as tabelas usuário e clínica: <br>

async function criarepopulartabelausuarios(nome_user, email_user, senha_user, telefone_user, endereco_user){ <br> 
async: faz a função abrigar funções assíncronas <br>

const db = await open ({ <br>
        filename: './banco.db', <br>
        driver: sqlite3.Database <br>
    }); <br>

await: faz com que a operação seja assíncrona, para o código não fica travado <br>
open: abre uma conexão com o banco de dados <br>
filename: pede o caminho para o banco de dados <br>
driver: pede a biblioteca encarregada de fazer a conexão e realizar as operações <br>

db.run('CREATE TABLE IF NOT EXISTS usuarios (id INTEGER PRIMARY KEY AUTOINCREMENT, nome_user TEXT, email_user TEXT, senha_user TEXT, telefone_user TEXT, endereco_user TEXT)'); <br>
* Cria a tabela "usarios", se ela não existir, e seus atributos <br>

db.run('INSERT INTO usuarios (nome_user, email_user, senha_user, telefone_user, endereco_user) VALUES (?, ?, ?, ?, ?)', [nome_user, email_user, senha_user, telefone_user, endereco_user]); <br>
* Insere valores na tabela "usuarios"



![código](foto.png)
