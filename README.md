# 🎓 SPEX - Sistema de Simulação e Preparação para Exames

## 📌 Sobre o Projeto
O **SPEX** é uma plataforma online desenvolvida para ajudar estudantes a se prepararem para exames através de simulações personalizadas. Ele permite que os usuários façam testes práticos, acompanhem seu progresso e acessem materiais de estudo.

## 🚀 Tecnologias Utilizadas
O projeto foi desenvolvido com as seguintes tecnologias:
- **PHP** (Backend)
- **MySQL** (Banco de Dados)
- **HTML5, CSS3** (Estrutura e Estilos)
- **Bulma** (Framework CSS)

## 📂 Estrutura de Diretórios
/spex
    │── /database
        │── /backups # Contém os cópias de segurança da base de dados criadas de forma automática
        │── backup.bat # Script para criar backups do banco de dados automaticamente (Windows)
        │── backup.sh # Script para criar backups do banco de dados automaticamente (Linux)
        │── CAMINHO_BACKUP # Contém o caminho do directório no qual serão guardados os arquivos de backup criados.
        │── schema.sql # Script SQL para criação da base de dados
        │── seeds.sql # Script SQL que contém dados iniciais da base de dados (usuários, cursos, etc)
        │── consultar_estudantes.sql # Script SQL para consultar os registros de "estudante" (para testes de login)
    │── /docs
        │── /diagramas # Contém os diagramas usados para implementar o sistema (UML)
            │── /diagrama_arquitectura_sistema
            │── /diagrama_entidade_relacionamento
            │── /diagramas_actividades
            │── /diagramas_casos_uso
            │── /diagramas_classes
            │── /diagramas_sequencia
            │── requisitos.md # Requisitos do sistema
            │── sys.md # Informacoes uteis sobre o sistema
            │── sys.txt # Versao txt de "sys.md"
            │── guia_instalacao # Ajuda para instalacao e funcionamento do sistema
    │── /public  
        ├── index.html # Página pública inicial
        ├── css # Arquivos CSS (Bulma, estilos personalizados)
            ├── bulma # Arquivos CSS Bulma
            ├── fontawesome # Arquivos de Fonte
        ├── img # Imagens utilizadas pelo sistema
        ├── js # Scripts JavaScript
        ├── uploads # Arquivos carregados pelos usuários
            ├── users # Arquivos pessoais de cada usuário
                ├── usuario_1 # Usuário 1
                    ├── perfil # Foto de perfil do usuario
                    ├── exames # Exames Realizados pelo usuário em formato sPDF
                    ├── relatorios # Relatórios sobre o desempenho do usuário em formato PDF
                    ├── docs # Outros documentos enviados
                ├── usuario_2 # Usuário 2
                    ├── perfil # Foto de perfil do usuario
                    ├── exames # Exames Realizados pelo usuário em formato sPDF
                    ├── relatorios # Relatórios sobre o desempenho do usuário em formato PDF
                    ├── docs # Outros documentos enviados
        ├── favicon.ico # Ícone do site
    │── /src
        │── /assets # contem os arquivos usados internamente pelo sistema
            │── /fonts # Fontes específicas para uso restrito
            │── /icons # Ícones específicos para uso restrito
            │── /img # Imagens específicas para uso restrito
        ├── /controllers # Controladores do sistema  
            │── /helpers # Funções ajudantes para tarefas genéricas repetitivas no backend
            │── AuthController.php # Gerencia o login no sistema
            │── EstudanteController.php # Gerencia as requisições dos usuários "estudantes"
        ├── /models # Modelos do banco de dados 
            │── EstudanteModel.php # Modela e define (atributos e métodos) a entidade estudante no sistema
        ├── /views # Páginas do usuário
            │── cadastro_estudante.php # Página a partir da qual o usuário se cadastra no sistema
            │── dashboard # página que serve de ponto de entrada para o usuário logado no sistema
            │── login.php # página por onde o usuário faz login
            │── recuperar_senha.php # página para recuperação de senhas
        │── /config │
            │── config.php # Configuração do ambiente da aplicação
            ├── database.php # Configuração do banco de dados
            │── env_loader.php # Carrega as variáveis do ambiente do ".env"
    │── /tests # contém arquivos de teste unitários e de integração do sistema
        │── /unit # testes unitários
        │── /integration # testes de integração
        │── test_db.php # testa a conexão com a base de dados
        │── test_login.php # testa o login no sistema (página de entrada)
        │── test_login2.php # página de redirecionamento após login bem-sucedido em "test_login.php"
│── index.php # Redirecionamento inicial 
│── README.md # Documentação do projeto
│── .env # Configurações de ambiente (credenciais do banco)
│── .gitignore # Arquivos a serem ignorados pelo Git


## 🛠️ Instalação
1. Clone este repositório: 
   git clone `https://github.com/GabrielAbreu19/spex.git`

2. Configure o banco de dados MySQL usando o script SQL fornecido.

3. Altere as credenciais do banco de dados em /config/database.php.

4. Inicie um servidor local:
    php -S localhost:8000 -t public

5. Acesse no navegador:
    http://localhost:8000
    
## 📌 Funcionalidades
    ✅ Registro e login de usuários
    ✅ Simulação de exames personalizados
    ✅ Histórico de desempenho
    ✅ Administração de questões e provas

## 🏗️ Contribuindo
    Se quiser contribuir para o projeto, siga os seguintes passos:
    1. Faça um fork do repositório.
    2. Crie uma branch com a sua feature:
        git checkout -b minha-feature

    3. Faça as alterações e commit:
        git commit -m "Minha nova feature"

    4. Envie para o repositório remoto:
        git push origin minha-feature

    5. Abra um Pull Request 🚀.

## 📄 Licença
    Este projeto está sob a licença MIT.  (Para mais detalhes, consulte o arquivo LICENSE.)