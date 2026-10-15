Postura de Tiro — Point IA Archery
Ferramenta de análise de postura de tiro no arco e flecha, rodando 100% no
navegador (MediaPipe Pose, 33 pontos). Nenhum vídeo é enviado a servidor —
tudo é processado localmente no dispositivo do usuário.
Como colocar no GitHub Pages
Crie um repositório novo (ou use um existente) e suba o arquivo
`index.html` na raiz.
No GitHub, vá em Settings → Pages.
Em Source, selecione a branch (geralmente `main`) e a pasta `/ (root)`.
Salve. Em alguns minutos o app estará disponível em:
`https://SEU-USUARIO.github.io/NOME-DO-REPO/`
Como o arquivo já se chama `index.html`, o GitHub Pages serve ele
automaticamente como página inicial — não precisa de mais nada.
Importante: MediaPipe exige HTTPS ou localhost
A detecção de esqueleto (MediaPipe Pose) só funciona quando a página é
aberta via `http://localhost` ou `https://`. O GitHub Pages já serve tudo
em HTTPS, então funciona normalmente assim que publicado.
Se quiser testar localmente antes de subir, não abra o arquivo com
duplo clique (`file://`). Em vez disso, na pasta do arquivo:
```bash
python3 -m http.server
```
e acesse `http://localhost:8000/index.html`.
Estrutura
`index.html` — aplicativo completo (HTML + CSS + JS em um único arquivo,
sem dependências de build). O único recurso externo é a biblioteca
MediaPipe Tasks Vision, carregada via CDN (`cdn.jsdelivr.net`).
