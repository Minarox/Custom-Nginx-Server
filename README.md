# Simple custom Nginx server

This repository provides a simple, up to date, Nginx Docker image configured with a custom `default.conf`.

## 🚀 Quick Start

- With Docker:

```bash
docker run --name custom-nginx-server -p 80:80 -v $(pwd):/usr/share/nginx/html:ro -d minarox/custom-nginx-server
```

- With Docker Compose:

```yaml
version: '3.8'
services:
  custom-nginx-server:
    container_name: custom-nginx-server
    image: minarox/custom-nginx-server
    ports:
      - "80:80"
    volume:
      - ./:/usr/share/nginx/html:ro
```

## ⚙️ Build custom image

- Edit `default.conf` as needed.
- Build the Docker image:

```bash
docker build -t minarox/custom-nginx-server .
```

- Run the container as shown above.

## 📚 Files

- `Dockerfile`: Builds the Nginx image and copies the config.
- `default.conf`: Nginx configuration file.

## 💼 License

MIT © [Mathis Serrieres Maniecki](https://github.com/Minarox)
