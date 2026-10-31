# Run the included application

[中文说明](#中文说明) · [Source attribution](../UPSTREAM.md)

The root directory contains the original team application. The nested `djjpg/` directory is an older starter project; use the root's `package.json` and `pages/` implementation.

## Setup

Use a Node.js version compatible with the included Next.js dependency, then run these commands from the repository root:

```bash
npm ci
cp .env.example .env.local
```

Fill in your own values in `.env.local`:

| Variable | Purpose |
| --- | --- |
| `OPENAI_API_KEY` | Server-side image analysis |
| `SPOTIFY_CLIENT_ID` | Your Spotify developer application |
| `SPOTIFY_CLIENT_SECRET` | Server-side Spotify authentication |
| `SPOTIFY_REDIRECT_URI` | Callback address for this copy of the application |

The local callback value in the template is `http://127.0.0.1:3000/api/auth/callback`. The configured application and Spotify developer settings need to use the same callback address. These notes describe the included implementation; access to provider features depends on your own application configuration and current provider permissions.

Then start the application:

```bash
npm run dev
```

Open [http://127.0.0.1:3000](http://127.0.0.1:3000). The landing page can be viewed without a Spotify session; the complete photo-to-playlist flow requires your configured services and Spotify authorization.

Production scripts supplied by the team are `npm run build` and `npm start`. This copy operation did not perform an authenticated integration test, redeploy the app, or establish that the original implementation passes a production build today. The historical demo remains unavailable.

Keep `.env.local` out of Git. The template is blank; do not reuse credentials from shared working documents. The [technical overview](TECHNICAL_OVERVIEW.md#image-handling) explains image handling in the copied source.

## 中文说明

1. 下载或克隆你的仓库，在包含根目录 `package.json` 的文件夹中打开项目。
2. 安装依赖：`npm ci`。
3. 把 `.env.example` 复制为 `.env.local`，填入你自己的 OpenAI 与 Spotify 服务凭据，并核对回调地址。
4. 启动：`npm run dev`，在浏览器打开 `http://127.0.0.1:3000`。

无需进入嵌套的 `djjpg/` 文件夹。首页可以单独查看；真实图片分析、歌曲获取和保存歌单需要有效的服务配置与 Spotify 授权。复制 GitHub 仓库本身不会自动恢复原来的在线 Demo。
