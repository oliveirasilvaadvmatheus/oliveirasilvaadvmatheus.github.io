# Site — Matheus Oliveira Silva Advocacia

Site institucional de página única, em HTML e CSS puros, hospedado no GitHub Pages.
Sem framework, sem build, sem dependência de servidor.

Barueri/SP · OAB/SP 550.010

---

## Arquivos

| Arquivo | O que é |
|---|---|
| `index.html` | O site inteiro: estrutura, estilo e conteúdo num arquivo só |
| `foto-topo.jpg` | Retrato do topo — aparece só no desktop |
| `foto-sobre.jpg` | Retrato da seção "Sobre" — aparece em todas as telas |

Os três precisam estar na mesma pasta, com esses nomes exatos.

---

## Como publicar (pelo navegador, sem instalar nada)

Este é o caminho recomendado. Não precisa de Git nem de linha de comando.

1. Crie uma conta em [github.com](https://github.com), se ainda não tiver.
2. Clique em **New repository**. No campo **Repository name**, digite
   `SEU-USUARIO.github.io` — trocando `SEU-USUARIO` pelo nome de usuário exato
   da sua conta. O nome precisa bater; é isso que faz o site ir para o endereço curto.
3. Marque **Public** e clique em **Create repository**.
4. Na página que abrir, clique em **uploading an existing file** e arraste os três
   arquivos (`index.html`, `foto-topo.jpg`, `foto-sobre.jpg`). Clique em **Commit changes**.
5. Vá em **Settings → Pages**. Em **Source**, escolha **Deploy from a branch**;
   em **Branch**, escolha `main` e a pasta `/ (root)`. Clique em **Save**.

Em alguns minutos o site estará no ar em `https://SEU-USUARIO.github.io`,
com HTTPS e sem custo nenhum.

Para alterar o site depois, abra o arquivo no GitHub, clique no ícone de lápis,
edite e salve — a alteração entra no ar sozinha em poucos minutos.

### Alternativa: pela linha de comando

Se preferir trabalhar local, instale o [Git](https://git-scm.com/download/win) e rode
na pasta do site:

```bash
git init
git add .
git commit -m "Site institucional - versao inicial"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/SEU-USUARIO.github.io.git
git push -u origin main
```

Depois configure **Settings → Pages** como no passo 5 acima.

---

## Como alterar o conteúdo

Tudo fica no `index.html`. As seções estão marcadas por comentários em maiúsculas
(`<!-- ============ ÁREAS ============ -->`), então dá para achar cada parte pelo nome.

**Trocar uma foto:** substitua o arquivo `.jpg` mantendo o mesmo nome. Use imagens
verticais na proporção 4×5 ou mais altas — o corte é feito pelo CSS. Mantenha cada
arquivo abaixo de 200 KB para o site continuar abrindo rápido.

**Usar o logo em imagem:** o cabeçalho hoje reconstrói a marca em tipografia. Para usar
o arquivo original, salve-o como `logo-ms.png` na pasta e siga a instrução no comentário
`/* ---------- logo ---------- */`, dentro do `<style>`. Peça ao designer uma versão só
do quadrado com o monograma: a marca completa fica ilegível a 42px de altura.

**Adicionar um texto novo em "Seus direitos":** copie um bloco `<article class="art">`
inteiro, cole abaixo do último e troque o conteúdo. Mantenha a linha `<p class="lei">`
com a base legal e a `<p class="upd">` com o mês da atualização.

---

## Antes de publicar qualquer alteração

O site é material de publicidade e está sujeito ao **Provimento nº 205/2021** do
Conselho Federal da OAB. Ao mexer no conteúdo, mantenha:

- o nome completo e o número de inscrição na OAB visíveis no rodapé;
- o aviso de caráter informativo no rodapé;
- ausência de promessa de resultado, de valores de honorários, de casos de clientes
  e de termos de superioridade ("o melhor", "especialista nº 1", "líder").

Enquanto a pós-graduação estiver em andamento, o texto correto é **"cursando"** —
anunciar "especialista" sem o título concluído é irregular perante a OAB.

---

## Domínio próprio (opcional, depois)

Para migrar de `SEU-USUARIO.github.io` para um domínio próprio:

1. Registre o domínio (o `.adv.br` é feito no Registro.br e exige comprovação de
   inscrição na OAB).
2. Crie um arquivo chamado `CNAME` na raiz do repositório contendo só o domínio,
   numa linha, sem `https://`.
3. Aponte o DNS para o GitHub Pages e marque **Enforce HTTPS** em Settings → Pages.

Nada do site precisa ser refeito — os links internos são todos relativos.
