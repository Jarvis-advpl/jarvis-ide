# JARVIS IDE

IDE para AdvPL/TLPP (TOTVS Protheus) com agente JARVIS. Este repositório é **público só de distribuição**: instalador Windows, notas de versão e o feed de update. O código-fonte da IDE permanece privado.

## Download

1. Abra [Releases](https://github.com/jarvis-advpl/jarvis-ide/releases/latest) e baixe `JarvisUserSetup-x64-*.exe` (Windows 10/11, 64 bits).
2. Confira o SHA-256 publicado na release (e no portal da sua conta) com:

```powershell
Get-FileHash .\JarvisUserSetup-x64-*.exe -Algorithm SHA256
```

3. Instale **sem administrador** (`%LOCALAPPDATA%\Programs\JARVIS`).
4. Entre com o e-mail e a senha da conta JARVIS. Sem créditos o agente não gera código.

Quem já tinha o instalador antigo (NSIS em `Program Files\JARVIS`) deve desinstalá-lo uma vez. Updates seguintes aparecem **dentro** do JARVIS (Ajuda → Verificar atualizações), como no VS Code: aceitar, esperar o download e reiniciar. Não é preciso baixar o `.exe` de novo.

## Aviso do Windows (instalador ainda não assinado)

Este lançamento **não está assinado** (Authenticode). O SmartScreen pode mostrar “O Windows protegeu o PC” / editor desconhecido. Clique em **Mais informações → Executar assim mesmo** depois de conferir o SHA-256. PCs com AppLocker/GPO que bloqueiam executáveis não reconhecidos não conseguem furar esse aviso.

## Atualizações

O envelope consulta `https://jarvis-advpl.github.io/jarvis-ide/stable/win32/x64/user/latest.json` (GitHub Pages). Settings, login e workspace em `%APPDATA%\.jarvis-ide` permanecem após o update.

## Licenças de terceiros no envelope

- VSCodium / Code OSS — MIT
- tds-vscode — Apache-2.0 ([NOTICE](NOTICE.md))
- Skills AdvPL/TLPP TOTVS — MIT

EULA do conhecimento: [EULA-CONHECIMENTO.txt](EULA-CONHECIMENTO.txt).

## Segurança

Vulnerabilidades: veja [SECURITY.md](SECURITY.md).
