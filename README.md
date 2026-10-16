# Video Maker

Editor de vídeo para Windows e Linux, desenvolvido em Rust a partir do código aberto FilmCraft.

## Instalar

Na página **Releases** deste repositório, escolha o pacote adequado:

- **Windows (64 bits)**: `video-maker-*-windows-x64.msi`. Abra o instalador e siga as etapas.
- **Windows portátil**: `video-maker-*-windows-x64-portable.zip`. Extraia e execute `filmcraft.exe`.
- **Linux AppImage**: baixe `video-maker-*-linux-x86_64.AppImage`, marque como executável (`chmod +x arquivo.AppImage`) e execute.
- **Linux Debian/Ubuntu/Mint**: instale o pacote `.deb` com `sudo apt install ./arquivo.deb`.
- **Linux Fedora**: instale o `.rpm` com `sudo dnf install ./arquivo.rpm`.
- **Linux TAR.GZ**: extraia o conteúdo e consulte o `install.sh` incluído.

Os executáveis ainda utilizam internamente o nome `filmcraft` por compatibilidade técnica. A interface e o instalador são identificados como **Video Maker**.

## Como usar

1. Abra o Video Maker e crie um novo projeto.
2. Importe vídeos, imagens e trilhas de áudio pelo painel de mídia.
3. Arraste os arquivos para a linha do tempo.
4. Ajuste cortes e a posição dos clipes, adicione transições e títulos conforme os recursos disponíveis.
5. Use os painéis de efeitos, cor e áudio para refinar a edição.
6. Salve o projeto e exporte o vídeo pelo menu de exportação.

O suporte a formatos e efeitos depende da versão compilada e das capacidades do dispositivo. Faça um teste curto de exportação antes de iniciar um projeto importante.

## Publicar nova versão

1. Atualize `version` em `[workspace.package]` no `Cargo.toml` e sincronize o `Cargo.lock`.
2. Faça commit e `git push` na branch `main`.
3. Abra **Actions → Publicar Video Maker** e execute para a versão correspondente.
4. Após Windows e Linux compilarem sem erros, os pacotes serão anexados à página **Releases**.
5. Quem já instalou deve baixar e executar o novo instalador. Enviar `git push` não atualiza automaticamente instalações existentes.

## Desenvolvimento

Com o Rust correspondente à versão informada no projeto:

```bash
cargo build --release --locked -p filmcraft -p filmcraft-cli
```

Consulte `GUIA-RELEASE.md` para detalhes de compilação e publicação. As licenças e atribuições dos autores originais permanecem nos arquivos legais do projeto.
