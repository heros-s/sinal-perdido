Sinal Perdido — Jogo de Exploração em HTML e CSS
=================================================

1. TEMA E PREMISSA
------------------
Você é a engenheira de manutenção da Estação Orbital Kepler-7. Ao despertar da câmara de hibernação, a estação encontra-se abandonada, operando em modo de energia mínima e com a reserva de oxigênio em queda constante. Seu objetivo é explorar os três módulos da estação (Laboratório, Engenharia e Comunicações), reunir os equipamentos essenciais e transmitir um pedido de socorro na frequência correta (406,0 MHz).

2. COMO ABRIR E JOGAR
---------------------
- Como abrir: basta dar dois cliques no arquivo `index.html` em qualquer navegador moderno (PC, tablet ou celular). O jogo funciona 100% offline.
- Navegação: faça suas escolhas clicando nos botões de ação de cada cena.
- Inventário e Exame: itens coletados aparecem na tabela de inventário. Clique em "Examinar" para abrir o painel de detalhes do item.
- Pistas e Compartimentos: clique nos painéis expansíveis (como "Anotações do Dr. Ivo" e "Armário de Manutenção") para revelar informações e itens opcionais.
- Botão Voltar: localizado no rodapé das páginas de exploração e instruções, restaura o ponto imediatamente anterior (desfazendo a última escolha).
- Cabeçalho: permite acessar a qualquer momento "Início", "Instruções" ou "Reiniciar" (que leva de volta ao início da exploração no Laboratório).

3. LISTA DE PÁGINAS (14 ARQUIVOS HTML)
--------------------------------------
01. `index.html` — Tela inicial com apresentação da história e acesso ao jogo e às instruções.
02. `pages/instrucoes.html` — Explicação do objetivo, regras, funcionamento do botão Voltar e legenda dos ícones.
03. `pages/laboratorio.html` — Módulo 1 (Progresso 1/3, Oxigênio 90%, Inventário vazio). Contém pista opcional e opções iniciais.
04. `pages/engenharia-trancada.html` — Porta da Engenharia bloqueada por falta do Cartão de Acesso (Progresso 1/3, Oxigênio 85%).
05. `pages/laboratorio-cartao.html` — Laboratório após coletar o Cartão de Acesso (Progresso 1/3, Oxigênio 80%, Inventário: Cartão).
06. `pages/engenharia.html` — Módulo 2 aberto com o Cartão (Progresso 2/3, Oxigênio 65%, Inventário: Cartão).
07. `pages/comunicacoes-sem-energia.html` — Módulo 3 apagado por falta da Célula de Energia (Progresso 2/3, Oxigênio 55%, Inventário: Cartão).
08. `pages/engenharia-celula.html` — Engenharia após retirar a Célula de Energia e liberar o armário com o Manual (Progresso 2/3, Oxigênio 55%, Inventário: Cartão, Célula).
09. `pages/engenharia-manual.html` — Engenharia após coletar também o Manual de Frequências (Progresso 2/3, Oxigênio 50%, Inventário: Cartão, Célula, Manual).
10. `pages/comunicacoes.html` — Módulo 3 energizado, com as três opções de frequência para transmissão (Progresso 3/3, Oxigênio 35%, Inventário: Cartão, Célula).
11. `pages/comunicacoes-manual.html` — Módulo 3 energizado e com destaque da frequência correta indicada pelo Manual (Progresso 3/3, Oxigênio 35%, Inventário: Cartão, Célula, Manual).
12. `pages/vitoria.html` — Tela de conclusão de vitória (transmissão em 406,0 MHz recebida pela equipe de resgate).
13. `pages/fim-contaminacao.html` — Tela de conclusão de derrota por abertura do contêiner da Amostra K-7 no Laboratório.
14. `pages/fim-sinal.html` — Tela de conclusão de derrota por transmissão em frequência desativada e esgotamento da bateria.

4. ESTRUTURA DE PASTAS
----------------------
/
├── index.html
├── README.txt
├── pages/
│   ├── instrucoes.html
│   ├── laboratorio.html
│   ├── laboratorio-cartao.html
│   ├── engenharia-trancada.html
│   ├── engenharia.html
│   ├── engenharia-celula.html
│   ├── engenharia-manual.html
│   ├── comunicacoes-sem-energia.html
│   ├── comunicacoes.html
│   ├── comunicacoes-manual.html
│   ├── vitoria.html
│   ├── fim-contaminacao.html
│   └── fim-sinal.html
├── css/
│   ├── base.css
│   ├── layout.css
│   ├── components.css
│   ├── pages.css
│   └── animations.css
└── img/
    ├── cenas/
    │   ├── capa.jpg
    │   ├── laboratorio.jpg
    │   ├── porta-trancada.jpg
    │   ├── engenharia.jpg
    │   ├── comunicacoes-apagada.jpg
    │   ├── comunicacoes.jpg
    │   ├── vitoria.jpg
    │   ├── contaminacao.jpg
    │   └── fim-sinal.jpg
    └── icones/
        ├── cartao.jpg
        ├── celula.jpg
        ├── manual.jpg
        ├── laboratorio-ic.jpg
        ├── engenharia-ic.jpg
        ├── comunicacoes-ic.jpg
        ├── oxigenio.jpg
        └── progresso.jpg

5. CRÉDITOS DAS IMAGENS
-----------------------
Ilustrações de cenas e ícones gerados especialmente para o projeto com auxílio de IA generativa (Nano Banana), armazenados localmente em formato JPG para funcionamento offline.

6. OBSERVAÇÃO TÉCNICA (SEM JAVASCRIPT)
--------------------------------------
Este projeto foi construído exclusivamente com HTML5 semântico e CSS3 puro. Não há nenhuma linha de JavaScript (`<script>`, atributos `on*` ou `javascript:`): todo o controle de estados, inventário, seções expansíveis (`<details>/<summary>`) e modais de inspeção (`:target`) funciona apenas com recursos nativos de HTML e CSS.
