# Publicar Video Maker no GitHub

1. Envie os arquivos deste pacote para um clone Git válido de `https://github.com/DisneyMjr/VIDEO-MAKER`, preservando `.git`.
2. Execute `git add .`, `git commit -m "Video Maker instaladores"`, `git push origin main`.
3. Acesse Actions e rode **Gerar MSI Video Maker** ou **Gerar Linux Video Maker** para testar os pacotes.
4. Depois dos testes passarem, execute **Publicar Video Maker** e informe exatamente `0.8.0` (versão atual de `Cargo.toml`).
5. Somente se ambos os builds passarem, os pacotes são publicados juntos em GitHub Releases.
6. Para uma nova versão, incremente `[workspace.package].version` em `Cargo.toml`, execute `cargo update --workspace` para sincronizar `Cargo.lock`, revise o número de versão do app e faça novo commit. Publicar novamente a mesma versão é bloqueado.

**ATENÇÃO:** `git push` não atualiza programas instalados. Quem usa MSI ou pacotes Linux precisará instalar a nova versão manualmente. Não há atualização automática implementada.

A compilação Windows requer WiX 5; Linux instala dependências nativas e nfpm. Se o GitHub Actions falhar, abra o log do job correspondente. O projeto ainda não foi testado em runners do GitHub neste pacote.

As licenças, copyright e atribuições dos autores originais devem permanecer no repositório.
