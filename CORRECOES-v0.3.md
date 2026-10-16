# Correções Video Maker v0.3

- Removidos 19 diretórios extras de VectorCraft, indevidamente misturados ao código-fonte do Video Maker. Esses módulos eram carregados pela expressão `crates/*`/`apps/*` e provocavam erros de dependências de workspace como `kurbo`, `image`, `flate2` e `crc32fast`.
- `Cargo.toml` passou a listar explicitamente os componentes do FilmCraft/Video Maker. Dessa forma, outros projetos copiados acidentalmente não passam a ser compilados.
- Todos os manifests `Cargo.toml` remanescentes foram verificados por parser TOML: nenhuma referência `workspace = true` carece de entrada em `[workspace.dependencies]`.
- Workflows Linux de build e de Release utilizam `actions/setup-go` e instalam o `nfpm` por `go install`; sem `/tmp/nfpm` ou URL 404.
- Scripts `.sh` foram normalizados para quebras de linha LF. Todos os scripts em `packaging/` passaram no teste `bash -n`.
- `.gitattributes` evita que Git para Windows converta `.sh` novamente para CRLF.

## Validação

Esta revisão validou manifests TOML e sintaxe de scripts shell. **Não foi possível compilar o binário Windows ou Linux neste ambiente**, portanto outros erros podem aparecer após o Cargo carregar o workspace corretamente.

## Atualização do repositório

Extraia este ZIP e copie o conteúdo de `VIDEO-MAKER` para um clone do repositório. Como as pastas de VectorCraft devem ser removidas, certifique-se de executar no clone:

```powershell
git rm -r --ignore-unmatch apps/vectorcraft apps/vectorcraft-cli apps/vectorcraft-web crates/affinity crates/brush crates/cad crates/doc crates/effects crates/eps crates/mcp crates/metafile crates/pathops crates/pdf crates/plugins crates/scriptcheck crates/svg crates/three-d crates/tools crates/trace

git add -A
git commit -m "Video Maker - limpar workspace e corrigir instaladores"
git push origin main
```

Confira antes do commit com `git status`; Git deve mostrar remoções das pastas VectorCraft e atualizações dos arquivos pertinentes.
