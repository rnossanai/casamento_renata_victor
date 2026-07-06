# Site de Casamento — Renata & Victor 💚

Site estático pronto para rodar no **Vercel** conectado ao **GitHub**. Nenhuma configuração extra é necessária — o Vercel detecta sozinho que é um site estático.

## 📁 Estrutura do projeto

```
(raiz do repositório)
├── index.html          ← o site inteiro (texto, cores, tudo)
├── vercel.json         ← configuração do Vercel (já pronta, não precisa mexer)
├── README.md           ← este arquivo
└── images/
    ├── hero-capa.jpg       ← foto de capa (com os nomes e a data)
    ├── igreja.jpg          ← foto da Igreja Santa Teresinha (Cerimônia)
    ├── gnu.png             ← foto do Grêmio Náutico União (Recepção e Festa)
    ├── roma-1.jpg          ← polaroide 1 — Pedido de Casamento
    ├── roma-2.jpg          ← polaroide 2 — Sim (o anel)
    └── textura-papel.jpg   ← fundo da seção Programação e Localização
```

⚠️ **Importante:** o `index.html` e a pasta `images/` precisam ficar na **raiz** do repositório (não dentro de outra pasta), senão as fotos não carregam.

## 🚀 Como publicar (repositório já conectado ao Vercel)

1. Abra o seu repositório no GitHub.
2. Clique em **Add file → Upload files**.
3. Arraste para lá: `index.html`, `vercel.json` e a pasta `images/` inteira.
4. Clique em **Commit changes** (botão verde).
5. Pronto! O Vercel detecta o commit e faz o deploy sozinho em ~1 minuto.
   Acompanhe em https://vercel.com/dashboard — o link do site aparece no projeto (algo como `seu-projeto.vercel.app`).

Toda vez que você editar qualquer arquivo no GitHub e der **Commit**, o Vercel republica o site automaticamente. Não precisa fazer mais nada.

### Configuração no Vercel (só confira uma vez)

No painel do projeto no Vercel → **Settings → Build & Development Settings**:
- **Framework Preset:** `Other`
- **Build Command:** (vazio)
- **Output Directory:** (vazio)

Como é um site estático puro, não tem build — o Vercel só serve os arquivos.

## 🖼️ Como trocar as fotos depois

Todas as fotos ficam na pasta `images/`:

1. No GitHub, entre na pasta `images` do repositório.
2. **Add file → Upload files** e suba a foto nova **com exatamente o mesmo nome** do arquivo que quer substituir (ex: `hero-capa.jpg`).
3. Commit → o Vercel atualiza o site sozinho.

## 🎨 Como trocar os fundos (capa e localização)

Abra o `index.html` no GitHub (clique no arquivo → ícone de lápis ✏️).
Bem no comecinho, dentro de `<style>`, tem este bloco:

```css
/* ============================================================
   ⚙️ CONFIGURAÇÕES FÁCEIS DE EDITAR
   ============================================================ */
:root{
  --hero-image: url('images/hero-capa.jpg');         /* 📷 foto de capa */
  --venue-bg-image: url('images/textura-papel.jpg'); /* 📄 fundo da Programação e Localização */
  --venue-bg-size: 520px auto;                       /* tamanho da textura */
}
```

- **Trocar a capa:** suba a foto nova em `images/` e troque `hero-capa.jpg` pelo nome dela.
- **Trocar o fundo da localização:** mesma coisa, troque `textura-papel.jpg`.
- **Textura muito grande/pequena?** Mude o `520px` (número maior = textura maior).

Depois clique em **Commit changes** e o Vercel republica sozinho.

## ✏️ Outras coisas fáceis de mudar no index.html

Use Ctrl+F (buscar) no editor do GitHub:

- **Chave Pix:** busque `03731389037` (aparece em todos os presentes).
- **WhatsApp do RSVP:** busque `WHATS_NUMBER` (formato: 55 + DDD + número, só dígitos).
- **Mensagem do WhatsApp:** logo abaixo, na linha `const msg`.
- **Horários e textos da cerimônia/festa:** busque `Cerimônia Religiosa`.
- **Preços e nomes dos presentes:** busque o nome do presente (ex: `Zoëtry`).
- **Fotos dos presentes e dos locais:** são links da internet (Unsplash). Para usar fotos suas, suba em `images/` e troque o link `https://images.unsplash.com/...` por `images/nome-da-sua-foto.jpg`.

Qualquer dúvida, é só me chamar de volta no Claude que eu ajudo a editar. 💍
