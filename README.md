# visualizar_wifi
visualizar a senha de uma rede Wi-Fi que está salva no seu notebook 



Se você precisa visualizar a senha de uma rede Wi-Fi que está salva no seu notebook Windows 10, mas não está conectado à rede no momento, você pode usar o Prompt de Comando (cmd) para obter essa informação. Aqui está como fazer:

1. **Abrir o Prompt de Comando**:
   - Pressione `Win + R` para abrir a caixa de diálogo "Executar".
   - Digite `cmd` e pressione Enter. Isso abrirá o Prompt de Comando.

2. **Listar Perfis de Rede Wi-Fi**:
   - No Prompt de Comando, digite o seguinte comando e pressione Enter:
     ```
     netsh wlan show profiles
     ```
   - Isso irá listar todos os perfis de rede Wi-Fi que estão salvos no seu computador.

3. **Visualizar a Senha de um Perfil de Rede Específico**:
   - Encontre o nome do perfil da rede Wi-Fi cuja senha você deseja visualizar. um exemplo, o nome da rede é  "ADM-TELECOM_5G".
   - Para visualizar a senha dessa rede, digite o seguinte comando no Prompt de Comando (substituindo `NomeDaRede` pelo nome do perfil da rede):
     ```
     netsh wlan show profile name="NomeDaRede" key=clear
     ```
     Por exemplo:
     ```
     netsh wlan show profile name="ADM-TELECOM_5G" key=clear
     ```

4. **Encontrar a Senha**:
   - Após executar o comando acima, procure a seção "Conteúdo da Chave" na saída do comando. Ao lado de "Conteúdo da Chave", você encontrará a senha da rede Wi-Fi.

Este comando permite que você visualize a senha de qualquer rede Wi-Fi salva no seu notebook Windows 10, mesmo que você não esteja atualmente conectado à rede. Certifique-se de executar o Prompt de Comando como administrador para garantir que tenha permissões suficientes para executar esses comandos.
