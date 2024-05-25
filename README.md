# DChat README

## Descrição

DChat é um aplicativo desenvolvido em Delphi que permite a interação com a API do ChatGPT da OpenAI. O aplicativo envia mensagens para o modelo ChatGPT e exibe as respostas, proporcionando uma interface de chat simples e funcional.

## Funcionalidades

- Enviar mensagens para a API do ChatGPT.
- Receber e exibir respostas do ChatGPT.
- Suporte para diferentes modelos de linguagem.
- Interface gráfica desenvolvida com VCL.

## Pré-requisitos

- Delphi 10.x ou superior
- Componente Indy para Delphi
- OpenSSL para Delphi (bibliotecas `libeay32.dll` e `ssleay32.dll`)

## Configuração

1. **Clonar o repositório**:
    ```sh
    git clone https://github.com/seu-usuario/DChat.git
    cd DChat
    ```

2. **Configurar a chave da API**:
    - No diretório `dproj/Win32/Debug/`, crie um arquivo chamado `OPENAIKEY.ini` com o seguinte conteúdo:
      ```ini
      [GERAL]
      CHAVE= coloque aqui sua secret Key
      ```

3. **Baixar e configurar as bibliotecas OpenSSL**:
    - Baixe as bibliotecas `libeay32.dll` e `ssleay32.dll` e coloque-as no diretório `dproj/Win32/Debug/`.

4. **Abrir o projeto no Delphi**:
    - Abra o Delphi e carregue o arquivo `.dproj` do projeto DChat.

## Uso

1. **Compilar e executar** o projeto no Delphi.
2. **Selecionar o modelo** desejado no combobox.
3. **Escrever a mensagem** no campo de texto "Enviar".
4. **Clicar no botão "Enviar"** para enviar a mensagem e receber a resposta do ChatGPT.

## Estrutura do Código

- **Interface (GUI)**:
  - `TfrmPrincipal` (Formulário Principal)
  - Painéis, Memo, ComboBox e Botão

- **Lógica**:
  - `btnEnviarClick`: Evento de clique do botão "Enviar".
  - `VerificaMensagemVazia`: Verifica se a mensagem está vazia.
  - `RetornaTexto`: Exibe a mensagem do usuário no Memo de retorno.
  - `RetornoMensagemChatGPT`: Processa a resposta do ChatGPT e exibe no Memo de retorno.
  - `EnviarMensagemChatGPT`: Envia a mensagem para a API do ChatGPT e retorna a resposta.
  - `LerArquivo`: Lê a chave da API do arquivo INI.

## Dependências

- **Indy Components**: Para realizar as requisições HTTP.
- **OpenSSL**: Necessário para conexões seguras. Certifique-se de que as bibliotecas `libeay32.dll` e `ssleay32.dll` estejam no diretório de execução do projeto.

## Contribuição

Contribuições são bem-vindas! Por favor, siga os passos abaixo:

1. **Fork** o repositório.
2. **Crie** uma nova branch:
    ```sh
    git checkout -b feature/nova-funcionalidade
    ```
3. **Commit** suas alterações:
    ```sh
    git commit -m 'Adicionar nova funcionalidade'
    ```
4. **Push** para a branch:
    ```sh
    git push origin feature/nova-funcionalidade
    ```
5. **Abra** um Pull Request.

## Licença

Este projeto está licenciado sob a Licença MIT - veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## Contato

Para mais informações, entre em contato com o autor:

- Nome: Lucas De Freitas Roberto
- Email: lucasfreitas.t.2@hotmail.com
