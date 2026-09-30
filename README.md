# Wisdom Mod Translator

Programa para traduzir mods do The Sims 4. Lê o texto das String Tables dentro de arquivos `.package`, guarda um dicionário para as próximas versões do mod e grava a tradução num pacote separado ou no mod aberto.

É um fork do [The Sims 4 Translator](https://github.com/voky1/sims4-translator), de voky1, sob a licença MIT. A ideia original vem do [xTranslator](https://www.nexusmods.com/skyrimspecialedition/mods/134).

## Requisitos

- Python 3
- Dependências do projeto

```bash
pip install -r requirements.txt
python main.py
```

## O que o programa traduz

O texto que o jogo mostra fica na String Table do `.package`. Para o cliente em português do Brasil, o destino é o idioma `POR_BR`.

Traduz-se o texto da frase. A chave da string e os tokens entre chaves, como `{0.SimFirstName}` e `{0.String}`, permanecem intactos. Dentro dos tokens de gênero, só o pronome muda: `{M0.He}` vira `{M0.Ele}`, `{F0.She}` vira `{F0.Ela}`.

Texto escrito direto num script `.ts4script` não passa por este programa.

## Recursos

- Dicionário local, para não retraduzir frases que não mudaram quando o mod atualiza.
- Gravação da tradução num `.package` separado, ou direto no mod aberto.
- Várias traduções reunidas num único arquivo.
- Tradução automática com Google e MyMemory. O DeepL entra na lista quando há uma chave de API nas opções.
- Tokens entre chaves ficam de fora da tradução automática.
- Importação e exportação em XML, no formato do DP STBL Editor, e em JSON ou binário do Sims 4 Studio.
- Tema claro e tema escuro.
- Interface já traduzida para português do Brasil.

## Como usar

1. Em **Opções**, escolha o idioma da interface e os idiomas de origem e destino. Para o jogo em português do Brasil, o destino é `POR_BR`.
2. Abra o mod (`.package`).
3. Traduza as linhas. Revise o texto automático antes de publicar.
4. Salve o dicionário se for atualizar esta tradução depois.
5. Salve a tradução num pacote separado para compartilhar, ou grave no mod aberto se for só para a sua pasta Mods.

Para publicar, distribua apenas o pacote da tradução, na mesma pasta do mod, e siga a política do autor. Reenviar o mod inteiro republica o trabalho de outra pessoa e entrega uma versão que envelhece no próximo update.

## Idioma da interface

Os textos da janela ficam em `prefs/interface/`. O português do Brasil está em `prefs/interface/brasil.xml` (tradução de luana67).

Para incluir outro idioma, coloque um XML novo nessa pasta.

## Fontes

- [Roboto](https://fonts.google.com/specimen/Roboto), licença [Apache 2.0](fonts/LICENSE-Roboto.txt).
- [JetBrains Mono](https://www.jetbrains.com/lp/mono/), licença [SIL Open Font License 1.1](fonts/LICENSE-JetBrains.txt).

## Licença

MIT. O aviso de copyright e o texto da licença estão em [LICENSE](LICENSE).
