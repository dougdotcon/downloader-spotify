# Spotify Playlist Downloader

Um aplicativo baseado em Python que permite aos usuários baixar playlists do Spotify como arquivos MP3.

---

## Pré-requisitos

- **Python 3.8+**: Certifique-se de que o Python esteja instalado no seu sistema.
- **FFmpeg**: Necessário para processar os arquivos de áudio. Instale-o via gerenciador de pacotes ou baixe os binários pré-compilados (ex: `ffmpeg-master-latest-win64-gpl-shared`). Certifique-se de adicionar o `ffmpeg` ao PATH do seu sistema.

---

## Instalação

1. **Clone o Repositório**
   bash
   git clone https://github.com/seu-usuario/SpotifyPlaylistDownloader.git
   cd SpotifyPlaylistDownloader
   

2. **Instale as Dependências**
   Execute o seguinte comando para instalar os pacotes necessários:
   bash
   pip install Flask spotipy youtubesearchpython yt-dlp
   

3. **Configure as Credenciais do Spotify**
   O script requer credenciais de desenvolvedor do Spotify. Siga os passos abaixo:

   - Acesse o [Spotify Developer Dashboard](https://developer.spotify.com/dashboard/login).
   - Crie um novo aplicativo.
   - Copie o **Client ID** e o **Client Secret** fornecidos.
   - Crie um arquivo chamado `config.py` no diretório raiz com o seguinte conteúdo:

     python
     # config.py
     SPOTIPY_CLIENT_ID = 'seu_client_id'
     SPOTIPY_CLIENT_SECRET = 'seu_client_secret'
     SPOTIPY_REDIRECT_URI = 'http://localhost:8080/callback'
     

---

## Utilização

1. **Execute a Aplicação**
   Inicie o servidor web com o comando:
   bash
   python app.py
   

2. **Acesse a Interface**
   - Abra seu navegador e acesse `http://localhost:8080`.

3. **Baixe a Playlist**
   - Cole a URL da playlist do Spotify no campo indicado e pressione **"Enviar"**.
   - As músicas serão processadas e baixadas como arquivos MP3 no diretório do projeto.

---

## Solução de Problemas (Troubleshooting)

Se encontrar problemas, verifique o seguinte:

1. **Dependências**: Certifique-se de que todos os pacotes Python foram instalados corretamente (`pip list`).
2. **Credenciais**: Confirme que suas credenciais do Spotify em `config.py` estão corretas e são válidas.
3. **Aplicativo Spotify**: Garanta que o aplicativo está configurado corretamente no painel do desenvolvedor do Spotify (inclua `http://localhost:8080/callback` em URIs de redirecionamento).
4. **FFmpeg**: Verifique se o FFmpeg está instalado e acessível pela linha de comando do sistema.

---

## Contribuindo

Contribuições são bem-vindas! Para colaborar:

1. **Fork o Repositório.**
2. **Crie uma Branch para sua Feature.**
   bash
   git checkout -b feature/nova-feature
   
3. **Commit suas Alterações.**
   bash
   git commit -m "Adiciona nova feature"
   
4. **Push para a Branch.**
   bash
   git push origin feature/nova-feature
   
5. **Abra um Pull Request.**

---

## Licença

Este projeto está licenciado sob a **MIT License**. Consulte o arquivo `LICENSE` para mais detalhes.

---

**⚠️ Aviso Legal:** O uso deste script pode violar os Termos de Serviço do Spotify e do YouTube. Utilize-o por sua conta e risco.