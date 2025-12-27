# Spotify Playlist Downloader

A Python-based application that enables users to download Spotify playlists as MP3 files.

---

## Prerequisites

- **Python 3.8+**: Ensure Python is installed on your system.
- **FFmpeg**: Required for processing audio files. Install it via your package manager or download the pre-compiled binaries (e.g., `ffmpeg-master-latest-win64-gpl-shared`). Ensure `ffmpeg` is added to your system's PATH.

---

## Installation

1. **Clone the Repository**
   bash
   git clone https://github.com/seu-usuario/SpotifyPlaylistDownloader.git
   cd SpotifyPlaylistDownloader
   

2. **Install Dependencies**
   Execute the following command to install the necessary packages:
   bash
   pip install Flask spotipy youtubesearchpython yt-dlp
   

3. **Configure Spotify Credentials**
   The script requires Spotify Developer credentials. Follow these steps:

   - Access the [Spotify Developer Dashboard](https://developer.spotify.com/dashboard/login).
   - Create a new application.
   - Copy the provided **Client ID** and **Client Secret**.
   - Create a file named `config.py` in the root directory with the following content:

     python
     # config.py
     SPOTIPY_CLIENT_ID = 'your_client_id'
     SPOTIPY_CLIENT_SECRET = 'your_client_secret'
     SPOTIPY_REDIRECT_URI = 'http://localhost:8080/callback'
     

---

## Usage

1. **Run the Application**
   Start the web server with the command:
   bash
   python app.py
   

2. **Access the Interface**
   - Open your web browser and navigate to `http://localhost:8080`.

3. **Download a Playlist**
   - Paste the URL of the Spotify playlist into the input field and click **"Submit"**.
   - The tracks will be processed and downloaded as MP3 files in the project directory.

---

## Troubleshooting

If you encounter issues, please verify the following:

1. **Dependencies**: Ensure all Python packages are installed correctly (`pip list`).
2. **Credentials**: Confirm that your Spotify credentials in `config.py` are correct and valid.
3. **Spotify App**: Ensure the application is properly configured in the Spotify Developer Dashboard (ensure `http://localhost:8080/callback` is added as a Redirect URI).
4. **FFmpeg**: Verify that FFmpeg is installed and accessible via your system's command line.

---

## Contributing

Contributions are welcome! To collaborate:

1. **Fork the Repository.**
2. **Create a Feature Branch.**
   bash
   git checkout -b feature/new-feature
   
3. **Commit Your Changes.**
   bash
   git commit -m "Add new feature"
   
4. **Push to the Branch.**
   bash
   git push origin feature/new-feature
   
5. **Open a Pull Request.**

---

## License

This project is licensed under the **MIT License**. See the `LICENSE` file for details.

---

**⚠️ Disclaimer:** The use of this script may violate the Terms of Service of Spotify and YouTube. Use it at your own risk.