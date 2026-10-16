# Video Maker

**Video Maker** é um editor de vídeo não linear para Windows, Linux e macOS, construído em Rust a partir do projeto de código aberto FilmCraft.

## Para que serve

O Video Maker permite organizar vídeos, imagens e áudio em projetos, montar sequências na linha do tempo, editar cortes e transições, ajustar cores, trabalhar com títulos, legendas, efeitos e áudio e exportar o resultado final.

## Como começar

1. Instale o programa usando o pacote adequado ao seu sistema operacional.
2. Abra **Video Maker** e crie um projeto.
3. Importe os arquivos de vídeo, áudio ou imagem pelo painel de mídia.
4. Arraste os arquivos para a linha do tempo e organize a sequência.
5. Use as ferramentas de corte, ajuste e transição para montar o vídeo.
6. Abra os painéis de cor, efeitos, títulos ou áudio para refinar o projeto.
7. Salve o projeto frequentemente e use **Exportar** para gerar o vídeo final.

## Principais áreas

- **Projeto / mídia:** arquivos importados e organização por pastas.
- **Monitor de origem:** pré-visualização de um arquivo antes de inserir na edição.
- **Monitor do programa:** pré-visualização do resultado da sequência.
- **Linha do tempo:** várias trilhas de vídeo e áudio, cortes, transições e marcadores.
- **Efeitos e cor:** ajustes visuais e controles aplicáveis aos clipes.
- **Áudio:** níveis, mixagem e acompanhamento do som.
- **Exportação:** configurações do arquivo final, conforme formatos suportados pela compilação.

## Arquivos e compatibilidade

As opções de importação e exportação variam conforme o formato, o sistema e as funções disponíveis na versão instalada. Confirme as opções de codec na janela de importação ou exportação do próprio programa antes de iniciar um trabalho importante.

## Instaladores

- **Windows:** use um instalador `.msi` publicado para a versão.
- **Linux:** use `.AppImage`, `.deb` ou `.rpm` conforme a distribuição e os pacotes disponíveis.
- **macOS:** utilize um pacote de instalação compatível com seu sistema, quando disponibilizado.

Os arquivos neste repositório são **código-fonte**. A geração de instaladores exige compilar o projeto; baixar o ZIP do código não instala o programa.

## Compilar a partir do código-fonte

É necessário instalar Rust e as dependências nativas exigidas pelo projeto. Na raiz do repositório, execute:

```bash
cargo build --release -p filmcraft
```

O pacote e o executável internos continuam com o nome `filmcraft` para preservar a estrutura de compilação. O nome mostrado ao usuário é **Video Maker**.

## Limitações

O software está em desenvolvimento. Alguns recursos e formatos podem não estar totalmente disponíveis ou podem exigir dependências adicionais. Teste suas exportações antes de usar em projetos de produção.

## Licenças e créditos

Video Maker é uma personalização do projeto original FilmCraft. As licenças e créditos de autores e bibliotecas permanecem nos arquivos `LICENSE-MIT`, `LICENSE-APACHE`, `NOTICE` e `ATTRIBUTION.md`.
