# CLAUDE.md — CEATOX

Site gerado pelo **SF (Site Factory)** em 15/04/2026.

## Contexto do Site

**Nome:** CEATOX
**Nicho:** Saúde e Bem-estar
**Keywords:** O QUE E O CEATOX SP O CEATOX e o Centro de
**Paleta de cores:** rose | **Fonte:** playfair

O QUE É O CEATOX - SP O CEATOX é o Centro de Assistência Toxicológica do Instituto da Criança do Hospital das Clinicas da Faculdade de Medicina da Universidade de São Paulo. Criado em agosto de 1991, ele funciona 24 horas por dia no prédio do Instituto da Criança e se destina a fornecer informações específicas em caráter de urgência, a profissionais de saúde e população em geral, nas eventualidades de envenenamento, exposição a substâncias tóxicas, contaminação com defensivos agrícolas, acidentes com animais venenosos e reações adversas a medicamentos, via telefone, auxiliando no diagnóstico e tratamento. O CEATOX é composto por um grupo de profissionais de sáude, médicos, farmacêuticos, psicólogos e acadêmicos de medicina, farmácia-bioquímica, enfermagem e medicina veterinária, que para o atendimento das consultas utilizam vários bancos de dados, além de comunicação on-line com bancos internacionais. Mantém contato com outros Centros de Intoxicação e interage com o Sistema Nacional de Informações Toxicológicas – SINITOX da Fundação Oswaldo Cruz – FIOCRUZ do Ministério da Saúde. O QUE FAZEMOS ? O CEATOX fornece informações especializadas em casos de intoxicações agudas ou crônicas, acidentais, intencionais ou ocupacionais, causadas por medicamentos, produtos químicos, plantas, animais peçonhentos, drogas de abuso, alimentos, cosméticos, etc à médicos e outros profissionais de saúde e também à população em geral. O CEATOX analisa os casos de reações adversas a medicamentos, relatando-os posteriormente à Organização Mundial de Saúde, que atualmente conta com um banco de dados com mais de 2.000.000 de casos de reações adversas. A atividade educativa junto à população é realizada através de palestras, aulas e entrevistas a órgãos de divulgação no sentido de orientar a forma mais segura de utilização dos produtos químicos e cuidados para se evitar as intoxicações. Anualmente, no mês de maio, o CEATOX oferece um curso de Toxicologia Clínica, destinado principalmente aos profissionais da saúde. Este curso é ministrado a noite e tem a duração de uma semana. Tem como um dos objetivos a seleção de novos plantonistas.



## Componentes visuais usados

| Seção | Variante |
|-------|----------|
| Header | Header-F |
| Hero | Hero-J |
| Features | Features-J |
| About Section | About-F |
| Posts | Posts-J |
| Footer | Footer-A |
| Página Sobre | Sobre-C |
| Página Contato | Contato-J |

## Estrutura do projeto

```
src/
  sections/        # Layout escolhido pelo SF — Header, Hero, Features, About, Posts, Footer, Sobre, Contato
  data/            # JSONs com todo o conteúdo editável
  content/blog/    # Posts em Markdown
  pages/           # Rotas Astro (index, sobre, contato, blog, privacidade, termos)
  layouts/         # BaseLayout com fonte e cores dinâmicas
  styles/          # global.css com variáveis CSS de cor
public/
  images/          # hero.jpg, about.jpg, blog/*.jpg — inseridos automaticamente via Pexels
```

## O que editar

### Textos e conteúdo
- **`src/data/home.json`** — hero (título, subtítulo, botão), features (título, items), about section (título, desc, stats), posts
- **`src/data/sobre.json`** — conteúdo completo da página Sobre (hero, texto, missão)
- **`src/data/contato.json`** — título, subtítulo, email, tempo de resposta
- **`src/data/siteConfig.json`** — nome, slug, email, redes sociais, menu

### Imagens
Imagens já estão em `public/images/` (via Pexels). Para substituir, mantenha os mesmos nomes de arquivo:
- `hero.jpg` — imagem de fundo do Hero
- `about.jpg` — imagem da seção About (home)
- `sobre.jpg` — imagem de fundo da página Sobre
- `blog/{slug}.jpg` — imagens dos posts

### Posts do blog
Arquivos em `src/content/blog/`. Ajuste o tom de voz, adicione dados específicos do nicho e personalize conforme a identidade do site.

### Cores
Variáveis em `src/styles/global.css`: `--color-primary`, `--color-accent`, `--color-dark`.

## Deploy

```bash
bun install
bun run build
# Faça upload da pasta dist/ para Netlify, Vercel ou hosting estático
```
