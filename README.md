# static-site-without-build
静的サイトホスティングサービスを比較するための静的サイト


## 調査方法

- 静的サイトホスティングサービスにこのリポジトリを接続
- 検証日：2022-01-12
- ビルド検証回数：初回接続1回のみ

## Netlify

- デプロイしたサイト： https://static-site-without-build.netlify.app/
- ビルド＆デプロイ： 5秒

### ビルド＆デプロイ

画面表示：Build time: 2s. Total deploy time: 2s
ログからの実際の時間：5s

<details>
<summary>Netlify Deploy log</summary>

```
4:12:45 PM: Build ready to start
4:12:47 PM: build-image version: 73def8bb10593b9b818f44989a75ea508018ccb7 (focal)
4:12:47 PM: build-image tag: v4.5.2
4:12:47 PM: buildbot version: 29a0d1af3616ecbfb22b1a678421693ce64d1dd8
4:12:47 PM: Fetching cached dependencies
4:12:47 PM: Failed to fetch cache, continuing with build
4:12:47 PM: Starting to prepare the repo for build
4:12:48 PM: No cached dependencies found. Cloning fresh repo
4:12:48 PM: git clone https://github.com/kyosuke/static-site-without-build
4:12:48 PM: Preparing Git Reference refs/heads/main
4:12:48 PM: Parsing package.json dependencies
4:12:49 PM: No build steps found, continuing to publishing
4:12:49 PM: Starting to deploy site from 'public'
4:12:49 PM: Creating deploy tree 
4:12:49 PM: Creating deploy upload records
4:12:49 PM: 1 new files to upload
4:12:49 PM: 0 new functions to upload
4:12:49 PM: Starting post processing
4:12:49 PM: Post processing - HTML
4:12:50 PM: Finished processing build request in 2.56345531s
4:12:50 PM: Post processing - header rules
4:12:50 PM: Post processing - redirect rules
4:12:50 PM: Post processing done
4:12:50 PM: Site is live ✨
```

</details>

## Vercel

- デプロイしたサイト： https://static-site-without-build.vercel.app/
- ビルド＆デプロイ： 10秒

### ビルド＆デプロイ

DURATION 10s

<details>
<summary>Vercel Building Log</summary>

```
16:07:20.267 Cloning github.com/kyosuke/static-site-without-build (Branch: main, Commit: 21829eb)
16:07:20.577 Cloning completed: 309.682ms
16:07:20.591 Analyzing source code...
16:07:25.737 Uploading build outputs...
16:07:26.454 Deploying build outputs...
16:07:28.648Done with "."
```

</details>

## Cloudflare Pages

- デプロイしたサイト： https://static-site-without-build.pages.dev/
- ビルド＆デプロイ： 2分27秒

### ビルド＆デプロイ

時間:2m 27s

<details>
<summary>Cloudflare Pages ビルド ログ</summary>

```
15:14:52.003	Initializing build environment. This may take up to a few minutes to complete
15:17:14.752	Success: Finished initializing build environment
15:17:14.752	Cloning repository...
15:17:15.863	Success: Finished cloning repository files
15:17:15.941	No build command specified. Skipping build step.
15:17:15.941	Note: No functions dir at /functions found. Skipping.
15:17:15.941	Validating asset output directory
15:17:16.271	Deploying your site to Cloudflare's global network...
15:17:19.413	Success: Your site was deployed!
```

</details>
