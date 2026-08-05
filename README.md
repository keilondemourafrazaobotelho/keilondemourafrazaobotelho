<img src="https://capsule-render.vercel.app/api?type=waving&height=300&color=gradient&text=Keilon%202°%20DES%202026%20&fontSize=40&fontAlignY=40" />

💻 Estudante de Desenvolvimento de Software



## 🚀 Sobre mim

- 🌱 Estudando HTML, CSS e JavaScript
- 📚 Aprendendo Git e GitHub
- 🎯 Objetivo: Tornar-me Desenvolvedor Full Stack

## 📫 Contato

- Email: keilondemoura55@gmail.com
- Tel: (19) 99806-2561

## 💻 Tecnologias

<img src="https://skillicons.dev/icons?i=html,css,js,git,github,vscode" />



name: Generate Snake

on:
  schedule:
    - cron: "0 */12 * * *"

  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest

  steps:
      - uses: Platane/snk@v3
        with:
          github_user_name: SEUUSUARIO
          outputs: dist/github-contribution-grid-snake.svg
    - uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
