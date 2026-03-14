# Pesquisa Culturama

Este é um projeto de formulário de pesquisa para a Culturama, desenvolvido como parte de um curso da Alura. O formulário coleta dados pessoais, perfil, hábitos e comentários dos usuários sobre serviços culturais.

## Funcionalidades

- Formulário de coleta de dados pessoais (nome, idade, data de nascimento, e-mail, telefone, foto)
- Seleção de gênero e estado civil
- Escolha de estado e cidade
- Preferências de redes sociais, estilo musical e cor favorita
- Avaliação da qualidade do serviço com comentários
- Confirmações de participação e recebimento de resultados por e-mail
- Página de sucesso após envio

## Estrutura do Projeto

```
pesquisa-culturama/
├── index.html          # Página principal com o formulário
├── sucesso.html        # Página de confirmação de envio
├── css/
│   ├── style.css       # Estilos para o formulário
│   └── sucesso.css     # Estilos para a página de sucesso
└── img/                # Imagens (logo, favicon, etc.)
```

## Como Executar

1. Abra o arquivo `index.html` em um navegador web.
2. Preencha o formulário e clique em "Enviar".
3. Você será redirecionado para a página de sucesso.

## Tecnologias Utilizadas

- HTML5
- CSS3
- Google Fonts (Fjalla One e Work Sans)

## Validação

O formulário inclui validações básicas:
- Campos obrigatórios (nome, idade, e-mail, telefone, estado, aceitação dos termos)
- Formato de e-mail e telefone
- Limite de idade (12-100 anos)

## Acessibilidade

O projeto implementa várias funcionalidades de acessibilidade para garantir que o formulário seja utilizável por pessoas com deficiências:

- **Estrutura Semântica**: Uso de elementos HTML semânticos como `<main>`, `<header>`, `<section>`, `<fieldset>` e `<legend>` para organizar o conteúdo de forma lógica.
- **Labels Associados**: Todos os campos de entrada possuem labels com o atributo `for` correspondente ao `id` do input, facilitando a navegação por leitores de tela.
- **Atributos ARIA**: 
  - `aria-describedby` para associar descrições auxiliares a campos específicos (telefone e upload de foto).
  - `aria-label` nos botões para descrever sua função.
  - `role="alert"` na página de sucesso para anunciar mensagens importantes aos leitores de tela.
- **Texto Alternativo**: Imagens possuem atributo `alt` com descrições adequadas.
- **Atributo Lang**: O idioma da página é definido como português brasileiro (`lang="pt-br"`).
- **Tipos de Input Adequados**: Uso de tipos específicos como `email`, `tel`, `date`, `number`, `color` e `file` para melhorar a experiência em dispositivos móveis e assistivos.
- **Validação Visual**: Bordas vermelhas para campos inválidos e verdes para válidos, além de mensagens de ajuda.
- **Navegação por Teclado**: O formulário é totalmente navegável via teclado, com foco visível nos elementos interativos.
- **Contraste e Legibilidade**: Fontes e cores escolhidas para garantir boa legibilidade.

## Observações

- Este é um projeto estático sem backend; os dados do formulário são enviados via GET para a página de sucesso, mas não são processados ou armazenados.
- Para um projeto real, seria necessário implementar um servidor para processar os dados.