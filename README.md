# Chá de Casa Nova · Damaris e Lucas

Aplicativo web (HTML, CSS e JavaScript). Não precisa instalar nada e não pede cadastro dos convidados.

**Passo a passo do convidado:** capa → 1 Local → 2 Presentes → 3 Bingo → 4 Confirmar (WhatsApp) → 5 Lembrete.
Depois que o convidado diz que enviou a mensagem, o app avança sozinho para o lembrete (calendário com aviso 1 dia e 2 horas antes).

## Arquivos

```
index.html          ← o site (página única)
css/style.css       ← cores e visual
js/config.js        ← AQUI você edita link da Havan, WhatsApp, endereço etc.
js/app.js           ← funcionamento do app
img/                ← logo e flores
```

## Publicar no GitHub Pages (grátis)

1. Entre em https://github.com (crie a conta, se precisar).
2. Toque em **+** (canto superior) → **New repository**.
3. Em **Repository name** escreva `cha-casa-nova`. Deixe **Public** marcado. Toque em **Create repository**.
4. Na página que abrir, toque em **uploading an existing file**.
5. No computador, abra o zip e **arraste para o GitHub o conteúdo da pasta**: o arquivo `index.html` e as pastas `css`, `js` e `img`. O `index.html` precisa ficar na raiz, não dentro de outra pasta.
6. Toque em **Commit changes**.
7. Vá em **Settings** → **Pages** (menu lateral).
8. Em **Build and deployment**, escolha **Deploy from a branch**. Em **Branch**, escolha `main` e a pasta `/ (root)`. Toque em **Save**.
9. Espere de 1 a 3 minutos e atualize a página. O endereço aparece no topo:
   `https://SEU-USUARIO.github.io/cha-casa-nova/`
10. Abra no celular, teste os botões e envie o link aos convidados.

## O que você pode editar depois (arquivo `js/config.js`)

| Campo | Para que serve |
|---|---|
| `COVER_STYLE` | 1ª tela: `"classica"` (a atual) ou `"casa"` (convite com telhado). |
| `HAVAN_LIST_URL` | Link da lista de presentes da Havan. Vazio = mostra "disponível em breve". |
| `WHATSAPP_NUMBER` | Número que recebe as confirmações (só números, com 55 + DDD). |
| `WHATSAPP_MESSAGE` | Mensagem pronta que o convidado envia. |
| `EVENT_ADDRESS` | Endereço usado no mapa, na rota e no botão de copiar. |
| `EVENT_DATE_ISO` | Data e hora do evento (usada na contagem e no lembrete). |
| `EVENT_DURATION_HOURS` | Duração, só para o calendário do convidado. |
| `GIFT_CATEGORIES` | Categorias e exemplos de presentes. |

**Como editar direto no GitHub:** abra o arquivo (`js` → `config.js`), toque no ícone de lápis, mude o valor entre aspas e toque em **Commit changes**. O site atualiza em 1 a 2 minutos.

Textos fixos (nomes, "05/12/2026", "16h") estão no `index.html`. As cores estão no começo do `css/style.css`.

## Sobre os lembretes

O site não envia mensagens sozinho (isso exige um serviço pago de WhatsApp). O que ele faz:
- salva o lembrete no calendário do convidado (aviso 1 dia e 2 horas antes);
- abre o WhatsApp com um texto de lembrete pronto para o convidado guardar ou compartilhar.

Para lembrar os convidados, vocês podem mandar as mensagens prontas do guia por uma **lista de transmissão** do WhatsApp.
