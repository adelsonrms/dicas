Na pagina de informações de contas (Win+I) há uma sessão logo abaixo das informações da conta da Microsof há uma sessão de informações do Xbox.
Nao sou gamer e nao quero ver isso toda vez que entrar nessa pagina.
Como remover ?

![image](https://github.com/user-attachments/assets/13f33bd0-7bc7-4903-a303-c633f8c1c4cc)

Segue instruções conforme ChatGPT

1. Editar o Registro do Windows
⚠️ Atenção: Alterar o registro pode causar problemas no sistema se não for feito corretamente. Faça um backup do registro antes de prosseguir:

Pressione Win + R, digite regedit, e pressione Enter.
Navegue até a seguinte chave:

``HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AccountSettings``

Se não encontrar essa chave, procure por algo semelhante relacionado ao Xbox ou Game Pass.

#2. Usar Política de Grupo (Pro Edition)
   
Se você tiver o Windows 11 Pro:

Pressione Win + R, digite gpedit.msc, e pressione Enter.
Navegue até:
Configuração do Computador > Modelos Administrativos > Componentes do Windows > Experiências do Usuário Conectado e Telemetria.
Localize a configuração Permitir o conteúdo da nuvem no painel de configurações e defina-a como Desativado.
3. Bloquear Integrações com Serviços Online
Para versões Home ou outras que não possuem o Editor de Política de Grupo, bloqueie a integração usando o registro:

Vá para:
plaintext
Copiar código
HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows
Crie uma nova chave chamada CloudContent.
Dentro dela, crie um valor DWORD (32 bits) chamado DisableSoftLanding e defina o valor como 1.
4. Remover Conexões da Conta Microsoft
Se ainda aparecer:

Vá para Configurações > Contas > Suas informações.
Verifique se você está conectado com uma conta Microsoft. Mude para uma conta local para evitar integrações indesejadas.
5. Considerações Finais
Mesmo aplicando esses passos, a seção pode reaparecer após atualizações futuras. Neste caso, é necessário repetir os ajustes ou usar ferramentas de customização do sistema, como o ExplorerPatcher ou o Winaero Tweaker, para ocultar elementos indesejados.

Se precisar de mais ajuda, posso detalhar qualquer etapa!
