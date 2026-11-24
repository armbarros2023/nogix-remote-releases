# Nogix Remote — instaladores

Acesso remoto ao computador, com servidor próprio. Baixe a versão mais recente em **[Releases](https://github.com/armbarros2023/nogix-remote-releases/releases/latest)**.

| Sistema | Arquivo |
|---|---|
| Windows (instalador) | `nogixremote-<versão>-x86_64.msi` |
| Windows (portátil) | `nogixremote-<versão>-x86_64.exe` |
| macOS Apple Silicon (M1 em diante) | `nogixremote-<versão>-aarch64-mac.zip` |
| macOS Intel | `nogixremote-<versão>-x86_64-mac.zip` |
| Linux Debian/Ubuntu | `nogixremote-<versão>-x86_64.deb` |
| Linux Fedora/openSUSE | `nogixremote-<versão>-x86_64.rpm` / `-suse.rpm` |

Os instaladores ainda não têm assinatura digital.
- **Windows:** se aparecer "O Windows protegeu o computador", clique em **Mais informações → Executar assim mesmo**.
- **macOS:** abra o .zip (vira o app NogixRemote), arraste o **NogixRemote** para a pasta Aplicativos e abra. Quando aparecer o aviso de que a Apple não pôde verificar o app, abra **Ajustes do Sistema → Privacidade e Segurança**, desça até a mensagem sobre o NogixRemote e clique em **Abrir Mesmo Assim**. Depois, permita **Gravação de Tela** e **Acessibilidade** quando o app pedir.

- **macOS, se aparecer "danificado" (recomendado):** cole este comando no Terminal. Ele baixa direto, sem a marca de quarentena que o macOS bloqueia, instala em Aplicativos e abre o app (Apple Silicon):

  ```
  curl -L -o /tmp/nogix.zip https://github.com/armbarros2023/nogix-remote-releases/releases/latest/download/nogixremote-1.5.3-aarch64-mac.zip && ditto -x -k /tmp/nogix.zip /Applications && xattr -cr /Applications/NogixRemote.app && open /Applications/NogixRemote.app
  ```

  Para Mac Intel, troque `aarch64` por `x86_64`.

Instale a mesma versão nos dois computadores: os dois precisam usar o servidor do Nogix Remote para se encontrar.

## Licença e código-fonte

O Nogix Remote é baseado no [RustDesk](https://github.com/rustdesk/rustdesk) © Purslane Ltd., distribuído sob a licença [AGPL-3.0](https://www.gnu.org/licenses/agpl-3.0.html). O Nogix Remote também é distribuído sob a AGPL-3.0.

Quem recebeu o Nogix Remote tem direito ao código-fonte correspondente, com as modificações. Para pedir, abra uma [issue neste repositório](https://github.com/armbarros2023/nogix-remote-releases/issues/new?title=Pedido%20de%20c%C3%B3digo-fonte) informando a versão.

`update.json` é lido pelo próprio app para avisar quando há versão nova.
