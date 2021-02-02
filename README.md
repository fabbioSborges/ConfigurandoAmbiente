# Configurando Ambiente de Desenvolvimento

Software que vamos utilizar!!
- Visual Studio Code (https://code.visualstudio.com/download)

## Tema Visual Studio Code

### Instalar a extensão Dracula 

  Name: Dracula Official
  
    Id: dracula-theme.theme-dracula
    Description: Official Dracula Theme. A dark theme for many editors, shells, and more.
    Version: 2.22.3
    Publisher: Dracula Theme
    VS Marketplace Link: https://marketplace.visualstudio.com/items?itemName=dracula-theme.theme-dracula

  *Aplicando o tema*
    
  preferences -> Color Scheme -> Dracula
    
    
### Configurando VSCode
  
  Digitar ctrl+Shift+P e escrever settings(json) na barra
  
    {
      "workbench.colorTheme": "Dracula",
      "editor.fontSize": 18,
      "editor.lineHeight": 24,
      "workbench.iconTheme": "vscode-icons",
      "editor.formatOnSave": true, //formatar e endentar o arquivo
      "editor.rulers": [
          80,
          120
      ], // define o espaçamento horizontal 
      "editor.tabSize": 2,
      "editor.renderLineHighlight": "gutter",
      "terminal.integrated.fontSize": 14,
      "emmet.syntaxProfiles": {
          "javascript": "jsx", //autocomplete js
      },
      "emmet.includeLanguages": {
          "javascript": "javascriptreact"
      },
      "javascript.updateImportsOnFileMove.enabled": "never", // previne que o editor altere os imports
      "breadcrumbs.enabled": true, //arvores de pastas do arquivo,
      "editor.parameterHints.enabled": false, //evita mostrar a documentação da função
    }
  

### Instalando plugins
      
  Instalar a extensão vcCode Icons 
  
    Name: vscode-icons
    Id: vscode-icons-team.vscode-icons
    Description: Icons for Visual Studio Code
    Version: 11.1.0
    Publisher: VSCode Icons Team
    VS Marketplace Link: https://marketplace.visualstudio.com/items?itemName=vscode-icons-team.vscode-icons
  
  Instalar previo da cor
    
    Color Highlight 
    Name: Color Highlight
    Id: naumovs.color-highlight
    Description: Highlight web colors in your editor
    Version: 2.3.0
    Publisher: Sergii Naumov
    VS Marketplace Link: https://marketplace.visualstudio.com/items?itemName=naumovs.color-highlight
  
  Editor Config for Cs Code
    
    Configurar o editor entre todos os desenvolvedores do time
    Name: EditorConfig for VS Code
    Id: editorconfig.editorconfig
    Description: EditorConfig Support for Visual Studio Code
    Version: 0.16.4
    Publisher: EditorConfig
    VS Marketplace Link: https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig
    
  ESLint
    
    Garanti manter padrões de codigo dentro do projeto
    Name: ESLint
    Id: dbaeumer.vscode-eslint
    Description: Integrates ESLint JavaScript into VS Code.
    Version: 2.1.14
    Publisher: Dirk Baeumer
    VS Marketplace Link: https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint

  Prettier - code formater

    Garantir que as regras do eslint sejam aplicadas no cdigo. 
    Name: Prettier - Code formatter
    Id: esbenp.prettier-vscode
    Description: Code formatter using prettier
    Version: 5.8.0
    Publisher: Prettier
    VS Marketplace Link: https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode
    
    Adiconar a linha abaixo nas configuraçoes Digitar ctrl+Shift+P e escrever settings(json) na barra
      "prettier.eslintIntegration":true,
    
    
    
  
    
    
    
