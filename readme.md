# Downloader Spotify

Baixe playlists do Spotify em formato MP3 usando este script em Python.

---

## Requisitos

- **Python 3.8+**
- **FFmpeg**: Necessário para processar os arquivos de áudio. Utilize o pacote `ffmpeg-master-latest-win64-gpl-shared` ou instale pelo seu gerenciador de pacotes.

---

## Instalação

1. **Clone o Repositório**
   ```bash
   git clone https://github.com/seu-usuario/downloader-spotify.git
   cd downloader-spotify
   ```

2. **Instale as Dependências**
   Execute o seguinte comando para instalar os pacotes necessários:
   ```bash
   pip install Flask spotipy youtubesearchpython yt-dlp
   ```

3. **Configure as Credenciais do Spotify**
   O script requer credenciais de desenvolvedor do Spotify para funcionar corretamente. Siga os passos abaixo:

   - Acesse o painel de desenvolvedores do Spotify: [Spotify Developer Dashboard](https://developer.spotify.com/dashboard/login).
   - Crie um novo aplicativo.
   - Copie o **Client ID** e o **Client Secret** fornecidos.
   - Adicione as credenciais ao arquivo de configuração `config.py`:

     ```python
     # config.py
     SPOTIPY_CLIENT_ID = 'seu_client_id'
     SPOTIPY_CLIENT_SECRET = 'seu_client_secret'
     SPOTIPY_REDIRECT_URI = 'http://localhost:8080/callback'
     ```

---

## Utilização

1. **Execute o Script**
   Inicie a aplicação com o comando:
   ```bash
   python app.py
   ```

2. **Acesse o Navegador**
   - Abra [http://localhost:8080](http://localhost:8080) no seu navegador.

3. **Baixe a Playlist**
   - Cole a URL da playlist do Spotify no campo indicado e pressione o botão **"Enviar"**.
   - As músicas serão baixadas como arquivos MP3 na pasta onde o script está localizado.

---

## Troubleshooting

Caso encontre problemas, siga estas etapas:

1. Verifique se todas as dependências foram instaladas corretamente.
2. Confirme que suas credenciais do Spotify estão configuradas e válidas.
3. Certifique-se de que o aplicativo foi criado corretamente no painel do desenvolvedor do Spotify.
4. Verifique se o FFmpeg está instalado e configurado corretamente no sistema.

---

## Contribuindo

Contribuições são bem-vindas! Para colaborar:

1. **Fork o Repositório.**
2. **Crie uma Branch para sua Feature.**
   ```bash
   git checkout -b feature/sua-feature
   ```
3. **Commit suas Alterações.**
   ```bash
   git commit -m "Adiciona nova feature"
   ```
4. **Push para a Branch.**
   ```bash
   git push origin feature/sua-feature
   ```
5. **Abra um Pull Request.**

---

## Licença

Este projeto está licenciado sob a **MIT License**. Consulte o arquivo `LICENSE` para mais informações.

---

**Atenção:** O uso deste script pode violar os Termos de Serviço do Spotify e do YouTube. Utilize-o por sua conta e risco.
