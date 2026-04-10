MIRAI Finance
Aplicação web de controle financeiro pessoal com foco em organização mensal, visão rápida dos gastos e praticidade no dia a dia.
> Este projeto nasceu como **Hylian Finance** e foi rebrandado visualmente para **MIRAI Finance**.  
> O backend Firebase foi mantido para preservar autenticação e dados já existentes dos usuários.
Visão geral
O MIRAI Finance é um app front-end hospedado como página estática, com persistência de dados no Firebase.  
A proposta é entregar uma experiência leve, direta e funcional para acompanhar finanças pessoais com uma interface moderna.
Funcionalidades
Resumo financeiro mensal
Gestão de cartões
Metas financeiras
Área de perfil do usuário
Lembretes/notificações
Navegação por mês
Exportação e importação de dados em JSON
Tema claro/escuro
Login com Google
Login com e-mail e senha
Recuperação de senha
Persistência em Firestore
Stack
HTML, CSS e JavaScript
Firebase Authentication
Firebase Firestore
Chart.js
Lucide Icons
Font Awesome
GitHub Pages para hospedagem do front-end
Estrutura do projeto
Atualmente o app foi construído de forma enxuta, com foco em agilidade:
```bash
.
├── index.html
├── README.md
├── mirai_symbol_transparent.png
└── mirai_favicon.png
```
Firebase
O projeto continua apontando para o mesmo backend Firebase já usado anteriormente, para evitar perda de dados dos usuários.
Observação importante
Mesmo com o rebranding para MIRAI Finance, o projeto Firebase permanece com identificadores legados, como:
`projectId: hylianfinance`
`authDomain: hylianfinance.firebaseapp.com`
Isso é intencional e ajuda a manter compatibilidade com a base existente.
Como rodar localmente
Como o app é estático, você pode abrir de algumas formas:
Opção 1
Abrir o `index.html` direto no navegador.
Opção 2
Servir com uma extensão/local server, por exemplo:
```bash
npx serve .
```
ou
```bash
python -m http.server 5500
```
Depois, abra no navegador o endereço local gerado.
Deploy
O deploy pode ser feito de forma simples no GitHub Pages.
Passos
Suba os arquivos do projeto para o repositório
Garanta que o arquivo principal esteja como `index.html`
Ative o GitHub Pages no branch principal
Caso use domínio customizado, mantenha a configuração DNS já apontada
Organização dos dados
A aplicação usa Firestore com estrutura separada por usuário autenticado, o que ajuda a manter os dados isolados por conta.
Exemplos de caminhos usados:
`users/{uid}/data/mensalidades`
`users/{uid}/data/cartoes`
`users/{uid}/data/compras`
`users/{uid}/data/metas`
`users/{uid}/transacoes/fin_ano_mes`
Objetivo do projeto
O MIRAI Finance foi pensado para ser:
simples de usar
rápido de abrir
fácil de manter
agradável visualmente
útil no acompanhamento financeiro diário e mensal
Roadmap
Ideias para evolução futura:
dashboard ainda mais refinado
relatórios mais completos
filtros avançados
categorias personalizadas
melhorias em metas
melhorias em compras parceladas
versão mais modular do código
separação de estilos e scripts em arquivos dedicados
Identidade
Empresa/marca: Kaji Labs  
Produto: MIRAI Finance  
Assistente interno: MiraiX
Autor
Desenvolvido por Felipe Ferreira.
---
Se este projeto te ajudou ou serviu de referência, fique à vontade para adaptar à sua própria necessidade.
