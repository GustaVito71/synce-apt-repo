# SynCE APT Repository

Repositorio APT para los paquetes SynCE Legacy portados a Debian 12 Bookworm.

## Uso

```bash
# 1. Agregar la clave GPG
wget -qO- https://GustaVito71.github.io/synce-apt-repo/public.key \
  | sudo tee /etc/apt/trusted.gpg.d/synce.asc

# 2. Agregar el repositorio (requiere lsb-release: sudo apt install lsb-release)
echo "deb https://GustaVito71.github.io/synce-apt-repo $(lsb_release -sc 2>/dev/null) main" \
  | sudo tee /etc/apt/sources.list.d/synce.list

# 3. Actualizar e instalar
sudo apt update
sudo apt install synce-sync-engine
```

## Paquetes disponibles

| Paquete | Versión |
|---------|---------|
| `librtfcomp0` | 1.3-0~bookworm1 |
| `librtfcomp-dev` | 1.3-0~bookworm1 |
| `python3-rtfcomp` | 1.3-0~bookworm1 |
| `libmimedir0` | 0.5.1-0~bookworm1 |
| `libmimedir-dev` | 0.5.1-0~bookworm1 |
| `libsynce0` | 0.17-0~bookworm8 |
| `libsynce0-dev` | 0.17-0~bookworm8 |
| `python3-rapi2` | 0.17-0~bookworm8 |
| `synce-tools` | 0.17-0~bookworm8 |
| `synce-dccm` | 0.17-0~bookworm8 |
| `librra0` | 0.17-0~bookworm2 |
| `librra-dev` | 0.17-0~bookworm2 |
| `librra-tools` | 0.17-0~bookworm2 |
| `python3-rra` | 0.17-0~bookworm2 |
| `synce-sync-engine` | 0.16-0~bookworm2 |

## Agregar nuevos paquetes

Copiar los `.deb` a `incoming/bookworm/` y hacer push a `main`.
GitHub Actions ejecutará reprepro automáticamente.
