# Plex to Last.fm Scrobbler

This project is a Python script that integrates Plex Media Server with Last.fm, allowing you to scrobble your music plays from Plex to your Last.fm account using the "Scrobbling now" feature that is missing from official Plex LastFm integration.

## Features

- Connects to Plex Media Server
- Authenticates with Last.fm
- Updates "Now Playing" status on Last.fm when a track starts playing on Plex
- Handles play, pause, and resume events from Plex

## Requirements

- Python 3.6+
- Plex Media Server
- Last.fm account
- Plex Webhook configured to send events to this script

## Installation

1. Clone this repository:
```
git clone https://github.com/yourusername/plex-lastfm-scrobbler.git
cd plex-lastfm-scrobbler
```

2. Install the required packages:
```
pip install -r requirements.txt
```

3. Create a `.env` file in the project root and add your configuration:
```
PLEX_URL=http://your-plex-server:32400
PLEX_TOKEN=your-plex-token
LASTFM_API_KEY=your-lastfm-api-key
LASTFM_API_SECRET=your-lastfm-api-secret
```

## Usage

1. Run the script:
```python plex_lastfm_scrobbler.py```

2. The script will prompt you to authorize the application with Last.fm if it's the first time running.

3. Configure your Plex Media Server to send webhooks to `http://your-ip:5000/webhook`

4. Play music on Plex, and it should now scrobble to Last.fm

## License

This project is licensed under the MIT License.
