# fidalGO TV para LG webOS

Aplicativo nativo de IPTV, Filmes, Séries e Animes para TVs **LG webOS (4.0 ou superior)**, baseado no [`lennylxx/webos-iptv-player`](https://github.com/lennylxx/webos-iptv-player) e pré-configurado com as listas brasileiras e os 11 addons do **fidalGO TV**.

## O que já vem pronto ao abrir na TV LG

- **353+ Canais Brasileiros Ao Vivo** (TV Aberta, Esportes, Filmes e Séries, Infantil, Notícias, Documentários, Variedades, 24 Horas e Música) com failover multi-fonte e proxy HLS no servidor fidalGO.
- **Filmes, Séries e Animes** resolvidos via servidor fidalGO usando os 11 addons configurados:
  - `BsCine`, `Zeus`, `PleiadesStream` (Animes & Doramas), `AnimeStream`, `FenixFlix`, `FrostStream`, `BestCine`, `PenguPlay`, `SuperStream`, `UnioFlix` e `MagnetFlix`.
- **Interface 100% em Português (Brasil)**, suporte nativo ao controle Magic Remote, D-Pad, Busca global, Lista de desejos, Continuar assistindo e legendas.

## Instalar na TV LG via Homebrew Channel

1. Na TV LG, abra o **Homebrew Channel**.
2. Vá em **Settings (Configurações)** → **Add repository (Adicionar repositório)**.
3. Informe a URL abaixo:

```text
https://raw.githubusercontent.com/SEU_USUARIO/fidalgo-webos-lg/main/homebrew-repository.json
```

4. Volte para a lista de aplicativos do Homebrew Channel, procure **fidalGO TV** e clique em **Install (Instalar)**.
5. Abra o **fidalGO TV** na TV — sua lista **fidalGO TV** (`https://fidalgotv.ngrok.app`) já vem conectada automaticamente na primeira abertura.

> Sempre que uma nova versão (`tag v*`) for publicada neste repositório, o GitHub Actions gera automaticamente o pacote `.ipk` e o `.manifest.json` no GitHub Releases para atualização direta pelo Homebrew Channel.

## Instalar manualmente via CLI (`ares-install`)

Baixe o arquivo `br.com.fidalgo.tv_<versao>_all.ipk` na aba **Releases** do GitHub e execute:

```bash
ares-install -d <nome-da-tv> br.com.fidalgo.tv_1.0.0_all.ipk
```

## Desenvolvimento local

```bash
npm install
npm run typecheck:all
npm run lint
npm test
npm run preview
```

## Créditos

Baseado no projeto open-source [lennylxx/webos-iptv-player](https://github.com/lennylxx/webos-iptv-player) (licença Apache-2.0).
