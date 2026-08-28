# 0low Connect — gerar APK pelo celular

## Método mais simples: GitHub Actions

1. Crie um repositório NOVO no GitHub.
2. Envie TODOS os arquivos desta pasta para a raiz do repositório.
3. Faça commit na branch `main`.
4. Abra o repositório > **Actions**.
5. Escolha **Build 0low Connect APK**.
6. Toque em **Run workflow**.
7. Espere o build terminar.
8. Abra a execução concluída e procure **Artifacts**.
9. Baixe `0low-connect-debug-apk`.
10. Extraia o ZIP do artifact e instale `app-debug.apk`.

### Se o GitHub não mostrar Actions
Abra a aba Actions e habilite workflows no repositório. Depois faça um novo commit ou rode manualmente.

## Importante sobre o servidor
O APK é o aplicativo. O `server.js` continua sendo o backend para chat, servidores e sinalização WebRTC. Ele deve continuar publicado no Render.

## Compartilhamento de tela
Esta primeira preparação gera o APK com Capacitor, mas o botão de captura de tela do seu JavaScript continua sujeito ao suporte do WebView. Para captura nativa garantida no Android, ainda é necessário adicionar um plugin/bridge Android usando MediaProjection.
