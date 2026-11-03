# AgentHub — instaladores

Aqui ficam só os instaladores do AgentHub para Windows e o feed de atualização automática (`latest.json`). O código-fonte é privado.

## Instalar

1. Abra a [última Release](https://github.com/andrewmautone/agenthub-releases/releases/latest).
2. Baixe `AgentHub_<versão>_x64-setup.exe` e execute. Não pede permissão de administrador: instala só para o seu usuário.

O Windows SmartScreen pode avisar que o instalador não é reconhecido, porque ele não tem assinatura de código da Microsoft. Clique em **Mais informações → Executar assim mesmo**.

## Atualizações

O AgentHub procura versões novas ao abrir e a cada 6 h. Também dá para procurar em **Configurações → Atualizações**. Nada é instalado sem a sua confirmação, porque atualizar reinicia o app e fecha todas as abas.

Os pacotes são assinados (minisign/Tauri). O app só instala uma atualização se a assinatura bater com a chave pública embutida nele.

## Desinstalar

Use **Configurações do Windows → Aplicativos → AgentHub → Desinstalar**. Seus dados em `%USERPROFILE%\.agenthub` (projetos, memória, wiki, histórico) **não são apagados**.
