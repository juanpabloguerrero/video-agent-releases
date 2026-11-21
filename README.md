# video-agent-releases

Binarios y scripts de instalacion del **VideoPlatform Agent**.

Este repositorio es **solo de distribucion**: el codigo fuente vive en el repositorio privado `video_analisis_glm51`. El CI (`.github/workflows/release-agent.yml`) publica aca, en cada tag `agent-v*`:

- `video-agent-windows-amd64.exe` / `video-agent-linux-amd64` / `video-agent-linux-arm64`
- `sha256sums.txt`
- `install-agent.ps1` / `uninstall-agent.ps1`

Instalacion (PowerShell como administrador en la PC del cliente):

```powershell
irm https://github.com/juanpabloguerrero/video-agent-releases/releases/latest/download/install-agent.ps1 -OutFile install-agent.ps1
.\install-agent.ps1
```

El instalador verifica el SHA256 del binario contra `sha256sums.txt` antes de instalar. Guia completa: `docs/COMO_INSTALAR_AGENTE.md` en el repositorio privado.
