# Publicacao no GitHub Pages

Esta pasta `/docs` contem tudo que o GitHub Pages precisa para publicar o ebook interativo.

## Arquivos desta pasta

- `index.html`: ebook interativo publicado.
- `.nojekyll`: desativa o processamento Jekyll e publica o HTML estatico diretamente.
- `README-publicacao-github-pages.md`: instrucoes de configuracao e atualizacao.

## Configuracao recomendada no GitHub

Use a opcao:

- Source: `Deploy from a branch`
- Branch: `main`
- Folder: `/docs`

Com isso, o endereco final ficara no formato:

```text
https://SEU_USUARIO.github.io/NOME_DO_REPOSITORIO/
```

## Primeira publicacao pelo terminal

Se este projeto ainda nao estiver conectado a um repositorio GitHub:

> Observacao deste workspace: existe uma pasta `.git` vazia/invalida no projeto. Se `git status` ou `git init` falhar, remova essa pasta vazia antes de inicializar:
>
> ```bash
> rmdir .git
> ```

```bash
git init
git add .
git commit -m "Publica ebook interativo no GitHub Pages"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/NOME_DO_REPOSITORIO.git
git push -u origin main
```

Depois, no GitHub:

1. Abra o repositorio.
2. Va em `Settings`.
3. No menu lateral, clique em `Pages`.
4. Em `Build and deployment`, selecione `Deploy from a branch`.
5. Em `Branch`, selecione `main`.
6. Em `Folder`, selecione `/docs`.
7. Clique em `Save`.

O GitHub pode levar alguns minutos para publicar. Apos publicar, a pagina `Settings > Pages` mostrara o link do site.

## Atualizacao do ebook depois de editar

Sempre que o arquivo principal for editado em:

```text
ebook/ebook-interativo-controle-carga.html
```

atualize a versao publicada com:

```bash
cp ebook/ebook-interativo-controle-carga.html docs/index.html
git add ebook/ebook-interativo-controle-carga.html docs/index.html
git commit -m "Atualiza ebook interativo"
git push
```

## Observacoes importantes

- O GitHub Pages publica sites publicos na internet.
- Se usar GitHub Free, o repositorio precisa ser publico para Pages em repositorios comuns.
- Para este ebook, nao e necessario configurar build, Node, Vite ou React. E apenas HTML estatico.
- Nao envie o arquivo `.html` cru pelo WhatsApp como produto final; envie o link publicado.
