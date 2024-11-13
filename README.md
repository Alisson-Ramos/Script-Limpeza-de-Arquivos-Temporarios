
# Windows Temporary Files Cleaner Script

Este script em PowerShell foi criado por Alisson Santos em 12/11/2024 e é projetado para limpar arquivos temporários de todas as contas de usuário (ativas e inativas) em uma máquina com Windows 10 (versão 22H2).

## Funcionalidade

O script identifica todas as contas de usuário locais e acessa a pasta TEMP de cada uma para excluir arquivos e pastas desnecessários, liberando espaço em disco e melhorando o desempenho geral do sistema.

## Pré-requisitos

- **Sistema Operacional**: Windows 10 (versão 22H2)
- **Permissões**: É necessário executar o script com privilégios administrativos para que ele possa acessar as pastas TEMP de todos os usuários.
- **PowerShell**: Recomenda-se o uso do PowerShell 5.1 ou superior.

## Como usar

1. **Clone este repositório** ou copie o script diretamente em um arquivo com extensão `.ps1`, como `limpeza_temp.ps1`.
2. **Execute o PowerShell como Administrador**.
3. Navegue até o diretório onde o script está salvo e execute o comando:
    ```powershell
    .\limpeza_temp.ps1
    ```

O script exibirá mensagens para cada usuário:
- **Cyan**: Indica que o processo de limpeza foi iniciado para o perfil do usuário.
- **Green**: Limpeza concluída com sucesso.
- **Yellow**: Pasta TEMP não encontrada para o perfil do usuário.
- **Red**: Indica um erro ao tentar limpar a pasta TEMP do perfil.

## Observações

- Este script utiliza o `Get-WmiObject` para listar os perfis de usuário, excluindo perfis especiais.
- O parâmetro `-ErrorAction SilentlyContinue` é usado para ignorar erros de permissão em arquivos que não podem ser excluídos.
- **Atenção**: Use este script com cautela, pois ele remove todos os arquivos e pastas na pasta TEMP de cada usuário.

## Contribuições

Se desejar aprimorar o script ou relatar problemas, sinta-se à vontade para abrir uma issue ou um pull request.
