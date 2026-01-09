# 🌐 WebSource Downloader API

An async FastAPI service that downloads a website's source files (HTML,
CSS, JS, images, fonts, media), packs them into a ZIP file, and provides
a temporary download link.

[![Deploy with
Vercel](https://vercel.com/button)](https://vercel.com/new/clone)

------------------------------------------------------------------------

## ✨ Features

-   ⚡ FastAPI + uvloop for high performance
-   📦 Downloads full webpage resources
-   🗜️ Auto ZIP archive generation
-   ⏳ Temporary download links with auto cleanup
-   🛡️ Size limits to prevent abuse
-   🌍 Works behind proxy / reverse proxy

------------------------------------------------------------------------

## 🧰 Requirements

-   Python 3.11+
-   See `requirements.txt` for dependencies

------------------------------------------------------------------------

## 📦 Installation

``` bash
git clone https://github.com/abirxdhack/SmartWebDL
python -m venv venv
source venv/bin/activate
pip3 install -r requirements.txt
```

------------------------------------------------------------------------

## ▶️ Run Server

``` bash
python3 api.py
```

Server runs on:

    http://0.0.0.0:3648

------------------------------------------------------------------------

## 🔌 API Usage

### 🌐 Download Website

    GET /api/web?url=https://example.com

Response:

``` json
{
  "success": true,
  "file_id": "xxxx",
  "download_url": "http://host/download/xxxx",
  "expires_in_seconds": 300
}
```

------------------------------------------------------------------------

### 📥 Download ZIP

    GET /download/{file_id}

Files expire automatically after a few minutes.

------------------------------------------------------------------------

## ⚠️ Notes

-   Large websites may be partially downloaded due to size limits.
-   Files are deleted automatically after expiry.
-   Intended for educational and testing purposes only.

------------------------------------------------------------------------

## 👤 Credits

-   👨‍💻 API Dev: **@ISmartCoder**\
-   📢 Updates: **@abirxdhackz**
