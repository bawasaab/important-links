
<!DOCTYPE html>
<html lang="en" class="desktop-view not-mobile-device text-size-normal anon">
  <head>
    <meta charset="utf-8">
    <title>How to build an Android APK file without using Android Studio in a Capacitor project? - Capacitor - Ionic Forum</title>
    <meta name="description" content="I recently came across Capacitor and i tried it, I find it better than Cordova. 
But the only thing is I could not find a command to generate .apk or archive. 
In Cordova, I was able to generate .apk without even opening&amp;hellip;">
    <meta name="discourse_theme_id" content="3">
    <meta name="discourse_current_homepage" content="categories">
    <meta name="generator" content="Discourse 2.8.0.beta6 - https://github.com/discourse/discourse version 6273dfad4bc79576808c00b98f9c211e575021f6">
<link rel="icon" type="image/png" href="https://aws1.discourse-cdn.com/ionicframework/optimized/3X/a/4/a4bdd686c6074c2dfe3c9d529350a82781516b3e_2_32x32.png">
<link rel="apple-touch-icon" type="image/png" href="https://aws1.discourse-cdn.com/ionicframework/optimized/3X/6/1/611c901fd53d1af605cd282e83292c2edf752d8d_2_180x180.png">
<meta name="theme-color" content="#ffffff">
<meta name="viewport" content="width=device-width, initial-scale=1.0, minimum-scale=1.0, user-scalable=yes, viewport-fit=cover">
<link rel="canonical" href="https://forum.ionicframework.com/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814" />
<script type="application/ld+json">{"@context":"http://schema.org","@type":"WebSite","url":"https://forum.ionicframework.com","potentialAction":{"@type":"SearchAction","target":"https://forum.ionicframework.com/search?q={search_term_string}","query-input":"required name=search_term_string"}}</script>
<link rel="search" type="application/opensearchdescription+xml" href="https://forum.ionicframework.com/opensearch.xml" title="Ionic Forum Search">

    

    <link href="https://sea2.discourse-cdn.com/ionicframework/stylesheets/color_definitions_light_1_3_906eadab44d479cf1f6dd806bd2b3ff4a7ff8204.css?__ws=forum.ionicframework.com" media="all" rel="stylesheet" class="light-scheme"/>

  <link href="https://sea2.discourse-cdn.com/ionicframework/stylesheets/desktop_11c0ecf3a0eb00fe7927f143c5ec1ce9f81d87ea.css?__ws=forum.ionicframework.com" media="all" rel="stylesheet" data-target="desktop"  />


  <link href="https://sea2.discourse-cdn.com/ionicframework/stylesheets/discourse-akismet_11c0ecf3a0eb00fe7927f143c5ec1ce9f81d87ea.css?__ws=forum.ionicframework.com" media="all" rel="stylesheet" data-target="discourse-akismet"  />
  <link href="https://sea2.discourse-cdn.com/ionicframework/stylesheets/discourse-cakeday_11c0ecf3a0eb00fe7927f143c5ec1ce9f81d87ea.css?__ws=forum.ionicframework.com" media="all" rel="stylesheet" data-target="discourse-cakeday"  />
  <link href="https://sea2.discourse-cdn.com/ionicframework/stylesheets/discourse-canned-replies_11c0ecf3a0eb00fe7927f143c5ec1ce9f81d87ea.css?__ws=forum.ionicframework.com" media="all" rel="stylesheet" data-target="discourse-canned-replies"  />
  <link href="https://sea2.discourse-cdn.com/ionicframework/stylesheets/discourse-checklist_11c0ecf3a0eb00fe7927f143c5ec1ce9f81d87ea.css?__ws=forum.ionicframework.com" media="all" rel="stylesheet" data-target="discourse-checklist"  />
  <link href="https://sea2.discourse-cdn.com/ionicframework/stylesheets/discourse-details_11c0ecf3a0eb00fe7927f143c5ec1ce9f81d87ea.css?__ws=forum.ionicframework.com" media="all" rel="stylesheet" data-target="discourse-details"  />
  <link href="https://sea2.discourse-cdn.com/ionicframework/stylesheets/discourse-local-dates_11c0ecf3a0eb00fe7927f143c5ec1ce9f81d87ea.css?__ws=forum.ionicframework.com" media="all" rel="stylesheet" data-target="discourse-local-dates"  />
  <link href="https://sea2.discourse-cdn.com/ionicframework/stylesheets/discourse-narrative-bot_11c0ecf3a0eb00fe7927f143c5ec1ce9f81d87ea.css?__ws=forum.ionicframework.com" media="all" rel="stylesheet" data-target="discourse-narrative-bot"  />
  <link href="https://sea2.discourse-cdn.com/ionicframework/stylesheets/discourse-presence_11c0ecf3a0eb00fe7927f143c5ec1ce9f81d87ea.css?__ws=forum.ionicframework.com" media="all" rel="stylesheet" data-target="discourse-presence"  />
  <link href="https://sea2.discourse-cdn.com/ionicframework/stylesheets/discourse-solved_11c0ecf3a0eb00fe7927f143c5ec1ce9f81d87ea.css?__ws=forum.ionicframework.com" media="all" rel="stylesheet" data-target="discourse-solved"  />
  <link href="https://sea2.discourse-cdn.com/ionicframework/stylesheets/discourse-spoiler-alert_11c0ecf3a0eb00fe7927f143c5ec1ce9f81d87ea.css?__ws=forum.ionicframework.com" media="all" rel="stylesheet" data-target="discourse-spoiler-alert"  />
  <link href="https://sea2.discourse-cdn.com/ionicframework/stylesheets/discourse-user-notes_11c0ecf3a0eb00fe7927f143c5ec1ce9f81d87ea.css?__ws=forum.ionicframework.com" media="all" rel="stylesheet" data-target="discourse-user-notes"  />
  <link href="https://sea2.discourse-cdn.com/ionicframework/stylesheets/discourse-voting_11c0ecf3a0eb00fe7927f143c5ec1ce9f81d87ea.css?__ws=forum.ionicframework.com" media="all" rel="stylesheet" data-target="discourse-voting"  />
  <link href="https://sea2.discourse-cdn.com/ionicframework/stylesheets/hosted-site_11c0ecf3a0eb00fe7927f143c5ec1ce9f81d87ea.css?__ws=forum.ionicframework.com" media="all" rel="stylesheet" data-target="hosted-site"  />
  <link href="https://sea2.discourse-cdn.com/ionicframework/stylesheets/lazy-yt_11c0ecf3a0eb00fe7927f143c5ec1ce9f81d87ea.css?__ws=forum.ionicframework.com" media="all" rel="stylesheet" data-target="lazy-yt"  />
  <link href="https://sea2.discourse-cdn.com/ionicframework/stylesheets/poll_11c0ecf3a0eb00fe7927f143c5ec1ce9f81d87ea.css?__ws=forum.ionicframework.com" media="all" rel="stylesheet" data-target="poll"  />
  <link href="https://sea2.discourse-cdn.com/ionicframework/stylesheets/discourse-voting_desktop_11c0ecf3a0eb00fe7927f143c5ec1ce9f81d87ea.css?__ws=forum.ionicframework.com" media="all" rel="stylesheet" data-target="discourse-voting_desktop"  />
  <link href="https://sea2.discourse-cdn.com/ionicframework/stylesheets/poll_desktop_11c0ecf3a0eb00fe7927f143c5ec1ce9f81d87ea.css?__ws=forum.ionicframework.com" media="all" rel="stylesheet" data-target="poll_desktop"  />

  <link href="https://sea2.discourse-cdn.com/ionicframework/stylesheets/desktop_theme_1_c037fb3df727468d9cc742f05ee6a7568777f7de.css?__ws=forum.ionicframework.com" media="all" rel="stylesheet" data-target="desktop_theme" data-theme-id="1" data-theme-name="ionic"/>
<link href="https://sea2.discourse-cdn.com/ionicframework/stylesheets/desktop_theme_3_455b3ca3e62cc262e1a908f48beddb01313d51de.css?__ws=forum.ionicframework.com" media="all" rel="stylesheet" data-target="desktop_theme" data-theme-id="3" data-theme-name="default"/>


      <meta name="fragment" content="!">


    

    <link rel="preload" href="https://aws1.discourse-cdn.com/ionicframework/assets/browser-detect-16ca87077aead9f656700e192992122d3a7eee8c1bb76da992127945464d4777.br.js" as="script">
<script src="https://aws1.discourse-cdn.com/ionicframework/assets/browser-detect-16ca87077aead9f656700e192992122d3a7eee8c1bb76da992127945464d4777.br.js"></script>


    <link rel="preload" href="https://aws1.discourse-cdn.com/ionicframework/assets/locales/en-261a662105d5032f4d7381e0465115debfc65444e8e5f9ca0ab9de43cf4b3f7f.br.js" as="script">
<script src="https://aws1.discourse-cdn.com/ionicframework/assets/locales/en-261a662105d5032f4d7381e0465115debfc65444e8e5f9ca0ab9de43cf4b3f7f.br.js"></script>

    <link rel="preload" href="https://aws1.discourse-cdn.com/ionicframework/assets/vendor-ccc170ebd7d3ab2d70c3e0c52d1121e7ced023e6ed05de129e0060c2a71ba2e3.br.js" as="script">
<script src="https://aws1.discourse-cdn.com/ionicframework/assets/vendor-ccc170ebd7d3ab2d70c3e0c52d1121e7ced023e6ed05de129e0060c2a71ba2e3.br.js"></script>

    <link rel="preload" href="https://aws1.discourse-cdn.com/ionicframework/assets/application-f7a301e038d547f34ec023dcdf99c166f3172b951e87e3d61875fb5a956d2fc2.br.js" as="script">
<script src="https://aws1.discourse-cdn.com/ionicframework/assets/application-f7a301e038d547f34ec023dcdf99c166f3172b951e87e3d61875fb5a956d2fc2.br.js"></script>

      <link rel="preload" href="https://aws1.discourse-cdn.com/ionicframework/assets/plugins/discourse-akismet-b158ed3716457724147fc14a3b6cf4c6234b3b715dcbb2dc830a349d3da3a5db.br.js" as="script">
<script src="https://aws1.discourse-cdn.com/ionicframework/assets/plugins/discourse-akismet-b158ed3716457724147fc14a3b6cf4c6234b3b715dcbb2dc830a349d3da3a5db.br.js"></script>

      <link rel="preload" href="https://aws1.discourse-cdn.com/ionicframework/assets/plugins/discourse-cakeday-600ed4e8da158bdecffbe690ea83a887981a822344335a239e49500e491d5ded.br.js" as="script">
<script src="https://aws1.discourse-cdn.com/ionicframework/assets/plugins/discourse-cakeday-600ed4e8da158bdecffbe690ea83a887981a822344335a239e49500e491d5ded.br.js"></script>

      <link rel="preload" href="https://aws1.discourse-cdn.com/ionicframework/assets/plugins/discourse-canned-replies-33e4732aee5d0bec3cee72adc45b9a5f41c8eaf95bdddb5b4d3026ec6280af09.br.js" as="script">
<script src="https://aws1.discourse-cdn.com/ionicframework/assets/plugins/discourse-canned-replies-33e4732aee5d0bec3cee72adc45b9a5f41c8eaf95bdddb5b4d3026ec6280af09.br.js"></script>

      <link rel="preload" href="https://aws1.discourse-cdn.com/ionicframework/assets/plugins/discourse-checklist-5fe159e04ddbe1aa83d16af087823f45ca50e8dbf486e53bf29489d934d690fc.br.js" as="script">
<script src="https://aws1.discourse-cdn.com/ionicframework/assets/plugins/discourse-checklist-5fe159e04ddbe1aa83d16af087823f45ca50e8dbf486e53bf29489d934d690fc.br.js"></script>

      <link rel="preload" href="https://aws1.discourse-cdn.com/ionicframework/assets/plugins/discourse-details-a5c71c75398c735e851440262e3c9ba43f9d8a2a7d81d8ecec16c8b2dbf452c3.br.js" as="script">
<script src="https://aws1.discourse-cdn.com/ionicframework/assets/plugins/discourse-details-a5c71c75398c735e851440262e3c9ba43f9d8a2a7d81d8ecec16c8b2dbf452c3.br.js"></script>

      <link rel="preload" href="https://aws1.discourse-cdn.com/ionicframework/assets/plugins/discourse-local-dates-9675a588e37a20fc0d322b2610c180527473e601af661bfb0ee00ec608ad64a7.br.js" as="script">
<script src="https://aws1.discourse-cdn.com/ionicframework/assets/plugins/discourse-local-dates-9675a588e37a20fc0d322b2610c180527473e601af661bfb0ee00ec608ad64a7.br.js"></script>

      <link rel="preload" href="https://aws1.discourse-cdn.com/ionicframework/assets/plugins/discourse-narrative-bot-30875b55b6ce1fa11b9bd05515c0c931e4636c32f7ec29078c789af26f3fdcd6.br.js" as="script">
<script src="https://aws1.discourse-cdn.com/ionicframework/assets/plugins/discourse-narrative-bot-30875b55b6ce1fa11b9bd05515c0c931e4636c32f7ec29078c789af26f3fdcd6.br.js"></script>

      <link rel="preload" href="https://aws1.discourse-cdn.com/ionicframework/assets/plugins/discourse-presence-9d6196005999f42e3a0768b2160d00e594999f44850f5284e33ad17b288d9a21.br.js" as="script">
<script src="https://aws1.discourse-cdn.com/ionicframework/assets/plugins/discourse-presence-9d6196005999f42e3a0768b2160d00e594999f44850f5284e33ad17b288d9a21.br.js"></script>

      <link rel="preload" href="https://aws1.discourse-cdn.com/ionicframework/assets/plugins/discourse-solved-124a87de0637e6b154d8a50c2ef81bed3e85d94524e274ff8c0e33aa8740fb30.br.js" as="script">
<script src="https://aws1.discourse-cdn.com/ionicframework/assets/plugins/discourse-solved-124a87de0637e6b154d8a50c2ef81bed3e85d94524e274ff8c0e33aa8740fb30.br.js"></script>

      <link rel="preload" href="https://aws1.discourse-cdn.com/ionicframework/assets/plugins/discourse-spoiler-alert-acf6e7cfe0c2032e73507e60b6015e04535b24fa5dbc1835274b53a43e4ae64e.br.js" as="script">
<script src="https://aws1.discourse-cdn.com/ionicframework/assets/plugins/discourse-spoiler-alert-acf6e7cfe0c2032e73507e60b6015e04535b24fa5dbc1835274b53a43e4ae64e.br.js"></script>

      <link rel="preload" href="https://aws1.discourse-cdn.com/ionicframework/assets/plugins/discourse-user-notes-b61df65536434e030d7448056ad63f61b87e26a846f072c00e47ab08080b0e58.br.js" as="script">
<script src="https://aws1.discourse-cdn.com/ionicframework/assets/plugins/discourse-user-notes-b61df65536434e030d7448056ad63f61b87e26a846f072c00e47ab08080b0e58.br.js"></script>

      <link rel="preload" href="https://aws1.discourse-cdn.com/ionicframework/assets/plugins/discourse-voting-8f07af504e2ac5345d9e0b2868f0c206b2404958786c3d947dc94c44c75fe040.br.js" as="script">
<script src="https://aws1.discourse-cdn.com/ionicframework/assets/plugins/discourse-voting-8f07af504e2ac5345d9e0b2868f0c206b2404958786c3d947dc94c44c75fe040.br.js"></script>

      <link rel="preload" href="https://aws1.discourse-cdn.com/ionicframework/assets/plugins/hosted-site-4b7b998b5126b242b6d0cf39a05b12850b916e4ffc9d58baa3c14c2ac48c8e6f.br.js" as="script">
<script src="https://aws1.discourse-cdn.com/ionicframework/assets/plugins/hosted-site-4b7b998b5126b242b6d0cf39a05b12850b916e4ffc9d58baa3c14c2ac48c8e6f.br.js"></script>

      <link rel="preload" href="https://aws1.discourse-cdn.com/ionicframework/assets/plugins/lazy-yt-4e94ac3522a311236b5b7b0cf0ad4f98ee8632f45a4c686ac5b6676fcabe6f78.br.js" as="script">
<script src="https://aws1.discourse-cdn.com/ionicframework/assets/plugins/lazy-yt-4e94ac3522a311236b5b7b0cf0ad4f98ee8632f45a4c686ac5b6676fcabe6f78.br.js"></script>

      <link rel="preload" href="https://aws1.discourse-cdn.com/ionicframework/assets/plugins/poll-07984e2b341bb511572ac36920ea9bf7532c0ea9e5a38df82d5398715dfe3be3.br.js" as="script">
<script src="https://aws1.discourse-cdn.com/ionicframework/assets/plugins/poll-07984e2b341bb511572ac36920ea9bf7532c0ea9e5a38df82d5398715dfe3be3.br.js"></script>


      
      
      

    <meta id="data-google-tag-manager"
  data-data-layer="{}"
  data-nonce="3007395e7c60328bab410c48916bac0b"
  data-container-id="GTM-TKMGCBC" />

<link rel="preload" href="https://aws1.discourse-cdn.com/ionicframework/assets/google-tag-manager-207e4e7db708ead224f0e2ee6d92492abfe9a29e717480b6f6f2614fa7873019.br.js" as="script">
<script src="https://aws1.discourse-cdn.com/ionicframework/assets/google-tag-manager-207e4e7db708ead224f0e2ee6d92492abfe9a29e717480b6f6f2614fa7873019.br.js"></script>


    
    <link rel="manifest" href="/manifest.webmanifest" crossorigin="use-credentials">



        <link rel="alternate" type="application/rss+xml" title="RSS feed of &#39;How to build an Android APK file without using Android Studio in a Capacitor project?&#39;" href="https://forum.ionicframework.com/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814.rss" />
    <meta property="og:site_name" content="Ionic Forum" />
<meta property="og:type" content="website" />
<meta name="twitter:card" content="summary_large_image" />
<meta name="twitter:image" content="https://aws1.discourse-cdn.com/ionicframework/original/3X/b/e/be9f21e0d32bf8b9c5f5962918f39bf73128fd5a.png" />
<meta property="og:image" content="https://aws1.discourse-cdn.com/ionicframework/original/3X/b/e/be9f21e0d32bf8b9c5f5962918f39bf73128fd5a.png" />
<meta property="og:url" content="https://forum.ionicframework.com/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814" />
<meta name="twitter:url" content="https://forum.ionicframework.com/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814" />
<meta property="og:title" content="How to build an Android APK file without using Android Studio in a Capacitor project?" />
<meta name="twitter:title" content="How to build an Android APK file without using Android Studio in a Capacitor project?" />
<meta property="og:description" content="I recently came across Capacitor and i tried it, I find it better than Cordova.  But the only thing is I could not find a command to generate .apk or archive.  In Cordova, I was able to generate .apk without even opening Android Studio.  I am looking for capacitor equivalent commands for ionic cordova build android and ionic cordova build ios" />
<meta name="twitter:description" content="I recently came across Capacitor and i tried it, I find it better than Cordova.  But the only thing is I could not find a command to generate .apk or archive.  In Cordova, I was able to generate .apk without even opening Android Studio.  I am looking for capacitor equivalent commands for ionic cordova build android and ionic cordova build ios" />
<meta name="twitter:label1" value="Reading time" />
<meta name="twitter:data1" value="3 mins 🕑" />
<meta name="twitter:label2" value="Likes" />
<meta name="twitter:data2" value="50 ❤" />
<meta property="article:published_time" content="2019-11-18T06:49:00+00:00" />
<meta property="og:ignore_canonical" content="true" />

        <link rel="next" href="/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814?page=2">


    <script type="application/ld+json">{"@context":"http://schema.org","@type":"QAPage","name":"How to build an Android APK file without using Android Studio in a Capacitor project?","mainEntity":{"@type":"Question","name":"How to build an Android APK file without using Android Studio in a Capacitor project?","text":"I recently came across Capacitor and i tried it, I find it better than Cordova.\n\nBut the only thing is I could not find a command to generate .apk or archive.\n\nIn Cordova, I was able to generate .apk without even opening Android Studio.\n\nI am looking for capacitor equivalent commands for ionic cordo&hellip;","upvoteCount":0,"answerCount":0,"dateCreated":"2019-11-18T06:49:00.750Z","author":{"@type":"Person","name":"Swapnil P133"}}}</script>

    <meta id="data-discourse-setup" data-cdn="https://sea2.discourse-cdn.com/ionicframework" data-base-url="https://forum.ionicframework.com" data-base-uri="" data-environment="production" data-letter-avatar-version="5_8fec8e114563efeaf5265573e510f08e" data-markdown-it-url="https://aws1.discourse-cdn.com/ionicframework/assets/markdown-it-bundle-31e9a9c535ca1801c26da78b0ff465821751a98f921c5cdc5457d7e5a69e9748.br.js" data-service-worker-url="service-worker.js" data-default-locale="en" data-asset-version="c733445c6e377120c4d4f932fbdac9ad" data-disable-custom-css="false" data-highlight-js-path="/highlight-js/forum.ionicframework.com/cdefff4af52a8d2d43094b5d57ebca1fc7613a63.js" data-svg-sprite-path="/svg-sprite/forum.ionicframework.com/svg-3-2bdd8cea3484a2ff1f88233fac294190200e8d7d.js" data-enable-js-error-reporting="true" data-color-scheme-is-dark="false" data-user-color-scheme-id="1" data-user-dark-scheme-id="-1" data-s3-cdn="https://aws1.discourse-cdn.com/ionicframework" data-s3-base-url="//discourse-cloud-file-uploads.s3.dualstack.us-west-2.amazonaws.com/ionicframework">

    <meta name="discourse/config/environment" content="%7B%22modulePrefix%22%3A%22discourse%22%2C%22environment%22%3A%22production%22%2C%22rootURL%22%3A%22%22%2C%22locationType%22%3A%22auto%22%2C%22historySupportMiddleware%22%3Afalse%2C%22EmberENV%22%3A%7B%22FEATURES%22%3A%7B%7D%2C%22EXTEND_PROTOTYPES%22%3A%7B%22Date%22%3Afalse%7D%2C%22_APPLICATION_TEMPLATE_WRAPPER%22%3Afalse%2C%22_DEFAULT_ASYNC_OBSERVERS%22%3Atrue%2C%22_JQUERY_INTEGRATION%22%3Atrue%7D%2C%22APP%22%3A%7B%22name%22%3A%22discourse%22%2C%22version%22%3A%222.8.0.beta6%206273dfad4bc79576808c00b98f9c211e575021f6%22%2C%22exportApplicationGlobal%22%3Atrue%7D%7D" />
  </head>

  <body class="">
      

    <!-- Google Tag Manager (noscript) -->
<noscript><iframe src="https://www.googletagmanager.com/ns.html?id=GTM-TKMGCBC"
height="0" width="0" style="display:none;visibility:hidden"></iframe></noscript>
<!-- End Google Tag Manager (noscript) -->

    <noscript data-path="/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814">
      
  <header class="d-header">
    <div class="wrap">
      <div class="contents clearfix">
        <div class="title">
          <a href="/">
              <picture>
                <img src="https://aws1.discourse-cdn.com/ionicframework/original/3X/3/b/3bcceade60c32df77565a17af301b363f2a418ae.png" alt="Ionic Forum" id="site-logo" />
              </picture>
          </a>
        </div>
        <div class="panel clearfix">
            <span class='header-buttons'>
              <a href="/login" class='btn btn-primary btn-small login-button btn-icon-text'><svg class="fa d-icon svg-icon svg-node" aria-hidden="true"><svg id="user" viewBox="0 0 448 512">
    <path d="M224 256c70.7 0 128-57.3 128-128S294.7 0 224 0 96 57.3 96 128s57.3 128 128 128zm89.6 32h-16.7c-22.2 10.2-46.9 16-72.9 16s-50.6-5.8-72.9-16h-16.7C60.2 288 0 348.2 0 422.4V464c0 26.5 21.5 48 48 48h352c26.5 0 48-21.5 48-48v-41.6c0-74.2-60.2-134.4-134.4-134.4z"/>
  </svg></svg>
Log In</a>
            </span>
        </div>
      </div>
    </div>
  </header>

      <div id="main-outlet" class="wrap" role="main">
        <!-- preload-content: -->
          <div id="topic-title">
    <h1>
      <a href="/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814">How to build an Android APK file without using Android Studio in a Capacitor project?</a>
    </h1>

      <div class="topic-category" itemscope itemtype="http://schema.org/BreadcrumbList">
          <span itemprop="itemListElement" itemscope itemtype="http://schema.org/ListItem">
            <a href="https://forum.ionicframework.com/c/capacitor/26" class="badge-wrapper bullet" itemprop="item">
              <span class='badge-category-bg' style='background-color: #4BB5FF'></span>
              <span class='badge-category clear-badge'>
                <span class='category-name' itemprop='name'>Capacitor</span>
              </span>
            </a>
            <meta itemprop="position" content="1" />
          </span>
      </div>

  </div>

  


      <div itemscope itemtype='http://schema.org/DiscussionForumPosting' class='topic-body crawler-post'>
        <div class='crawler-post-meta'>
          <div itemprop='publisher' itemscope itemtype="http://schema.org/Organization">
            <meta itemprop='name' content='Drifty Co.'>
              <div itemprop='logo' itemscope itemtype="http://schema.org/ImageObject">
                <meta itemprop='url' content='https://aws1.discourse-cdn.com/ionicframework/original/3X/3/b/3bcceade60c32df77565a17af301b363f2a418ae.png'>
              </div>
          </div>
          <span class="creator" itemprop="author" itemscope itemtype="http://schema.org/Person">
            <a itemprop="url" href='https://forum.ionicframework.com/u/SwapnilP133'><span itemprop='name'>SwapnilP133</span></a>
            
          </span>

          <link itemprop="mainEntityOfPage" href="https://forum.ionicframework.com/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814">


          <span class="crawler-post-infos">
              <time itemprop='datePublished' datetime='2019-11-18T06:49:00Z' class='post-time'>
                November 18, 2019,  6:49am
              </time>
              <meta itemprop='dateModified' content='2020-11-10T17:53:24Z'>
          <span itemprop='position'>#1</span>
          </span>
        </div>
        <div class='post' itemprop='articleBody'>
          <p>I recently came across Capacitor and i tried it, I find it better than Cordova.<br>
But the only thing is I could not find a command to generate .apk or archive.<br>
In Cordova, I was able to generate .apk without even opening Android Studio.<br>
I am looking for capacitor equivalent commands for <code>ionic cordova build android</code> and <code>ionic cordova build ios</code></p>
        </div>

        <meta itemprop='headline' content='How to build an Android APK file without using Android Studio in a Capacitor project?'>
          <meta itemprop='keywords' content=''>

        <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
           <meta itemprop="interactionType" content="http://schema.org/LikeAction"/>
           <meta itemprop="userInteractionCount" content="0" />
           <span class='post-likes'></span>
         </div>

         <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
            <meta itemprop="interactionType" content="http://schema.org/CommentAction"/>
            <meta itemprop="userInteractionCount" content="0" />
          </div>

      </div>
      <div itemscope itemtype='http://schema.org/DiscussionForumPosting' class='topic-body crawler-post'>
        <div class='crawler-post-meta'>
          <div itemprop='publisher' itemscope itemtype="http://schema.org/Organization">
            <meta itemprop='name' content='Drifty Co.'>
              <div itemprop='logo' itemscope itemtype="http://schema.org/ImageObject">
                <meta itemprop='url' content='https://aws1.discourse-cdn.com/ionicframework/original/3X/3/b/3bcceade60c32df77565a17af301b363f2a418ae.png'>
              </div>
          </div>
          <span class="creator" itemprop="author" itemscope itemtype="http://schema.org/Person">
            <a itemprop="url" href='https://forum.ionicframework.com/u/terranmarine'><span itemprop='name'>terranmarine</span></a>
            
          </span>

          <link itemprop="mainEntityOfPage" href="https://forum.ionicframework.com/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814">


          <span class="crawler-post-infos">
              <time itemprop='datePublished' datetime='2019-11-18T14:39:17Z' class='post-time'>
                November 18, 2019,  2:39pm
              </time>
              <meta itemprop='dateModified' content='2019-11-18T14:39:17Z'>
          <span itemprop='position'>#2</span>
          </span>
        </div>
        <div class='post' itemprop='articleBody'>
          <p>Hello,</p>
<p>Give this a try:<br>
<code>    "ios": "sudo ionic build &amp;&amp; npx cap sync ios &amp;&amp; npx cap open ios",     "android": "sudo ionic build &amp;&amp; npx cap sync android &amp;&amp; npx cap open android",</code></p>
<p>You can add there to your package json and when you want a new build just go <code>npm run [platform]</code>. You can also try running it without <code>sudo</code><br>
Alex.</p>
        </div>

        <meta itemprop='headline' content='How to build an Android APK file without using Android Studio in a Capacitor project?'>

        <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
           <meta itemprop="interactionType" content="http://schema.org/LikeAction"/>
           <meta itemprop="userInteractionCount" content="0" />
           <span class='post-likes'></span>
         </div>

         <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
            <meta itemprop="interactionType" content="http://schema.org/CommentAction"/>
            <meta itemprop="userInteractionCount" content="0" />
          </div>

      </div>
      <div itemscope itemtype='http://schema.org/DiscussionForumPosting' class='topic-body crawler-post'>
        <div class='crawler-post-meta'>
          <div itemprop='publisher' itemscope itemtype="http://schema.org/Organization">
            <meta itemprop='name' content='Drifty Co.'>
              <div itemprop='logo' itemscope itemtype="http://schema.org/ImageObject">
                <meta itemprop='url' content='https://aws1.discourse-cdn.com/ionicframework/original/3X/3/b/3bcceade60c32df77565a17af301b363f2a418ae.png'>
              </div>
          </div>
          <span class="creator" itemprop="author" itemscope itemtype="http://schema.org/Person">
            <a itemprop="url" href='https://forum.ionicframework.com/u/mcroni'><span itemprop='name'>mcroni</span></a>
            
          </span>

          <link itemprop="mainEntityOfPage" href="https://forum.ionicframework.com/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814">


          <span class="crawler-post-infos">
              <time itemprop='datePublished' datetime='2019-11-18T17:35:54Z' class='post-time'>
                November 18, 2019,  5:35pm
              </time>
              <meta itemprop='dateModified' content='2019-11-18T17:35:54Z'>
          <span itemprop='position'>#3</span>
          </span>
        </div>
        <div class='post' itemprop='articleBody'>
          <p>Hey,  type <code>npx cap open android</code>, this will open the android studio automatically. Wait till the gradle downloads successful and click on the play button (that’s if you have an android device connected to the pc) else click on <code>Build -- &gt;Build Bundle /Apk</code> and you are good to go</p>
        </div>

        <meta itemprop='headline' content='How to build an Android APK file without using Android Studio in a Capacitor project?'>

        <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
           <meta itemprop="interactionType" content="http://schema.org/LikeAction"/>
           <meta itemprop="userInteractionCount" content="1" />
           <span class='post-likes'>1 Like</span>
         </div>

         <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
            <meta itemprop="interactionType" content="http://schema.org/CommentAction"/>
            <meta itemprop="userInteractionCount" content="1" />
          </div>

      </div>
      <div itemscope itemtype='http://schema.org/DiscussionForumPosting' class='topic-body crawler-post'>
        <div class='crawler-post-meta'>
          <div itemprop='publisher' itemscope itemtype="http://schema.org/Organization">
            <meta itemprop='name' content='Drifty Co.'>
              <div itemprop='logo' itemscope itemtype="http://schema.org/ImageObject">
                <meta itemprop='url' content='https://aws1.discourse-cdn.com/ionicframework/original/3X/3/b/3bcceade60c32df77565a17af301b363f2a418ae.png'>
              </div>
          </div>
          <span class="creator" itemprop="author" itemscope itemtype="http://schema.org/Person">
            <a itemprop="url" href='https://forum.ionicframework.com/u/roboter'><span itemprop='name'>roboter</span></a>
            
          </span>

          <link itemprop="mainEntityOfPage" href="https://forum.ionicframework.com/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814">


          <span class="crawler-post-infos">
              <time itemprop='datePublished' datetime='2019-11-20T11:13:52Z' class='post-time'>
                November 20, 2019, 11:13am
              </time>
              <meta itemprop='dateModified' content='2019-11-20T11:13:52Z'>
          <span itemprop='position'>#5</span>
          </span>
        </div>
        <div class='post' itemprop='articleBody'>
          <p>Hey, did you read the question?</p>
<blockquote>
<p>without using Android Studio</p>
</blockquote>
<p>Looking for same</p>
        </div>

        <meta itemprop='headline' content='How to build an Android APK file without using Android Studio in a Capacitor project?'>

        <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
           <meta itemprop="interactionType" content="http://schema.org/LikeAction"/>
           <meta itemprop="userInteractionCount" content="8" />
           <span class='post-likes'>8 Likes</span>
         </div>

         <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
            <meta itemprop="interactionType" content="http://schema.org/CommentAction"/>
            <meta itemprop="userInteractionCount" content="0" />
          </div>

      </div>
      <div itemscope itemtype='http://schema.org/DiscussionForumPosting' class='topic-body crawler-post'>
        <div class='crawler-post-meta'>
          <div itemprop='publisher' itemscope itemtype="http://schema.org/Organization">
            <meta itemprop='name' content='Drifty Co.'>
              <div itemprop='logo' itemscope itemtype="http://schema.org/ImageObject">
                <meta itemprop='url' content='https://aws1.discourse-cdn.com/ionicframework/original/3X/3/b/3bcceade60c32df77565a17af301b363f2a418ae.png'>
              </div>
          </div>
          <span class="creator" itemprop="author" itemscope itemtype="http://schema.org/Person">
            <a itemprop="url" href='https://forum.ionicframework.com/u/SwapnilP133'><span itemprop='name'>SwapnilP133</span></a>
            
          </span>

          <link itemprop="mainEntityOfPage" href="https://forum.ionicframework.com/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814">


          <span class="crawler-post-infos">
              <time itemprop='datePublished' datetime='2019-11-20T14:17:48Z' class='post-time'>
                November 20, 2019,  2:17pm
              </time>
              <meta itemprop='dateModified' content='2019-11-20T14:17:48Z'>
          <span itemprop='position'>#6</span>
          </span>
        </div>
        <div class='post' itemprop='articleBody'>
          <p>I have a current project in Cordova and it is integrated with Team City CI / CD.<br>
We generate .apk and Xcode archives by running Cordova build whenever we push something to the master branch.<br>
I like Capacitor but didn’t find the capacitor build commands for my scenario.</p>
        </div>

        <meta itemprop='headline' content='How to build an Android APK file without using Android Studio in a Capacitor project?'>

        <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
           <meta itemprop="interactionType" content="http://schema.org/LikeAction"/>
           <meta itemprop="userInteractionCount" content="0" />
           <span class='post-likes'></span>
         </div>

         <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
            <meta itemprop="interactionType" content="http://schema.org/CommentAction"/>
            <meta itemprop="userInteractionCount" content="0" />
          </div>

      </div>
      <div itemscope itemtype='http://schema.org/DiscussionForumPosting' class='topic-body crawler-post'>
        <div class='crawler-post-meta'>
          <div itemprop='publisher' itemscope itemtype="http://schema.org/Organization">
            <meta itemprop='name' content='Drifty Co.'>
              <div itemprop='logo' itemscope itemtype="http://schema.org/ImageObject">
                <meta itemprop='url' content='https://aws1.discourse-cdn.com/ionicframework/original/3X/3/b/3bcceade60c32df77565a17af301b363f2a418ae.png'>
              </div>
          </div>
          <span class="creator" itemprop="author" itemscope itemtype="http://schema.org/Person">
            <a itemprop="url" href='https://forum.ionicframework.com/u/mikrochipkid'><span itemprop='name'>mikrochipkid</span></a>
            
          </span>

          <link itemprop="mainEntityOfPage" href="https://forum.ionicframework.com/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814">


          <span class="crawler-post-infos">
              <time itemprop='datePublished' datetime='2019-11-20T19:11:14Z' class='post-time'>
                November 20, 2019,  7:11pm
              </time>
              <meta itemprop='dateModified' content='2019-11-20T19:11:14Z'>
          <span itemprop='position'>#7</span>
          </span>
        </div>
        <div class='post' itemprop='articleBody'>
          <p>You can’t. Capacitor just opens the IDEs that you need in order to build Platform projects.</p>
        </div>

        <meta itemprop='headline' content='How to build an Android APK file without using Android Studio in a Capacitor project?'>

        <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
           <meta itemprop="interactionType" content="http://schema.org/LikeAction"/>
           <meta itemprop="userInteractionCount" content="1" />
           <span class='post-likes'>1 Like</span>
         </div>

         <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
            <meta itemprop="interactionType" content="http://schema.org/CommentAction"/>
            <meta itemprop="userInteractionCount" content="1" />
          </div>

      </div>
      <div itemscope itemtype='http://schema.org/DiscussionForumPosting' class='topic-body crawler-post'>
        <div class='crawler-post-meta'>
          <div itemprop='publisher' itemscope itemtype="http://schema.org/Organization">
            <meta itemprop='name' content='Drifty Co.'>
              <div itemprop='logo' itemscope itemtype="http://schema.org/ImageObject">
                <meta itemprop='url' content='https://aws1.discourse-cdn.com/ionicframework/original/3X/3/b/3bcceade60c32df77565a17af301b363f2a418ae.png'>
              </div>
          </div>
          <span class="creator" itemprop="author" itemscope itemtype="http://schema.org/Person">
            <a itemprop="url" href='https://forum.ionicframework.com/u/rapropos'><span itemprop='name'>rapropos</span></a>
            
          </span>

          <link itemprop="mainEntityOfPage" href="https://forum.ionicframework.com/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814">


          <span class="crawler-post-infos">
              <time itemprop='datePublished' datetime='2019-11-20T19:25:36Z' class='post-time'>
                November 20, 2019,  7:25pm
              </time>
              <meta itemprop='dateModified' content='2019-11-20T19:25:36Z'>
          <span itemprop='position'>#8</span>
          </span>
        </div>
        <div class='post' itemprop='articleBody'>
          <p>I would suggest following/participating in <a href="https://github.com/ionic-team/capacitor/issues/324">this issue</a>.</p>
        </div>

        <meta itemprop='headline' content='How to build an Android APK file without using Android Studio in a Capacitor project?'>

        <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
           <meta itemprop="interactionType" content="http://schema.org/LikeAction"/>
           <meta itemprop="userInteractionCount" content="1" />
           <span class='post-likes'>1 Like</span>
         </div>

         <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
            <meta itemprop="interactionType" content="http://schema.org/CommentAction"/>
            <meta itemprop="userInteractionCount" content="0" />
          </div>

      </div>
      <div itemscope itemtype='http://schema.org/DiscussionForumPosting' class='topic-body crawler-post'>
        <div class='crawler-post-meta'>
          <div itemprop='publisher' itemscope itemtype="http://schema.org/Organization">
            <meta itemprop='name' content='Drifty Co.'>
              <div itemprop='logo' itemscope itemtype="http://schema.org/ImageObject">
                <meta itemprop='url' content='https://aws1.discourse-cdn.com/ionicframework/original/3X/3/b/3bcceade60c32df77565a17af301b363f2a418ae.png'>
              </div>
          </div>
          <span class="creator" itemprop="author" itemscope itemtype="http://schema.org/Person">
            <a itemprop="url" href='https://forum.ionicframework.com/u/codebru'><span itemprop='name'>codebru</span></a>
            
          </span>

          <link itemprop="mainEntityOfPage" href="https://forum.ionicframework.com/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814">


          <span class="crawler-post-infos">
              <time itemprop='datePublished' datetime='2020-04-09T16:48:35Z' class='post-time'>
                April 9, 2020,  4:48pm
              </time>
              <meta itemprop='dateModified' content='2020-04-09T16:48:35Z'>
          <span itemprop='position'>#9</span>
          </span>
        </div>
        <div class='post' itemprop='articleBody'>
          <p>I was having this issue and the way I worked out to do this:</p>
<p>You need to add android first:</p>
<pre><code class="lang-auto">ionic capacitor add android 
</code></pre>
<pre><code class="lang-auto">ionic capacitor copy android &amp;&amp; cd android &amp;&amp; ./gradlew assembleDebug &amp;&amp; cd ..
</code></pre>
<p>Then your apk will be at:</p>
<pre><code class="lang-auto">android/app/build/outputs/apk/debug/app-debug.apk
</code></pre>
<p>If you want to run on device directly from command line:</p>
<pre><code class="lang-auto">ionic capacitor copy android &amp;&amp; cd android &amp;&amp; ./gradlew assembleDebug &amp;&amp; ./gradlew installDebug &amp;&amp; cd ..
</code></pre>
<p>Note: It doesn’t work without entering the android directory</p>
<p>I hope that helps!</p>
        </div>

        <meta itemprop='headline' content='How to build an Android APK file without using Android Studio in a Capacitor project?'>

        <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
           <meta itemprop="interactionType" content="http://schema.org/LikeAction"/>
           <meta itemprop="userInteractionCount" content="20" />
           <span class='post-likes'>20 Likes</span>
         </div>

         <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
            <meta itemprop="interactionType" content="http://schema.org/CommentAction"/>
            <meta itemprop="userInteractionCount" content="7" />
          </div>

      </div>
      <div itemscope itemtype='http://schema.org/DiscussionForumPosting' class='topic-body crawler-post'>
        <div class='crawler-post-meta'>
          <div itemprop='publisher' itemscope itemtype="http://schema.org/Organization">
            <meta itemprop='name' content='Drifty Co.'>
              <div itemprop='logo' itemscope itemtype="http://schema.org/ImageObject">
                <meta itemprop='url' content='https://aws1.discourse-cdn.com/ionicframework/original/3X/3/b/3bcceade60c32df77565a17af301b363f2a418ae.png'>
              </div>
          </div>
          <span class="creator" itemprop="author" itemscope itemtype="http://schema.org/Person">
            <a itemprop="url" href='https://forum.ionicframework.com/u/rahulsharma841990'><span itemprop='name'>rahulsharma841990</span></a>
            
          </span>

          <link itemprop="mainEntityOfPage" href="https://forum.ionicframework.com/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814">


          <span class="crawler-post-infos">
              <time itemprop='datePublished' datetime='2020-05-02T08:26:51Z' class='post-time'>
                May 2, 2020,  8:26am
              </time>
              <meta itemprop='dateModified' content='2020-05-02T08:26:51Z'>
          <span itemprop='position'>#10</span>
          </span>
        </div>
        <div class='post' itemprop='articleBody'>
          <p>Awesome dude!</p>
<p>It work’s. What about the release and production apk?</p>
        </div>

        <meta itemprop='headline' content='How to build an Android APK file without using Android Studio in a Capacitor project?'>

        <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
           <meta itemprop="interactionType" content="http://schema.org/LikeAction"/>
           <meta itemprop="userInteractionCount" content="0" />
           <span class='post-likes'></span>
         </div>

         <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
            <meta itemprop="interactionType" content="http://schema.org/CommentAction"/>
            <meta itemprop="userInteractionCount" content="1" />
          </div>

      </div>
      <div itemscope itemtype='http://schema.org/DiscussionForumPosting' class='topic-body crawler-post'>
        <div class='crawler-post-meta'>
          <div itemprop='publisher' itemscope itemtype="http://schema.org/Organization">
            <meta itemprop='name' content='Drifty Co.'>
              <div itemprop='logo' itemscope itemtype="http://schema.org/ImageObject">
                <meta itemprop='url' content='https://aws1.discourse-cdn.com/ionicframework/original/3X/3/b/3bcceade60c32df77565a17af301b363f2a418ae.png'>
              </div>
          </div>
          <span class="creator" itemprop="author" itemscope itemtype="http://schema.org/Person">
            <a itemprop="url" href='https://forum.ionicframework.com/u/codebru'><span itemprop='name'>codebru</span></a>
            
          </span>

          <link itemprop="mainEntityOfPage" href="https://forum.ionicframework.com/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814">


          <span class="crawler-post-infos">
              <time itemprop='datePublished' datetime='2020-05-04T09:13:18Z' class='post-time'>
                May 4, 2020,  9:13am
              </time>
              <meta itemprop='dateModified' content='2020-05-04T09:13:18Z'>
          <span itemprop='position'>#11</span>
          </span>
        </div>
        <div class='post' itemprop='articleBody'>
          <p>I have not done this yet, please share your solution if you do it.</p>
        </div>

        <meta itemprop='headline' content='How to build an Android APK file without using Android Studio in a Capacitor project?'>

        <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
           <meta itemprop="interactionType" content="http://schema.org/LikeAction"/>
           <meta itemprop="userInteractionCount" content="0" />
           <span class='post-likes'></span>
         </div>

         <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
            <meta itemprop="interactionType" content="http://schema.org/CommentAction"/>
            <meta itemprop="userInteractionCount" content="1" />
          </div>

      </div>
      <div itemscope itemtype='http://schema.org/DiscussionForumPosting' class='topic-body crawler-post'>
        <div class='crawler-post-meta'>
          <div itemprop='publisher' itemscope itemtype="http://schema.org/Organization">
            <meta itemprop='name' content='Drifty Co.'>
              <div itemprop='logo' itemscope itemtype="http://schema.org/ImageObject">
                <meta itemprop='url' content='https://aws1.discourse-cdn.com/ionicframework/original/3X/3/b/3bcceade60c32df77565a17af301b363f2a418ae.png'>
              </div>
          </div>
          <span class="creator" itemprop="author" itemscope itemtype="http://schema.org/Person">
            <a itemprop="url" href='https://forum.ionicframework.com/u/kazlauskis'><span itemprop='name'>kazlauskis</span></a>
            
          </span>

          <link itemprop="mainEntityOfPage" href="https://forum.ionicframework.com/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814">


          <span class="crawler-post-infos">
              <time itemprop='datePublished' datetime='2020-05-05T14:38:16Z' class='post-time'>
                May 5, 2020,  2:38pm
              </time>
              <meta itemprop='dateModified' content='2020-05-05T14:38:16Z'>
          <span itemprop='position'>#12</span>
          </span>
        </div>
        <div class='post' itemprop='articleBody'>
          <p>Here is how to production build for Android:</p>
<pre><code class="lang-auto">cd android &amp;&amp; 
./gradlew assembleRelease &amp;&amp; 
cd app/build/outputs/apk/release &amp;&amp;
jarsigner -keystore YOUR_KEYSTORE_PATH -storepass YOUR_KEYSTORE_PASS app-release-unsigned.apk YOUR_KEYSTORE_ALIAS &amp;&amp;
zipalign 4 app-release-unsigned.apk app-release.apk
</code></pre>
<p>This will generate <code>app-release.apk</code> which should be good to go the play store (see <code>android/app/build/outputs/apk/release</code> folder).</p>
<p>Here is the jarsigner command <a href="https://docs.oracle.com/en/java/javase/14/docs/specs/man/jarsigner.html" rel="nofollow noopener">manual</a>.</p>
        </div>

        <meta itemprop='headline' content='How to build an Android APK file without using Android Studio in a Capacitor project?'>

        <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
           <meta itemprop="interactionType" content="http://schema.org/LikeAction"/>
           <meta itemprop="userInteractionCount" content="9" />
           <span class='post-likes'>9 Likes</span>
         </div>

         <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
            <meta itemprop="interactionType" content="http://schema.org/CommentAction"/>
            <meta itemprop="userInteractionCount" content="2" />
          </div>

      </div>
      <div itemscope itemtype='http://schema.org/DiscussionForumPosting' class='topic-body crawler-post'>
        <div class='crawler-post-meta'>
          <div itemprop='publisher' itemscope itemtype="http://schema.org/Organization">
            <meta itemprop='name' content='Drifty Co.'>
              <div itemprop='logo' itemscope itemtype="http://schema.org/ImageObject">
                <meta itemprop='url' content='https://aws1.discourse-cdn.com/ionicframework/original/3X/3/b/3bcceade60c32df77565a17af301b363f2a418ae.png'>
              </div>
          </div>
          <span class="creator" itemprop="author" itemscope itemtype="http://schema.org/Person">
            <a itemprop="url" href='https://forum.ionicframework.com/u/anshcena'><span itemprop='name'>anshcena</span></a>
            
          </span>

          <link itemprop="mainEntityOfPage" href="https://forum.ionicframework.com/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814">


          <span class="crawler-post-infos">
              <time itemprop='datePublished' datetime='2020-05-06T15:47:15Z' class='post-time'>
                May 6, 2020,  3:47pm
              </time>
              <meta itemprop='dateModified' content='2020-05-06T15:47:15Z'>
          <span itemprop='position'>#13</span>
          </span>
        </div>
        <div class='post' itemprop='articleBody'>
          <p>Thanks, worked fine! Saved my day <img src="https://emoji.discourse-cdn.com/twitter/slight_smile.png?v=9" title=":slight_smile:" class="emoji" alt=":slight_smile:"></p>
        </div>

        <meta itemprop='headline' content='How to build an Android APK file without using Android Studio in a Capacitor project?'>

        <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
           <meta itemprop="interactionType" content="http://schema.org/LikeAction"/>
           <meta itemprop="userInteractionCount" content="1" />
           <span class='post-likes'>1 Like</span>
         </div>

         <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
            <meta itemprop="interactionType" content="http://schema.org/CommentAction"/>
            <meta itemprop="userInteractionCount" content="0" />
          </div>

      </div>
      <div itemscope itemtype='http://schema.org/DiscussionForumPosting' class='topic-body crawler-post'>
        <div class='crawler-post-meta'>
          <div itemprop='publisher' itemscope itemtype="http://schema.org/Organization">
            <meta itemprop='name' content='Drifty Co.'>
              <div itemprop='logo' itemscope itemtype="http://schema.org/ImageObject">
                <meta itemprop='url' content='https://aws1.discourse-cdn.com/ionicframework/original/3X/3/b/3bcceade60c32df77565a17af301b363f2a418ae.png'>
              </div>
          </div>
          <span class="creator" itemprop="author" itemscope itemtype="http://schema.org/Person">
            <a itemprop="url" href='https://forum.ionicframework.com/u/codebru'><span itemprop='name'>codebru</span></a>
            
          </span>

          <link itemprop="mainEntityOfPage" href="https://forum.ionicframework.com/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814">


          <span class="crawler-post-infos">
              <time itemprop='datePublished' datetime='2020-05-11T08:12:33Z' class='post-time'>
                May 11, 2020,  8:12am
              </time>
              <meta itemprop='dateModified' content='2020-05-11T08:12:33Z'>
          <span itemprop='position'>#14</span>
          </span>
        </div>
        <div class='post' itemprop='articleBody'>
          <p>Thanks, this worked for me and saved me a bunch of time!</p>
        </div>

        <meta itemprop='headline' content='How to build an Android APK file without using Android Studio in a Capacitor project?'>

        <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
           <meta itemprop="interactionType" content="http://schema.org/LikeAction"/>
           <meta itemprop="userInteractionCount" content="2" />
           <span class='post-likes'>2 Likes</span>
         </div>

         <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
            <meta itemprop="interactionType" content="http://schema.org/CommentAction"/>
            <meta itemprop="userInteractionCount" content="0" />
          </div>

      </div>
      <div itemscope itemtype='http://schema.org/DiscussionForumPosting' class='topic-body crawler-post'>
        <div class='crawler-post-meta'>
          <div itemprop='publisher' itemscope itemtype="http://schema.org/Organization">
            <meta itemprop='name' content='Drifty Co.'>
              <div itemprop='logo' itemscope itemtype="http://schema.org/ImageObject">
                <meta itemprop='url' content='https://aws1.discourse-cdn.com/ionicframework/original/3X/3/b/3bcceade60c32df77565a17af301b363f2a418ae.png'>
              </div>
          </div>
          <span class="creator" itemprop="author" itemscope itemtype="http://schema.org/Person">
            <a itemprop="url" href='https://forum.ionicframework.com/u/cordial666'><span itemprop='name'>cordial666</span></a>
            
          </span>

          <link itemprop="mainEntityOfPage" href="https://forum.ionicframework.com/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814">


          <span class="crawler-post-infos">
              <time itemprop='datePublished' datetime='2020-06-30T22:21:18Z' class='post-time'>
                June 30, 2020, 10:21pm
              </time>
              <meta itemprop='dateModified' content='2020-06-30T22:21:18Z'>
          <span itemprop='position'>#15</span>
          </span>
        </div>
        <div class='post' itemprop='articleBody'>
          <aside class="quote no-group" data-username="kazlauskis" data-post="12" data-topic="177814">
<div class="title">
<div class="quote-controls"></div>
<img alt="" width="20" height="20" src="https://sea2.discourse-cdn.com/ionicframework/user_avatar/forum.ionicframework.com/kazlauskis/40/132156_2.png" class="avatar"> kazlauskis:</div>
<blockquote>
<p><code>YOUR_KEYSTORE_PASS</code></p>
</blockquote>
</aside>
<p>What should YOUR_KEYSTORE_ALIAS be?</p>
        </div>

        <meta itemprop='headline' content='How to build an Android APK file without using Android Studio in a Capacitor project?'>

        <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
           <meta itemprop="interactionType" content="http://schema.org/LikeAction"/>
           <meta itemprop="userInteractionCount" content="0" />
           <span class='post-likes'></span>
         </div>

         <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
            <meta itemprop="interactionType" content="http://schema.org/CommentAction"/>
            <meta itemprop="userInteractionCount" content="1" />
          </div>

      </div>
      <div itemscope itemtype='http://schema.org/DiscussionForumPosting' class='topic-body crawler-post'>
        <div class='crawler-post-meta'>
          <div itemprop='publisher' itemscope itemtype="http://schema.org/Organization">
            <meta itemprop='name' content='Drifty Co.'>
              <div itemprop='logo' itemscope itemtype="http://schema.org/ImageObject">
                <meta itemprop='url' content='https://aws1.discourse-cdn.com/ionicframework/original/3X/3/b/3bcceade60c32df77565a17af301b363f2a418ae.png'>
              </div>
          </div>
          <span class="creator" itemprop="author" itemscope itemtype="http://schema.org/Person">
            <a itemprop="url" href='https://forum.ionicframework.com/u/kazlauskis'><span itemprop='name'>kazlauskis</span></a>
            
          </span>

          <link itemprop="mainEntityOfPage" href="https://forum.ionicframework.com/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814">


          <span class="crawler-post-infos">
              <time itemprop='datePublished' datetime='2020-07-01T08:17:31Z' class='post-time'>
                July 1, 2020,  8:17am
              </time>
              <meta itemprop='dateModified' content='2020-07-01T08:17:31Z'>
          <span itemprop='position'>#16</span>
          </span>
        </div>
        <div class='post' itemprop='articleBody'>
          <p>You can find your keystore alias by running <code>keytool -v -list -keystore YOUR_KEYSTORE_PATH</code></p>
        </div>

        <meta itemprop='headline' content='How to build an Android APK file without using Android Studio in a Capacitor project?'>

        <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
           <meta itemprop="interactionType" content="http://schema.org/LikeAction"/>
           <meta itemprop="userInteractionCount" content="0" />
           <span class='post-likes'></span>
         </div>

         <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
            <meta itemprop="interactionType" content="http://schema.org/CommentAction"/>
            <meta itemprop="userInteractionCount" content="0" />
          </div>

      </div>
      <div itemscope itemtype='http://schema.org/DiscussionForumPosting' class='topic-body crawler-post'>
        <div class='crawler-post-meta'>
          <div itemprop='publisher' itemscope itemtype="http://schema.org/Organization">
            <meta itemprop='name' content='Drifty Co.'>
              <div itemprop='logo' itemscope itemtype="http://schema.org/ImageObject">
                <meta itemprop='url' content='https://aws1.discourse-cdn.com/ionicframework/original/3X/3/b/3bcceade60c32df77565a17af301b363f2a418ae.png'>
              </div>
          </div>
          <span class="creator" itemprop="author" itemscope itemtype="http://schema.org/Person">
            <a itemprop="url" href='https://forum.ionicframework.com/u/Karthik-V-V'><span itemprop='name'>Karthik-V-V</span></a>
            
          </span>

          <link itemprop="mainEntityOfPage" href="https://forum.ionicframework.com/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814">


          <span class="crawler-post-infos">
              <time itemprop='datePublished' datetime='2020-08-19T06:33:13Z' class='post-time'>
                August 19, 2020,  6:33am
              </time>
              <meta itemprop='dateModified' content='2020-08-19T06:33:13Z'>
          <span itemprop='position'>#17</span>
          </span>
        </div>
        <div class='post' itemprop='articleBody'>
          <p>After spending a whole night trying to configure Android studio, which wouldn’t let a simple ionic app build properly, and then trying to fix issues for cordova, this post of yours gave me my spirits back! You’re really awesome man!!</p>
        </div>

        <meta itemprop='headline' content='How to build an Android APK file without using Android Studio in a Capacitor project?'>

        <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
           <meta itemprop="interactionType" content="http://schema.org/LikeAction"/>
           <meta itemprop="userInteractionCount" content="1" />
           <span class='post-likes'>1 Like</span>
         </div>

         <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
            <meta itemprop="interactionType" content="http://schema.org/CommentAction"/>
            <meta itemprop="userInteractionCount" content="0" />
          </div>

      </div>
      <div itemscope itemtype='http://schema.org/DiscussionForumPosting' class='topic-body crawler-post'>
        <div class='crawler-post-meta'>
          <div itemprop='publisher' itemscope itemtype="http://schema.org/Organization">
            <meta itemprop='name' content='Drifty Co.'>
              <div itemprop='logo' itemscope itemtype="http://schema.org/ImageObject">
                <meta itemprop='url' content='https://aws1.discourse-cdn.com/ionicframework/original/3X/3/b/3bcceade60c32df77565a17af301b363f2a418ae.png'>
              </div>
          </div>
          <span class="creator" itemprop="author" itemscope itemtype="http://schema.org/Person">
            <a itemprop="url" href='https://forum.ionicframework.com/u/rahjain'><span itemprop='name'>rahjain</span></a>
            
          </span>

          <link itemprop="mainEntityOfPage" href="https://forum.ionicframework.com/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814">


          <span class="crawler-post-infos">
              <time itemprop='datePublished' datetime='2020-09-05T08:01:49Z' class='post-time'>
                September 5, 2020,  8:01am
              </time>
              <meta itemprop='dateModified' content='2020-09-05T08:01:49Z'>
          <span itemprop='position'>#18</span>
          </span>
        </div>
        <div class='post' itemprop='articleBody'>
          <p>Just a trick to know all the targets -</p>
<pre><code class="lang-auto">cd android 
gradlew app:tasks --all
</code></pre>
<p>This will out you all the tasks which can be called by gradlew without opening android studio.<br>
Example for building app bundle</p>
<pre><code class="lang-auto">./gradlew bundleRelease
</code></pre>
<p>Hope it helps <img src="https://emoji.discourse-cdn.com/twitter/slight_smile.png?v=9" title=":slight_smile:" class="emoji" alt=":slight_smile:"></p>
        </div>

        <meta itemprop='headline' content='How to build an Android APK file without using Android Studio in a Capacitor project?'>

        <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
           <meta itemprop="interactionType" content="http://schema.org/LikeAction"/>
           <meta itemprop="userInteractionCount" content="2" />
           <span class='post-likes'>2 Likes</span>
         </div>

         <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
            <meta itemprop="interactionType" content="http://schema.org/CommentAction"/>
            <meta itemprop="userInteractionCount" content="0" />
          </div>

      </div>
      <div itemscope itemtype='http://schema.org/DiscussionForumPosting' class='topic-body crawler-post'>
        <div class='crawler-post-meta'>
          <div itemprop='publisher' itemscope itemtype="http://schema.org/Organization">
            <meta itemprop='name' content='Drifty Co.'>
              <div itemprop='logo' itemscope itemtype="http://schema.org/ImageObject">
                <meta itemprop='url' content='https://aws1.discourse-cdn.com/ionicframework/original/3X/3/b/3bcceade60c32df77565a17af301b363f2a418ae.png'>
              </div>
          </div>
          <span class="creator" itemprop="author" itemscope itemtype="http://schema.org/Person">
            <a itemprop="url" href='https://forum.ionicframework.com/u/hfunescom'><span itemprop='name'>hfunescom</span></a>
            
          </span>

          <link itemprop="mainEntityOfPage" href="https://forum.ionicframework.com/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814">


          <span class="crawler-post-infos">
              <time itemprop='datePublished' datetime='2020-10-23T20:38:38Z' class='post-time'>
                October 23, 2020,  8:38pm
              </time>
              <meta itemprop='dateModified' content='2020-10-23T20:38:38Z'>
          <span itemprop='position'>#19</span>
          </span>
        </div>
        <div class='post' itemprop='articleBody'>
          <aside class="quote no-group" data-username="codebru" data-post="9" data-topic="177814">
<div class="title">
<div class="quote-controls"></div>
<img alt="" width="20" height="20" src="https://avatars.discourse-cdn.com/v4/letter/c/7ea924/40.png" class="avatar"> codebru:</div>
<blockquote>
<p><code>android/app/build/outputs/apk/debug/</code></p>
</blockquote>
</aside>
<p>Could continue with my Gitlab CI config because of you <img src="https://emoji.discourse-cdn.com/twitter/slight_smile.png?v=9" title=":slight_smile:" class="emoji" alt=":slight_smile:"><br>
Thank you so much!</p>
        </div>

        <meta itemprop='headline' content='How to build an Android APK file without using Android Studio in a Capacitor project?'>

        <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
           <meta itemprop="interactionType" content="http://schema.org/LikeAction"/>
           <meta itemprop="userInteractionCount" content="1" />
           <span class='post-likes'>1 Like</span>
         </div>

         <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
            <meta itemprop="interactionType" content="http://schema.org/CommentAction"/>
            <meta itemprop="userInteractionCount" content="0" />
          </div>

      </div>
      <div itemscope itemtype='http://schema.org/DiscussionForumPosting' class='topic-body crawler-post'>
        <div class='crawler-post-meta'>
          <div itemprop='publisher' itemscope itemtype="http://schema.org/Organization">
            <meta itemprop='name' content='Drifty Co.'>
              <div itemprop='logo' itemscope itemtype="http://schema.org/ImageObject">
                <meta itemprop='url' content='https://aws1.discourse-cdn.com/ionicframework/original/3X/3/b/3bcceade60c32df77565a17af301b363f2a418ae.png'>
              </div>
          </div>
          <span class="creator" itemprop="author" itemscope itemtype="http://schema.org/Person">
            <a itemprop="url" href='https://forum.ionicframework.com/u/AiAbdrahim'><span itemprop='name'>AiAbdrahim</span></a>
            
          </span>

          <link itemprop="mainEntityOfPage" href="https://forum.ionicframework.com/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814">


          <span class="crawler-post-infos">
              <time itemprop='datePublished' datetime='2020-10-26T10:50:47Z' class='post-time'>
                October 26, 2020, 10:50am
              </time>
              <meta itemprop='dateModified' content='2020-10-26T10:50:47Z'>
          <span itemprop='position'>#20</span>
          </span>
        </div>
        <div class='post' itemprop='articleBody'>
          <p>Thank u bro <img src="https://emoji.discourse-cdn.com/twitter/heart_eyes.png?v=9" title=":heart_eyes:" class="emoji" alt=":heart_eyes:"> <img src="https://emoji.discourse-cdn.com/twitter/smiling_face_with_three_hearts.png?v=9" title=":smiling_face_with_three_hearts:" class="emoji" alt=":smiling_face_with_three_hearts:"> <img src="https://emoji.discourse-cdn.com/twitter/tada.png?v=9" title=":tada:" class="emoji" alt=":tada:"> <img src="https://emoji.discourse-cdn.com/twitter/tada.png?v=9" title=":tada:" class="emoji" alt=":tada:"> <img src="https://emoji.discourse-cdn.com/twitter/tada.png?v=9" title=":tada:" class="emoji" alt=":tada:"> <img src="https://emoji.discourse-cdn.com/twitter/tada.png?v=9" title=":tada:" class="emoji" alt=":tada:"> <img src="https://emoji.discourse-cdn.com/twitter/confetti_ball.png?v=9" title=":confetti_ball:" class="emoji" alt=":confetti_ball:"> <img src="https://emoji.discourse-cdn.com/twitter/confetti_ball.png?v=9" title=":confetti_ball:" class="emoji" alt=":confetti_ball:"> <img src="https://emoji.discourse-cdn.com/twitter/1st_place_medal.png?v=9" title=":1st_place_medal:" class="emoji" alt=":1st_place_medal:"> <img src="https://emoji.discourse-cdn.com/twitter/1st_place_medal.png?v=9" title=":1st_place_medal:" class="emoji" alt=":1st_place_medal:"> <img src="https://emoji.discourse-cdn.com/twitter/1st_place_medal.png?v=9" title=":1st_place_medal:" class="emoji" alt=":1st_place_medal:"> <img src="https://emoji.discourse-cdn.com/twitter/1st_place_medal.png?v=9" title=":1st_place_medal:" class="emoji" alt=":1st_place_medal:"></p>
        </div>

        <meta itemprop='headline' content='How to build an Android APK file without using Android Studio in a Capacitor project?'>

        <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
           <meta itemprop="interactionType" content="http://schema.org/LikeAction"/>
           <meta itemprop="userInteractionCount" content="1" />
           <span class='post-likes'>1 Like</span>
         </div>

         <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
            <meta itemprop="interactionType" content="http://schema.org/CommentAction"/>
            <meta itemprop="userInteractionCount" content="0" />
          </div>

      </div>
      <div itemscope itemtype='http://schema.org/DiscussionForumPosting' class='topic-body crawler-post'>
        <div class='crawler-post-meta'>
          <div itemprop='publisher' itemscope itemtype="http://schema.org/Organization">
            <meta itemprop='name' content='Drifty Co.'>
              <div itemprop='logo' itemscope itemtype="http://schema.org/ImageObject">
                <meta itemprop='url' content='https://aws1.discourse-cdn.com/ionicframework/original/3X/3/b/3bcceade60c32df77565a17af301b363f2a418ae.png'>
              </div>
          </div>
          <span class="creator" itemprop="author" itemscope itemtype="http://schema.org/Person">
            <a itemprop="url" href='https://forum.ionicframework.com/u/obinnae'><span itemprop='name'>obinnae</span></a>
            
          </span>

          <link itemprop="mainEntityOfPage" href="https://forum.ionicframework.com/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814">


          <span class="crawler-post-infos">
              <time itemprop='datePublished' datetime='2020-12-28T01:57:12Z' class='post-time'>
                December 28, 2020,  1:57am
              </time>
              <meta itemprop='dateModified' content='2020-12-28T01:57:12Z'>
          <span itemprop='position'>#22</span>
          </span>
        </div>
        <div class='post' itemprop='articleBody'>
          <p>In case someone on a Mac Big Sur is still having issues, run this (same as the chosen answer, but with ‘sudo’ added)…</p>
<p><code>sudo ionic capacitor copy android &amp;&amp; cd android &amp;&amp; sudo ./gradlew assembleDebug &amp;&amp; cd ..</code></p>
        </div>

        <meta itemprop='headline' content='How to build an Android APK file without using Android Studio in a Capacitor project?'>

        <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
           <meta itemprop="interactionType" content="http://schema.org/LikeAction"/>
           <meta itemprop="userInteractionCount" content="1" />
           <span class='post-likes'>1 Like</span>
         </div>

         <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
            <meta itemprop="interactionType" content="http://schema.org/CommentAction"/>
            <meta itemprop="userInteractionCount" content="0" />
          </div>

      </div>

    <div role='navigation' itemscope itemtype='http://schema.org/SiteNavigationElement' class="topic-body crawler-post">
        <span itemprop='name'><b><a rel="next" itemprop="url" href="/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814?page=2">next page →</a></b></span>
    </div>





        <!-- :preload-content -->
        <footer class="noscript-footer-nav">
          <nav itemscope itemtype='http://schema.org/SiteNavigationElement'>
            <a href='/'>Home</a>
            <a href="/categories">Categories</a>
            <a href="/guidelines">FAQ/Guidelines</a>
            <a href="/tos">Terms of Service</a>
            <a href="/privacy">Privacy Policy</a>
          </nav>
        </footer>
      </div>

      <footer id='noscript-footer'>
        <p>Powered by <a href="https://www.discourse.org">Discourse</a>, best viewed with JavaScript enabled</p>
      </footer>
    </noscript>

      

      

    <section id='main'>
    </section>

      <form id='hidden-login-form' method="post" action="/login" style="display: none;">
        <input name="username" type="text"     id="signin_username">
        <input name="password" type="password" id="signin_password">
        <input name="redirect" type="hidden">
        <input type="submit" id="signin-button" value="Log In">
      </form>

    <div class="hidden" id="data-preloaded" data-preloaded="{&quot;site&quot;:&quot;{\&quot;default_archetype\&quot;:\&quot;regular\&quot;,\&quot;notification_types\&quot;:{\&quot;mentioned\&quot;:1,\&quot;replied\&quot;:2,\&quot;quoted\&quot;:3,\&quot;edited\&quot;:4,\&quot;liked\&quot;:5,\&quot;private_message\&quot;:6,\&quot;invited_to_private_message\&quot;:7,\&quot;invitee_accepted\&quot;:8,\&quot;posted\&quot;:9,\&quot;moved_post\&quot;:10,\&quot;linked\&quot;:11,\&quot;granted_badge\&quot;:12,\&quot;invited_to_topic\&quot;:13,\&quot;custom\&quot;:14,\&quot;group_mentioned\&quot;:15,\&quot;group_message_summary\&quot;:16,\&quot;watching_first_post\&quot;:17,\&quot;topic_reminder\&quot;:18,\&quot;liked_consolidated\&quot;:19,\&quot;post_approved\&quot;:20,\&quot;code_review_commit_approved\&quot;:21,\&quot;membership_request_accepted\&quot;:22,\&quot;membership_request_consolidated\&quot;:23,\&quot;bookmark_reminder\&quot;:24,\&quot;reaction\&quot;:25,\&quot;votes_released\&quot;:26,\&quot;event_reminder\&quot;:27,\&quot;event_invitation\&quot;:28,\&quot;chat_mention\&quot;:29,\&quot;chat_message\&quot;:30},\&quot;post_types\&quot;:{\&quot;regular\&quot;:1,\&quot;moderator_action\&quot;:2,\&quot;small_action\&quot;:3,\&quot;whisper\&quot;:4},\&quot;trust_levels\&quot;:{\&quot;newuser\&quot;:0,\&quot;basic\&quot;:1,\&quot;member\&quot;:2,\&quot;regular\&quot;:3,\&quot;leader\&quot;:4},\&quot;groups\&quot;:[],\&quot;filters\&quot;:[\&quot;latest\&quot;,\&quot;unread\&quot;,\&quot;new\&quot;,\&quot;unseen\&quot;,\&quot;top\&quot;,\&quot;read\&quot;,\&quot;posted\&quot;,\&quot;bookmarks\&quot;,\&quot;votes\&quot;],\&quot;periods\&quot;:[\&quot;all\&quot;,\&quot;yearly\&quot;,\&quot;quarterly\&quot;,\&quot;monthly\&quot;,\&quot;weekly\&quot;,\&quot;daily\&quot;],\&quot;top_menu_items\&quot;:[\&quot;latest\&quot;,\&quot;unread\&quot;,\&quot;new\&quot;,\&quot;unseen\&quot;,\&quot;top\&quot;,\&quot;read\&quot;,\&quot;posted\&quot;,\&quot;bookmarks\&quot;,\&quot;categories\&quot;,\&quot;votes\&quot;],\&quot;anonymous_top_menu_items\&quot;:[\&quot;latest\&quot;,\&quot;top\&quot;,\&quot;categories\&quot;,\&quot;categories\&quot;,\&quot;top\&quot;,\&quot;votes\&quot;],\&quot;uncategorized_category_id\&quot;:12,\&quot;user_field_max_length\&quot;:2048,\&quot;post_action_types\&quot;:[{\&quot;id\&quot;:1,\&quot;name_key\&quot;:\&quot;bookmark\&quot;,\&quot;name\&quot;:\&quot;Bookmark\&quot;,\&quot;description\&quot;:\&quot;Bookmark this post\&quot;,\&quot;short_description\&quot;:\&quot;Bookmark this post\&quot;,\&quot;is_flag\&quot;:false,\&quot;is_custom_flag\&quot;:false},{\&quot;id\&quot;:2,\&quot;name_key\&quot;:\&quot;like\&quot;,\&quot;name\&quot;:\&quot;Like\&quot;,\&quot;description\&quot;:\&quot;Like this post\&quot;,\&quot;short_description\&quot;:\&quot;Like this post\&quot;,\&quot;is_flag\&quot;:false,\&quot;is_custom_flag\&quot;:false},{\&quot;id\&quot;:3,\&quot;name_key\&quot;:\&quot;off_topic\&quot;,\&quot;name\&quot;:\&quot;Off-Topic\&quot;,\&quot;description\&quot;:\&quot;This post is not relevant to the current discussion as defined by the title and first post, and should probably be moved elsewhere.\&quot;,\&quot;short_description\&quot;:\&quot;Not relevant to the discussion\&quot;,\&quot;is_flag\&quot;:true,\&quot;is_custom_flag\&quot;:false},{\&quot;id\&quot;:4,\&quot;name_key\&quot;:\&quot;inappropriate\&quot;,\&quot;name\&quot;:\&quot;Inappropriate\&quot;,\&quot;description\&quot;:\&quot;This post contains content that a reasonable person would consider offensive, abusive, or a violation of \\u003ca href=\\\&quot;/guidelines\\\&quot;\\u003eour community guidelines\\u003c/a\\u003e.\&quot;,\&quot;short_description\&quot;:\&quot;A violation of \\u003ca href=\\\&quot;/guidelines\\\&quot;\\u003eour community guidelines\\u003c/a\\u003e\&quot;,\&quot;is_flag\&quot;:true,\&quot;is_custom_flag\&quot;:false},{\&quot;id\&quot;:8,\&quot;name_key\&quot;:\&quot;spam\&quot;,\&quot;name\&quot;:\&quot;Spam\&quot;,\&quot;description\&quot;:\&quot;This post is an advertisement, or vandalism. It is not useful or relevant to the current topic.\&quot;,\&quot;short_description\&quot;:\&quot;This is an advertisement or vandalism\&quot;,\&quot;is_flag\&quot;:true,\&quot;is_custom_flag\&quot;:false},{\&quot;id\&quot;:6,\&quot;name_key\&quot;:\&quot;notify_user\&quot;,\&quot;name\&quot;:\&quot;Send @%{username} a message\&quot;,\&quot;description\&quot;:\&quot;I want to talk to this person directly and personally about their post.\&quot;,\&quot;short_description\&quot;:\&quot;I want to talk to this person directly and personally about their post.\&quot;,\&quot;is_flag\&quot;:true,\&quot;is_custom_flag\&quot;:true},{\&quot;id\&quot;:null,\&quot;name_key\&quot;:null,\&quot;name\&quot;:\&quot;translation missing: en.post_action_types..title\&quot;,\&quot;description\&quot;:\&quot;translation missing: en.post_action_types.description\&quot;,\&quot;short_description\&quot;:\&quot;translation missing: en.post_action_types.short_description\&quot;,\&quot;is_flag\&quot;:false,\&quot;is_custom_flag\&quot;:false},{\&quot;id\&quot;:7,\&quot;name_key\&quot;:\&quot;notify_moderators\&quot;,\&quot;name\&quot;:\&quot;Something Else\&quot;,\&quot;description\&quot;:\&quot;This post requires staff attention for another reason not listed above.\&quot;,\&quot;short_description\&quot;:\&quot;Requires staff attention for another reason\&quot;,\&quot;is_flag\&quot;:true,\&quot;is_custom_flag\&quot;:true}],\&quot;topic_flag_types\&quot;:[{\&quot;id\&quot;:4,\&quot;name_key\&quot;:\&quot;inappropriate\&quot;,\&quot;name\&quot;:\&quot;Inappropriate\&quot;,\&quot;description\&quot;:\&quot;This topic contains content that a reasonable person would consider offensive, abusive, or a violation of \\u003ca href=\\\&quot;/guidelines\\\&quot;\\u003eour community guidelines\\u003c/a\\u003e.\&quot;,\&quot;short_description\&quot;:\&quot;A violation of \\u003ca href=\\\&quot;/guidelines\\\&quot;\\u003eour community guidelines\\u003c/a\\u003e\&quot;,\&quot;is_flag\&quot;:true,\&quot;is_custom_flag\&quot;:false},{\&quot;id\&quot;:8,\&quot;name_key\&quot;:\&quot;spam\&quot;,\&quot;name\&quot;:\&quot;Spam\&quot;,\&quot;description\&quot;:\&quot;This topic is an advertisement. It is not useful or relevant to this site, but promotional in nature.\&quot;,\&quot;short_description\&quot;:\&quot;This is an advertisement\&quot;,\&quot;is_flag\&quot;:true,\&quot;is_custom_flag\&quot;:false},{\&quot;id\&quot;:null,\&quot;name_key\&quot;:null,\&quot;name\&quot;:\&quot;translation missing: en.topic_flag_types..title\&quot;,\&quot;description\&quot;:\&quot;translation missing: en.topic_flag_types.description\&quot;,\&quot;short_description\&quot;:\&quot;translation missing: en.topic_flag_types.short_description\&quot;,\&quot;is_flag\&quot;:false,\&quot;is_custom_flag\&quot;:false},{\&quot;id\&quot;:7,\&quot;name_key\&quot;:\&quot;notify_moderators\&quot;,\&quot;name\&quot;:\&quot;Something Else\&quot;,\&quot;description\&quot;:\&quot;This topic requires general staff attention based on the \\u003ca href=\\\&quot;/guidelines\\\&quot;\\u003eguidelines\\u003c/a\\u003e, \\u003ca href=\\\&quot;https://ionicframework.com/tos\\\&quot;\\u003eTOS\\u003c/a\\u003e, or for another reason not listed above.\&quot;,\&quot;short_description\&quot;:\&quot;Requires staff attention for another reason\&quot;,\&quot;is_flag\&quot;:true,\&quot;is_custom_flag\&quot;:true}],\&quot;can_create_tag\&quot;:null,\&quot;can_tag_topics\&quot;:null,\&quot;can_tag_pms\&quot;:false,\&quot;tags_filter_regexp\&quot;:\&quot;[/\\\\?#\\\\[\\\\]@!\\\\$\\u0026&#39;\\\\(\\\\)\\\\*\\\\+,;=\\\\.%\\\\\\\\`^\\\\s|\\\\{\\\\}\\\&quot;\\u003c\\u003e]+\&quot;,\&quot;top_tags\&quot;:[\&quot;faq\&quot;],\&quot;topic_featured_link_allowed_category_ids\&quot;:[6,13,31,26,24,30,12,23,27,17,25,14,16,28,3,18,5,7,4,19,29,15,21,20],\&quot;user_themes\&quot;:[{\&quot;theme_id\&quot;:3,\&quot;name\&quot;:\&quot;Default\&quot;,\&quot;default\&quot;:true,\&quot;color_scheme_id\&quot;:1}],\&quot;user_color_schemes\&quot;:[],\&quot;default_dark_color_scheme\&quot;:null,\&quot;censored_regexp\&quot;:null,\&quot;custom_emoji_translation\&quot;:{},\&quot;watched_words_replace\&quot;:null,\&quot;watched_words_link\&quot;:null,\&quot;categories\&quot;:[{\&quot;id\&quot;:23,\&quot;name\&quot;:\&quot;Ionic Framework\&quot;,\&quot;color\&quot;:\&quot;3C80FF\&quot;,\&quot;text_color\&quot;:\&quot;FFFFFF\&quot;,\&quot;slug\&quot;:\&quot;ionic\&quot;,\&quot;topic_count\&quot;:7283,\&quot;post_count\&quot;:25506,\&quot;position\&quot;:0,\&quot;description\&quot;:\&quot;This category is for all posts related to modern \\u003ca href=\\\&quot;http://ionicframework.com/\\\&quot;\\u003eIonic Framework\\u003c/a\\u003e, including \\u003ca href=\\\&quot;https://forum.ionicframework.com/c/ionic/angular/27\\\&quot;\\u003eIonic Angular\\u003c/a\\u003e, \\u003ca href=\\\&quot;https://forum.ionicframework.com/c/ionic/react/28\\\&quot;\\u003eIonic React\\u003c/a\\u003e, and \\u003ca href=\\\&quot;https://forum.ionicframework.com/c/ionic/vue/29\\\&quot;\\u003eIonic Vue\\u003c/a\\u003e. This includes all versions of Ionic Framework, from 4.0 and up.\&quot;,\&quot;description_text\&quot;:\&quot;This category is for all posts related to modern Ionic Framework, including Ionic Angular, Ionic React, and Ionic Vue. This includes all versions of Ionic Framework, from 4.0 and up.\&quot;,\&quot;description_excerpt\&quot;:\&quot;This category is for all posts related to modern \\u003ca href=\\\&quot;http://ionicframework.com/\\\&quot;\\u003eIonic Framework\\u003c/a\\u003e, including \\u003ca href=\\\&quot;https://forum.ionicframework.com/c/ionic/angular/27\\\&quot;\\u003eIonic Angular\\u003c/a\\u003e, \\u003ca href=\\\&quot;https://forum.ionicframework.com/c/ionic/react/28\\\&quot;\\u003eIonic React\\u003c/a\\u003e, and \\u003ca href=\\\&quot;https://forum.ionicframework.com/c/ionic/vue/29\\\&quot;\\u003eIonic Vue\\u003c/a\\u003e. This includes all versions of Ionic Framework, from 4.0 and up.\&quot;,\&quot;topic_url\&quot;:\&quot;/t/about-the-ionic-framework-category/136377\&quot;,\&quot;read_restricted\&quot;:false,\&quot;permission\&quot;:null,\&quot;notification_level\&quot;:1,\&quot;topic_template\&quot;:\&quot;Please describe the question in detail and share your code, configuration, and other relevant info.\&quot;,\&quot;has_children\&quot;:true,\&quot;sort_order\&quot;:\&quot;\&quot;,\&quot;sort_ascending\&quot;:null,\&quot;show_subcategory_list\&quot;:false,\&quot;num_featured_topics\&quot;:3,\&quot;default_view\&quot;:\&quot;\&quot;,\&quot;subcategory_list_style\&quot;:\&quot;rows_with_featured_topics\&quot;,\&quot;default_top_period\&quot;:\&quot;all\&quot;,\&quot;default_list_filter\&quot;:\&quot;all\&quot;,\&quot;minimum_required_tags\&quot;:0,\&quot;navigate_to_first_post_after_read\&quot;:false,\&quot;custom_fields\&quot;:{\&quot;enable_unassigned_filter\&quot;:null,\&quot;enable_accepted_answers\&quot;:null},\&quot;allowed_tags\&quot;:[],\&quot;allowed_tag_groups\&quot;:[],\&quot;allow_global_tags\&quot;:false,\&quot;min_tags_from_required_group\&quot;:1,\&quot;required_tag_group_name\&quot;:null,\&quot;read_only_banner\&quot;:\&quot;\&quot;,\&quot;uploaded_logo\&quot;:{\&quot;id\&quot;:139185,\&quot;url\&quot;:\&quot;//discourse-cloud-file-uploads.s3.dualstack.us-west-2.amazonaws.com/ionicframework/original/3X/a/4/a488f17e4616738ff04531ef23fa4572a4659d64.png\&quot;,\&quot;width\&quot;:512,\&quot;height\&quot;:512},\&quot;uploaded_background\&quot;:null,\&quot;can_edit\&quot;:false},{\&quot;id\&quot;:27,\&quot;name\&quot;:\&quot;Ionic Angular\&quot;,\&quot;color\&quot;:\&quot;DD0031\&quot;,\&quot;text_color\&quot;:\&quot;FFFFFF\&quot;,\&quot;slug\&quot;:\&quot;angular\&quot;,\&quot;topic_count\&quot;:2042,\&quot;post_count\&quot;:6363,\&quot;position\&quot;:1,\&quot;description\&quot;:\&quot;This category is for anything related to Ionic Angular, the official Angular version of \\u003ca href=\\\&quot;https://ionicframework.com\\\&quot;\\u003eIonic Framework\\u003c/a\\u003e.\&quot;,\&quot;description_text\&quot;:\&quot;This category is for anything related to Ionic Angular, the official Angular version of Ionic Framework.\&quot;,\&quot;description_excerpt\&quot;:\&quot;This category is for anything related to Ionic Angular, the official Angular version of \\u003ca href=\\\&quot;https://ionicframework.com\\\&quot;\\u003eIonic Framework\\u003c/a\\u003e.\&quot;,\&quot;topic_url\&quot;:\&quot;/t/about-the-ionic-angular-category/179165\&quot;,\&quot;read_restricted\&quot;:false,\&quot;permission\&quot;:null,\&quot;parent_category_id\&quot;:23,\&quot;notification_level\&quot;:1,\&quot;topic_template\&quot;:\&quot;\&quot;,\&quot;has_children\&quot;:false,\&quot;sort_order\&quot;:\&quot;\&quot;,\&quot;sort_ascending\&quot;:null,\&quot;show_subcategory_list\&quot;:false,\&quot;num_featured_topics\&quot;:3,\&quot;default_view\&quot;:\&quot;\&quot;,\&quot;subcategory_list_style\&quot;:\&quot;rows_with_featured_topics\&quot;,\&quot;default_top_period\&quot;:\&quot;all\&quot;,\&quot;default_list_filter\&quot;:\&quot;all\&quot;,\&quot;minimum_required_tags\&quot;:0,\&quot;navigate_to_first_post_after_read\&quot;:false,\&quot;custom_fields\&quot;:{\&quot;enable_unassigned_filter\&quot;:null,\&quot;enable_accepted_answers\&quot;:null},\&quot;allowed_tags\&quot;:[],\&quot;allowed_tag_groups\&quot;:[],\&quot;allow_global_tags\&quot;:false,\&quot;min_tags_from_required_group\&quot;:1,\&quot;required_tag_group_name\&quot;:null,\&quot;read_only_banner\&quot;:\&quot;\&quot;,\&quot;uploaded_logo\&quot;:{\&quot;id\&quot;:139202,\&quot;url\&quot;:\&quot;//discourse-cloud-file-uploads.s3.dualstack.us-west-2.amazonaws.com/ionicframework/original/3X/9/4/94e7079b5bffc5cd6b8dc0a8ca87c6a327ec69d5.png\&quot;,\&quot;width\&quot;:512,\&quot;height\&quot;:512},\&quot;uploaded_background\&quot;:null,\&quot;can_edit\&quot;:false},{\&quot;id\&quot;:28,\&quot;name\&quot;:\&quot;Ionic React\&quot;,\&quot;color\&quot;:\&quot;61dafb\&quot;,\&quot;text_color\&quot;:\&quot;FFFFFF\&quot;,\&quot;slug\&quot;:\&quot;react\&quot;,\&quot;topic_count\&quot;:606,\&quot;post_count\&quot;:1819,\&quot;position\&quot;:2,\&quot;description\&quot;:\&quot;This category is for anything related to Ionic React, the official React version of \\u003ca href=\\\&quot;https://ionicframework.com\\\&quot;\\u003eIonic Framework\\u003c/a\\u003e.\&quot;,\&quot;description_text\&quot;:\&quot;This category is for anything related to Ionic React, the official React version of Ionic Framework.\&quot;,\&quot;description_excerpt\&quot;:\&quot;This category is for anything related to Ionic React, the official React version of \\u003ca href=\\\&quot;https://ionicframework.com\\\&quot;\\u003eIonic Framework\\u003c/a\\u003e.\&quot;,\&quot;topic_url\&quot;:\&quot;/t/about-the-ionic-react-category/179166\&quot;,\&quot;read_restricted\&quot;:false,\&quot;permission\&quot;:null,\&quot;parent_category_id\&quot;:23,\&quot;notification_level\&quot;:1,\&quot;topic_template\&quot;:\&quot;\&quot;,\&quot;has_children\&quot;:false,\&quot;sort_order\&quot;:\&quot;\&quot;,\&quot;sort_ascending\&quot;:null,\&quot;show_subcategory_list\&quot;:false,\&quot;num_featured_topics\&quot;:3,\&quot;default_view\&quot;:\&quot;\&quot;,\&quot;subcategory_list_style\&quot;:\&quot;rows_with_featured_topics\&quot;,\&quot;default_top_period\&quot;:\&quot;all\&quot;,\&quot;default_list_filter\&quot;:\&quot;all\&quot;,\&quot;minimum_required_tags\&quot;:0,\&quot;navigate_to_first_post_after_read\&quot;:false,\&quot;custom_fields\&quot;:{\&quot;enable_unassigned_filter\&quot;:null,\&quot;enable_accepted_answers\&quot;:null},\&quot;allowed_tags\&quot;:[],\&quot;allowed_tag_groups\&quot;:[],\&quot;allow_global_tags\&quot;:false,\&quot;min_tags_from_required_group\&quot;:1,\&quot;required_tag_group_name\&quot;:null,\&quot;read_only_banner\&quot;:\&quot;\&quot;,\&quot;uploaded_logo\&quot;:{\&quot;id\&quot;:139203,\&quot;url\&quot;:\&quot;//discourse-cloud-file-uploads.s3.dualstack.us-west-2.amazonaws.com/ionicframework/original/3X/e/1/e1b4c4373465945fce1941ce27985faca49f2d61.png\&quot;,\&quot;width\&quot;:512,\&quot;height\&quot;:512},\&quot;uploaded_background\&quot;:null,\&quot;can_edit\&quot;:false},{\&quot;id\&quot;:29,\&quot;name\&quot;:\&quot;Ionic Vue\&quot;,\&quot;color\&quot;:\&quot;42b983\&quot;,\&quot;text_color\&quot;:\&quot;FFFFFF\&quot;,\&quot;slug\&quot;:\&quot;vue\&quot;,\&quot;topic_count\&quot;:515,\&quot;post_count\&quot;:2080,\&quot;position\&quot;:3,\&quot;description\&quot;:\&quot;This category is for anything related to Ionic Vue, the official Vue version of \\u003ca href=\\\&quot;https://ionicframework.com\\\&quot;\\u003eIonic Framework\\u003c/a\\u003e.\&quot;,\&quot;description_text\&quot;:\&quot;This category is for anything related to Ionic Vue, the official Vue version of Ionic Framework.\&quot;,\&quot;description_excerpt\&quot;:\&quot;This category is for anything related to Ionic Vue, the official Vue version of \\u003ca href=\\\&quot;https://ionicframework.com\\\&quot;\\u003eIonic Framework\\u003c/a\\u003e.\&quot;,\&quot;topic_url\&quot;:\&quot;/t/about-the-ionic-vue-category/197495\&quot;,\&quot;read_restricted\&quot;:false,\&quot;permission\&quot;:null,\&quot;parent_category_id\&quot;:23,\&quot;notification_level\&quot;:1,\&quot;topic_template\&quot;:\&quot;\&quot;,\&quot;has_children\&quot;:false,\&quot;sort_order\&quot;:\&quot;\&quot;,\&quot;sort_ascending\&quot;:null,\&quot;show_subcategory_list\&quot;:false,\&quot;num_featured_topics\&quot;:3,\&quot;default_view\&quot;:\&quot;\&quot;,\&quot;subcategory_list_style\&quot;:\&quot;rows_with_featured_topics\&quot;,\&quot;default_top_period\&quot;:\&quot;all\&quot;,\&quot;default_list_filter\&quot;:\&quot;all\&quot;,\&quot;minimum_required_tags\&quot;:0,\&quot;navigate_to_first_post_after_read\&quot;:false,\&quot;custom_fields\&quot;:{\&quot;enable_unassigned_filter\&quot;:null,\&quot;enable_accepted_answers\&quot;:null},\&quot;allowed_tags\&quot;:[],\&quot;allowed_tag_groups\&quot;:[],\&quot;allow_global_tags\&quot;:false,\&quot;min_tags_from_required_group\&quot;:1,\&quot;required_tag_group_name\&quot;:null,\&quot;read_only_banner\&quot;:\&quot;\&quot;,\&quot;uploaded_logo\&quot;:{\&quot;id\&quot;:139204,\&quot;url\&quot;:\&quot;//discourse-cloud-file-uploads.s3.dualstack.us-west-2.amazonaws.com/ionicframework/original/3X/3/4/34fb900237aaa7267b3c4a607769d9fd154688f6.png\&quot;,\&quot;width\&quot;:512,\&quot;height\&quot;:512},\&quot;uploaded_background\&quot;:null,\&quot;can_edit\&quot;:false},{\&quot;id\&quot;:18,\&quot;name\&quot;:\&quot;ionic-v3\&quot;,\&quot;color\&quot;:\&quot;12A89D\&quot;,\&quot;text_color\&quot;:\&quot;FFFFFF\&quot;,\&quot;slug\&quot;:\&quot;ionic-v3\&quot;,\&quot;topic_count\&quot;:38553,\&quot;post_count\&quot;:173542,\&quot;position\&quot;:4,\&quot;description\&quot;:\&quot;The \\u003cstrong\\u003eIonic-v3\\u003c/strong\\u003e category is for all posts related to \\u003ccode\\u003eionic-angular\\u003c/code\\u003e the framework itself.\\u003cbr\\u003e\\nIf you have any questions about the forum, please use the meta tag instead.\&quot;,\&quot;description_text\&quot;:\&quot;The Ionic-v3 category is for all posts related to ionic-angular the framework itself.\\nIf you have any questions about the forum, please use the meta tag instead.\&quot;,\&quot;description_excerpt\&quot;:\&quot;The Ionic-v3 category is for all posts related to ionic-angular the framework itself. \\nIf you have any questions about the forum, please use the meta tag instead.\&quot;,\&quot;topic_url\&quot;:\&quot;/t/about-the-ionic-v3-category/35251\&quot;,\&quot;read_restricted\&quot;:false,\&quot;permission\&quot;:null,\&quot;parent_category_id\&quot;:23,\&quot;notification_level\&quot;:1,\&quot;topic_template\&quot;:\&quot;\&quot;,\&quot;has_children\&quot;:false,\&quot;sort_order\&quot;:\&quot;\&quot;,\&quot;sort_ascending\&quot;:null,\&quot;show_subcategory_list\&quot;:false,\&quot;num_featured_topics\&quot;:3,\&quot;default_view\&quot;:\&quot;latest\&quot;,\&quot;subcategory_list_style\&quot;:\&quot;rows_with_featured_topics\&quot;,\&quot;default_top_period\&quot;:\&quot;all\&quot;,\&quot;default_list_filter\&quot;:\&quot;all\&quot;,\&quot;minimum_required_tags\&quot;:0,\&quot;navigate_to_first_post_after_read\&quot;:false,\&quot;custom_fields\&quot;:{\&quot;enable_unassigned_filter\&quot;:null,\&quot;enable_accepted_answers\&quot;:null},\&quot;allowed_tags\&quot;:[],\&quot;allowed_tag_groups\&quot;:[],\&quot;allow_global_tags\&quot;:false,\&quot;min_tags_from_required_group\&quot;:1,\&quot;required_tag_group_name\&quot;:null,\&quot;read_only_banner\&quot;:null,\&quot;uploaded_logo\&quot;:null,\&quot;uploaded_background\&quot;:null,\&quot;can_edit\&quot;:false},{\&quot;id\&quot;:26,\&quot;name\&quot;:\&quot;Capacitor\&quot;,\&quot;color\&quot;:\&quot;4BB5FF\&quot;,\&quot;text_color\&quot;:\&quot;FFFFFF\&quot;,\&quot;slug\&quot;:\&quot;capacitor\&quot;,\&quot;topic_count\&quot;:1120,\&quot;post_count\&quot;:3598,\&quot;position\&quot;:5,\&quot;description\&quot;:\&quot;\\u003ca href=\\\&quot;https://capacitorjs.com/\\\&quot;\\u003eCapacitor\\u003c/a\\u003e is the native runtime that powers modern Web Native apps, providing tooling, plugins, and the ability to provide full native access to any web app running on mobile. Capacitor works with Ionic Framework but can be used with any modern web app technology.\&quot;,\&quot;description_text\&quot;:\&quot;Capacitor is the native runtime that powers modern Web Native apps, providing tooling, plugins, and the ability to provide full native access to any web app running on mobile. Capacitor works with Ionic Framework but can be used with any modern web app technology.\&quot;,\&quot;description_excerpt\&quot;:\&quot;\\u003ca href=\\\&quot;https://capacitorjs.com/\\\&quot;\\u003eCapacitor\\u003c/a\\u003e is the native runtime that powers modern Web Native apps, providing tooling, plugins, and the ability to provide full native access to any web app running on mobile. Capacitor works with Ionic Framework but can be used with any modern web app technology.\&quot;,\&quot;topic_url\&quot;:\&quot;/t/about-the-capacitor-category/166587\&quot;,\&quot;read_restricted\&quot;:false,\&quot;permission\&quot;:null,\&quot;notification_level\&quot;:1,\&quot;topic_template\&quot;:\&quot;Please describe the question in detail and share your code, configuration, and other relevant info.\&quot;,\&quot;has_children\&quot;:false,\&quot;sort_order\&quot;:\&quot;\&quot;,\&quot;sort_ascending\&quot;:null,\&quot;show_subcategory_list\&quot;:false,\&quot;num_featured_topics\&quot;:3,\&quot;default_view\&quot;:\&quot;\&quot;,\&quot;subcategory_list_style\&quot;:\&quot;rows_with_featured_topics\&quot;,\&quot;default_top_period\&quot;:\&quot;all\&quot;,\&quot;default_list_filter\&quot;:\&quot;all\&quot;,\&quot;minimum_required_tags\&quot;:0,\&quot;navigate_to_first_post_after_read\&quot;:false,\&quot;custom_fields\&quot;:{\&quot;enable_unassigned_filter\&quot;:null,\&quot;enable_accepted_answers\&quot;:null},\&quot;allowed_tags\&quot;:[],\&quot;allowed_tag_groups\&quot;:[],\&quot;allow_global_tags\&quot;:false,\&quot;min_tags_from_required_group\&quot;:1,\&quot;required_tag_group_name\&quot;:null,\&quot;read_only_banner\&quot;:\&quot;\&quot;,\&quot;uploaded_logo\&quot;:{\&quot;id\&quot;:134546,\&quot;url\&quot;:\&quot;//discourse-cloud-file-uploads.s3.dualstack.us-west-2.amazonaws.com/ionicframework/original/3X/5/e/5e6a13a860b64192ad412b32cefa12efcbda704b.png\&quot;,\&quot;width\&quot;:512,\&quot;height\&quot;:512},\&quot;uploaded_background\&quot;:null,\&quot;can_edit\&quot;:false},{\&quot;id\&quot;:20,\&quot;name\&quot;:\&quot;Appflow\&quot;,\&quot;color\&quot;:\&quot;4F68FF\&quot;,\&quot;text_color\&quot;:\&quot;FFFFFF\&quot;,\&quot;slug\&quot;:\&quot;ionic-appflow\&quot;,\&quot;topic_count\&quot;:1410,\&quot;post_count\&quot;:6150,\&quot;position\&quot;:6,\&quot;description\&quot;:\&quot;Topics related to \\u003ca href=\\\&quot;https://ionic.io/appflow\\\&quot;\\u003eAppflow\\u003c/a\\u003e, the official Mobile DevOps and CI/CD service for Capacitor/Cordova/Ionic apps.\&quot;,\&quot;description_text\&quot;:\&quot;Topics related to Appflow, the official Mobile DevOps and CI\\u0026#x2F;CD service for Capacitor\\u0026#x2F;Cordova\\u0026#x2F;Ionic apps.\&quot;,\&quot;description_excerpt\&quot;:\&quot;Topics related to \\u003ca href=\\\&quot;https://ionic.io/appflow\\\&quot;\\u003eAppflow\\u003c/a\\u003e, the official Mobile DevOps and CI/CD service for Capacitor/Cordova/Ionic apps.\&quot;,\&quot;topic_url\&quot;:\&quot;/t/about-the-appflow-category/109841\&quot;,\&quot;read_restricted\&quot;:false,\&quot;permission\&quot;:null,\&quot;notification_level\&quot;:1,\&quot;topic_template\&quot;:\&quot;Login trouble? Build errors? Production issues? Open a ticket by emailing support@ionic.io. Use the email address your account is registered under and include the Appflow App ID.\\n\&quot;,\&quot;has_children\&quot;:false,\&quot;sort_order\&quot;:\&quot;\&quot;,\&quot;sort_ascending\&quot;:null,\&quot;show_subcategory_list\&quot;:false,\&quot;num_featured_topics\&quot;:3,\&quot;default_view\&quot;:\&quot;latest\&quot;,\&quot;subcategory_list_style\&quot;:\&quot;rows_with_featured_topics\&quot;,\&quot;default_top_period\&quot;:\&quot;all\&quot;,\&quot;default_list_filter\&quot;:\&quot;all\&quot;,\&quot;minimum_required_tags\&quot;:0,\&quot;navigate_to_first_post_after_read\&quot;:false,\&quot;custom_fields\&quot;:{\&quot;enable_unassigned_filter\&quot;:null,\&quot;enable_accepted_answers\&quot;:null},\&quot;allowed_tags\&quot;:[],\&quot;allowed_tag_groups\&quot;:[],\&quot;allow_global_tags\&quot;:false,\&quot;min_tags_from_required_group\&quot;:1,\&quot;required_tag_group_name\&quot;:null,\&quot;read_only_banner\&quot;:\&quot;\&quot;,\&quot;uploaded_logo\&quot;:{\&quot;id\&quot;:134547,\&quot;url\&quot;:\&quot;//discourse-cloud-file-uploads.s3.dualstack.us-west-2.amazonaws.com/ionicframework/original/3X/b/9/b9d93e9bf8dfbf066fcad98477cb1adc886d001e.png\&quot;,\&quot;width\&quot;:512,\&quot;height\&quot;:512},\&quot;uploaded_background\&quot;:null,\&quot;can_edit\&quot;:false},{\&quot;id\&quot;:21,\&quot;name\&quot;:\&quot;Stencil\&quot;,\&quot;color\&quot;:\&quot;161616\&quot;,\&quot;text_color\&quot;:\&quot;FFFFFF\&quot;,\&quot;slug\&quot;:\&quot;stencil\&quot;,\&quot;topic_count\&quot;:194,\&quot;post_count\&quot;:557,\&quot;position\&quot;:7,\&quot;description\&quot;:\&quot;Topics related to \\u003ca href=\\\&quot;https://stenciljs.com/\\\&quot;\\u003eStencil\\u003c/a\\u003e, the toolchain for building reusable, scalable Design Systems and blazing fast static web apps.\&quot;,\&quot;description_text\&quot;:\&quot;Topics related to Stencil, the toolchain for building reusable, scalable Design Systems and blazing fast static web apps.\&quot;,\&quot;description_excerpt\&quot;:\&quot;Topics related to \\u003ca href=\\\&quot;https://stenciljs.com/\\\&quot;\\u003eStencil\\u003c/a\\u003e, the toolchain for building reusable, scalable Design Systems and blazing fast static web apps.\&quot;,\&quot;topic_url\&quot;:\&quot;/t/about-the-stencil-category/125380\&quot;,\&quot;read_restricted\&quot;:false,\&quot;permission\&quot;:null,\&quot;notification_level\&quot;:1,\&quot;topic_template\&quot;:\&quot;\\u003c!-- Please remember to search the forum first before posting a new question. Thanks! --\\u003e\&quot;,\&quot;has_children\&quot;:false,\&quot;sort_order\&quot;:\&quot;\&quot;,\&quot;sort_ascending\&quot;:null,\&quot;show_subcategory_list\&quot;:false,\&quot;num_featured_topics\&quot;:3,\&quot;default_view\&quot;:\&quot;\&quot;,\&quot;subcategory_list_style\&quot;:\&quot;rows_with_featured_topics\&quot;,\&quot;default_top_period\&quot;:\&quot;all\&quot;,\&quot;default_list_filter\&quot;:\&quot;all\&quot;,\&quot;minimum_required_tags\&quot;:0,\&quot;navigate_to_first_post_after_read\&quot;:false,\&quot;custom_fields\&quot;:{\&quot;enable_unassigned_filter\&quot;:null,\&quot;enable_accepted_answers\&quot;:null},\&quot;allowed_tags\&quot;:[],\&quot;allowed_tag_groups\&quot;:[],\&quot;allow_global_tags\&quot;:false,\&quot;min_tags_from_required_group\&quot;:1,\&quot;required_tag_group_name\&quot;:null,\&quot;read_only_banner\&quot;:\&quot;\&quot;,\&quot;uploaded_logo\&quot;:{\&quot;id\&quot;:134548,\&quot;url\&quot;:\&quot;//discourse-cloud-file-uploads.s3.dualstack.us-west-2.amazonaws.com/ionicframework/original/3X/2/d/2dfb1c5b66a1eb853fefa04602e628fa8388a89b.png\&quot;,\&quot;width\&quot;:512,\&quot;height\&quot;:512},\&quot;uploaded_background\&quot;:null,\&quot;can_edit\&quot;:false},{\&quot;id\&quot;:31,\&quot;name\&quot;:\&quot;Portals\&quot;,\&quot;color\&quot;:\&quot;0038C9\&quot;,\&quot;text_color\&quot;:\&quot;FFFFFF\&quot;,\&quot;slug\&quot;:\&quot;portals\&quot;,\&quot;topic_count\&quot;:1,\&quot;post_count\&quot;:2,\&quot;position\&quot;:8,\&quot;description\&quot;:\&quot;\\u003ca href=\\\&quot;https://ionic.io/portals\\\&quot;\\u003eIonic Portals\\u003c/a\\u003e is a supercharged native Web View component for iOS and Android that lets you add web-based experiences to native mobile apps. It enables native and web teams to better collaborate and bring new and existing web experiences to mobile in a safe, controlled way.\&quot;,\&quot;description_text\&quot;:\&quot;Ionic Portals is a supercharged native Web View component for iOS and Android that lets you add web-based experiences to native mobile apps. It enables native and web teams to better collaborate and bring new and existing web experiences to mobile in a safe, controlled way.\&quot;,\&quot;description_excerpt\&quot;:\&quot;\\u003ca href=\\\&quot;https://ionic.io/portals\\\&quot;\\u003eIonic Portals\\u003c/a\\u003e is a supercharged native Web View component for iOS and Android that lets you add web-based experiences to native mobile apps. It enables native and web teams to better collaborate and bring new and existing web experiences to mobile in a safe, controlled way.\&quot;,\&quot;topic_url\&quot;:\&quot;/t/about-the-portals-category/215462\&quot;,\&quot;read_restricted\&quot;:false,\&quot;permission\&quot;:null,\&quot;notification_level\&quot;:1,\&quot;topic_template\&quot;:\&quot;\&quot;,\&quot;has_children\&quot;:false,\&quot;sort_order\&quot;:\&quot;\&quot;,\&quot;sort_ascending\&quot;:null,\&quot;show_subcategory_list\&quot;:false,\&quot;num_featured_topics\&quot;:3,\&quot;default_view\&quot;:\&quot;\&quot;,\&quot;subcategory_list_style\&quot;:\&quot;rows_with_featured_topics\&quot;,\&quot;default_top_period\&quot;:\&quot;all\&quot;,\&quot;default_list_filter\&quot;:\&quot;all\&quot;,\&quot;minimum_required_tags\&quot;:0,\&quot;navigate_to_first_post_after_read\&quot;:false,\&quot;custom_fields\&quot;:{\&quot;enable_unassigned_filter\&quot;:null,\&quot;enable_accepted_answers\&quot;:null},\&quot;allowed_tags\&quot;:[],\&quot;allowed_tag_groups\&quot;:[],\&quot;allow_global_tags\&quot;:false,\&quot;min_tags_from_required_group\&quot;:1,\&quot;required_tag_group_name\&quot;:null,\&quot;read_only_banner\&quot;:\&quot;\&quot;,\&quot;uploaded_logo\&quot;:{\&quot;id\&quot;:139184,\&quot;url\&quot;:\&quot;//discourse-cloud-file-uploads.s3.dualstack.us-west-2.amazonaws.com/ionicframework/original/3X/5/e/5ef8e20aebf7c27e0dd34d4c12b3160dfb6c6651.png\&quot;,\&quot;width\&quot;:512,\&quot;height\&quot;:512},\&quot;uploaded_background\&quot;:null,\&quot;can_edit\&quot;:false},{\&quot;id\&quot;:6,\&quot;name\&quot;:\&quot;announcement\&quot;,\&quot;color\&quot;:\&quot;f7bc1d\&quot;,\&quot;text_color\&quot;:\&quot;FFFFFF\&quot;,\&quot;slug\&quot;:\&quot;announcement\&quot;,\&quot;topic_count\&quot;:60,\&quot;post_count\&quot;:831,\&quot;position\&quot;:9,\&quot;description\&quot;:\&quot;The Announcement category is used for Ionic-related updates and new releases. The devs will use this category periodically when appropriate.\&quot;,\&quot;description_text\&quot;:\&quot;The Announcement category is used for Ionic-related updates and new releases. The devs will use this category periodically when appropriate.\&quot;,\&quot;description_excerpt\&quot;:\&quot;The Announcement category is used for Ionic-related updates and new releases. The devs will use this category periodically when appropriate.\&quot;,\&quot;topic_url\&quot;:\&quot;/t/category-definition-for-announcement/476\&quot;,\&quot;read_restricted\&quot;:false,\&quot;permission\&quot;:null,\&quot;notification_level\&quot;:1,\&quot;topic_template\&quot;:null,\&quot;has_children\&quot;:false,\&quot;sort_order\&quot;:null,\&quot;sort_ascending\&quot;:null,\&quot;show_subcategory_list\&quot;:false,\&quot;num_featured_topics\&quot;:3,\&quot;default_view\&quot;:null,\&quot;subcategory_list_style\&quot;:\&quot;rows_with_featured_topics\&quot;,\&quot;default_top_period\&quot;:\&quot;all\&quot;,\&quot;default_list_filter\&quot;:\&quot;all\&quot;,\&quot;minimum_required_tags\&quot;:0,\&quot;navigate_to_first_post_after_read\&quot;:false,\&quot;custom_fields\&quot;:{\&quot;enable_unassigned_filter\&quot;:null,\&quot;enable_accepted_answers\&quot;:null},\&quot;allowed_tags\&quot;:[],\&quot;allowed_tag_groups\&quot;:[],\&quot;allow_global_tags\&quot;:false,\&quot;min_tags_from_required_group\&quot;:1,\&quot;required_tag_group_name\&quot;:null,\&quot;read_only_banner\&quot;:null,\&quot;uploaded_logo\&quot;:null,\&quot;uploaded_background\&quot;:null,\&quot;can_edit\&quot;:false},{\&quot;id\&quot;:24,\&quot;name\&quot;:\&quot;Site Feedback\&quot;,\&quot;color\&quot;:\&quot;808281\&quot;,\&quot;text_color\&quot;:\&quot;FFFFFF\&quot;,\&quot;slug\&quot;:\&quot;site-feedback\&quot;,\&quot;topic_count\&quot;:35,\&quot;post_count\&quot;:68,\&quot;position\&quot;:10,\&quot;description\&quot;:\&quot;Discussion about this site, its organization, how it works, and how we can improve it.\&quot;,\&quot;description_text\&quot;:\&quot;Discussion about this site, its organization, how it works, and how we can improve it.\&quot;,\&quot;description_excerpt\&quot;:\&quot;Discussion about this site, its organization, how it works, and how we can improve it.\&quot;,\&quot;topic_url\&quot;:\&quot;/t/about-the-site-feedback-category/162362\&quot;,\&quot;read_restricted\&quot;:false,\&quot;permission\&quot;:null,\&quot;notification_level\&quot;:1,\&quot;topic_template\&quot;:null,\&quot;has_children\&quot;:false,\&quot;sort_order\&quot;:null,\&quot;sort_ascending\&quot;:null,\&quot;show_subcategory_list\&quot;:false,\&quot;num_featured_topics\&quot;:3,\&quot;default_view\&quot;:null,\&quot;subcategory_list_style\&quot;:\&quot;rows_with_featured_topics\&quot;,\&quot;default_top_period\&quot;:\&quot;all\&quot;,\&quot;default_list_filter\&quot;:\&quot;all\&quot;,\&quot;minimum_required_tags\&quot;:0,\&quot;navigate_to_first_post_after_read\&quot;:false,\&quot;custom_fields\&quot;:{\&quot;enable_unassigned_filter\&quot;:null,\&quot;enable_accepted_answers\&quot;:null},\&quot;allowed_tags\&quot;:[],\&quot;allowed_tag_groups\&quot;:[],\&quot;allow_global_tags\&quot;:false,\&quot;min_tags_from_required_group\&quot;:1,\&quot;required_tag_group_name\&quot;:null,\&quot;read_only_banner\&quot;:null,\&quot;uploaded_logo\&quot;:null,\&quot;uploaded_background\&quot;:null,\&quot;can_edit\&quot;:false},{\&quot;id\&quot;:5,\&quot;name\&quot;:\&quot;ionic-v1\&quot;,\&quot;color\&quot;:\&quot;4e8cf9\&quot;,\&quot;text_color\&quot;:\&quot;FFFFFF\&quot;,\&quot;slug\&quot;:\&quot;ionic-v1\&quot;,\&quot;topic_count\&quot;:25082,\&quot;post_count\&quot;:95176,\&quot;position\&quot;:11,\&quot;description\&quot;:\&quot;The Ionic-v1 category is for all posts related to the Ionic V1 framework itself. If you have any questions about the forum, please use the \\u003ccode\\u003emeta\\u003c/code\\u003e tag instead.\&quot;,\&quot;description_text\&quot;:\&quot;The Ionic-v1 category is for all posts related to the Ionic V1 framework itself. If you have any questions about the forum, please use the meta tag instead.\&quot;,\&quot;description_excerpt\&quot;:\&quot;The Ionic-v1 category is for all posts related to the Ionic V1 framework itself. If you have any questions about the forum, please use the meta tag instead.\&quot;,\&quot;topic_url\&quot;:\&quot;/t/category-definition-for-ionic/50\&quot;,\&quot;read_restricted\&quot;:false,\&quot;permission\&quot;:null,\&quot;notification_level\&quot;:1,\&quot;topic_template\&quot;:\&quot;\&quot;,\&quot;has_children\&quot;:false,\&quot;sort_order\&quot;:\&quot;\&quot;,\&quot;sort_ascending\&quot;:null,\&quot;show_subcategory_list\&quot;:false,\&quot;num_featured_topics\&quot;:3,\&quot;default_view\&quot;:\&quot;latest\&quot;,\&quot;subcategory_list_style\&quot;:\&quot;rows_with_featured_topics\&quot;,\&quot;default_top_period\&quot;:\&quot;all\&quot;,\&quot;default_list_filter\&quot;:\&quot;all\&quot;,\&quot;minimum_required_tags\&quot;:0,\&quot;navigate_to_first_post_after_read\&quot;:false,\&quot;custom_fields\&quot;:{\&quot;enable_unassigned_filter\&quot;:null,\&quot;enable_accepted_answers\&quot;:null},\&quot;allowed_tags\&quot;:[],\&quot;allowed_tag_groups\&quot;:[],\&quot;allow_global_tags\&quot;:false,\&quot;min_tags_from_required_group\&quot;:1,\&quot;required_tag_group_name\&quot;:null,\&quot;read_only_banner\&quot;:null,\&quot;uploaded_logo\&quot;:null,\&quot;uploaded_background\&quot;:null,\&quot;can_edit\&quot;:false},{\&quot;id\&quot;:12,\&quot;name\&quot;:\&quot;Uncategorized\&quot;,\&quot;color\&quot;:\&quot;AB9364\&quot;,\&quot;text_color\&quot;:\&quot;FFFFFF\&quot;,\&quot;slug\&quot;:\&quot;uncategorized\&quot;,\&quot;topic_count\&quot;:5823,\&quot;post_count\&quot;:22822,\&quot;position\&quot;:12,\&quot;description\&quot;:\&quot;Topics that don&#39;t need a category, or don&#39;t fit into any other existing category.\&quot;,\&quot;description_text\&quot;:\&quot;Topics that don&#39;t need a category, or don&#39;t fit into any other existing category.\&quot;,\&quot;description_excerpt\&quot;:\&quot;Topics that don&#39;t need a category, or don&#39;t fit into any other existing category.\&quot;,\&quot;topic_url\&quot;:\&quot;/t/\&quot;,\&quot;read_restricted\&quot;:false,\&quot;permission\&quot;:null,\&quot;notification_level\&quot;:1,\&quot;topic_template\&quot;:null,\&quot;has_children\&quot;:false,\&quot;sort_order\&quot;:null,\&quot;sort_ascending\&quot;:null,\&quot;show_subcategory_list\&quot;:false,\&quot;num_featured_topics\&quot;:3,\&quot;default_view\&quot;:null,\&quot;subcategory_list_style\&quot;:\&quot;rows_with_featured_topics\&quot;,\&quot;default_top_period\&quot;:\&quot;all\&quot;,\&quot;default_list_filter\&quot;:\&quot;all\&quot;,\&quot;minimum_required_tags\&quot;:0,\&quot;navigate_to_first_post_after_read\&quot;:false,\&quot;custom_fields\&quot;:{\&quot;enable_unassigned_filter\&quot;:null,\&quot;enable_accepted_answers\&quot;:null},\&quot;allowed_tags\&quot;:[],\&quot;allowed_tag_groups\&quot;:[],\&quot;allow_global_tags\&quot;:false,\&quot;min_tags_from_required_group\&quot;:1,\&quot;required_tag_group_name\&quot;:null,\&quot;read_only_banner\&quot;:null,\&quot;uploaded_logo\&quot;:null,\&quot;uploaded_background\&quot;:null,\&quot;can_edit\&quot;:false},{\&quot;id\&quot;:19,\&quot;name\&quot;:\&quot;Ionic Native\&quot;,\&quot;color\&quot;:\&quot;BF1E2E\&quot;,\&quot;text_color\&quot;:\&quot;FFFFFF\&quot;,\&quot;slug\&quot;:\&quot;ionic-native\&quot;,\&quot;topic_count\&quot;:4037,\&quot;post_count\&quot;:15506,\&quot;position\&quot;:13,\&quot;description\&quot;:\&quot;Have a question about using Ionic Native plugins in your Ionic app? Feel free to post them here.\&quot;,\&quot;description_text\&quot;:\&quot;Have a question about using Ionic Native plugins in your Ionic app? Feel free to post them here.\&quot;,\&quot;description_excerpt\&quot;:\&quot;Have a question about using Ionic Native plugins in your Ionic app? Feel free to post them here.\&quot;,\&quot;topic_url\&quot;:\&quot;/t/about-the-ionic-native-category/89098\&quot;,\&quot;read_restricted\&quot;:false,\&quot;permission\&quot;:null,\&quot;notification_level\&quot;:1,\&quot;topic_template\&quot;:null,\&quot;has_children\&quot;:false,\&quot;sort_order\&quot;:\&quot;\&quot;,\&quot;sort_ascending\&quot;:null,\&quot;show_subcategory_list\&quot;:false,\&quot;num_featured_topics\&quot;:3,\&quot;default_view\&quot;:\&quot;latest\&quot;,\&quot;subcategory_list_style\&quot;:\&quot;rows_with_featured_topics\&quot;,\&quot;default_top_period\&quot;:\&quot;all\&quot;,\&quot;default_list_filter\&quot;:\&quot;all\&quot;,\&quot;minimum_required_tags\&quot;:0,\&quot;navigate_to_first_post_after_read\&quot;:false,\&quot;custom_fields\&quot;:{\&quot;enable_unassigned_filter\&quot;:null,\&quot;enable_accepted_answers\&quot;:null},\&quot;allowed_tags\&quot;:[],\&quot;allowed_tag_groups\&quot;:[],\&quot;allow_global_tags\&quot;:false,\&quot;min_tags_from_required_group\&quot;:1,\&quot;required_tag_group_name\&quot;:null,\&quot;read_only_banner\&quot;:null,\&quot;uploaded_logo\&quot;:null,\&quot;uploaded_background\&quot;:null,\&quot;can_edit\&quot;:false},{\&quot;id\&quot;:4,\&quot;name\&quot;:\&quot;tutorials\&quot;,\&quot;color\&quot;:\&quot;12A89D\&quot;,\&quot;text_color\&quot;:\&quot;FFFFFF\&quot;,\&quot;slug\&quot;:\&quot;tutorials\&quot;,\&quot;topic_count\&quot;:955,\&quot;post_count\&quot;:3675,\&quot;position\&quot;:14,\&quot;description\&quot;:\&quot;Ionic tutorials and tutorial discussion.\&quot;,\&quot;description_text\&quot;:\&quot;Ionic tutorials and tutorial discussion.\&quot;,\&quot;description_excerpt\&quot;:\&quot;Ionic tutorials and tutorial discussion.\&quot;,\&quot;topic_url\&quot;:\&quot;/t/tutorial-topics/14\&quot;,\&quot;read_restricted\&quot;:false,\&quot;permission\&quot;:null,\&quot;notification_level\&quot;:1,\&quot;topic_template\&quot;:null,\&quot;has_children\&quot;:false,\&quot;sort_order\&quot;:null,\&quot;sort_ascending\&quot;:null,\&quot;show_subcategory_list\&quot;:false,\&quot;num_featured_topics\&quot;:3,\&quot;default_view\&quot;:null,\&quot;subcategory_list_style\&quot;:\&quot;rows_with_featured_topics\&quot;,\&quot;default_top_period\&quot;:\&quot;all\&quot;,\&quot;default_list_filter\&quot;:\&quot;all\&quot;,\&quot;minimum_required_tags\&quot;:0,\&quot;navigate_to_first_post_after_read\&quot;:false,\&quot;custom_fields\&quot;:{\&quot;enable_unassigned_filter\&quot;:null,\&quot;enable_accepted_answers\&quot;:null},\&quot;allowed_tags\&quot;:[],\&quot;allowed_tag_groups\&quot;:[],\&quot;allow_global_tags\&quot;:false,\&quot;min_tags_from_required_group\&quot;:1,\&quot;required_tag_group_name\&quot;:null,\&quot;read_only_banner\&quot;:null,\&quot;uploaded_logo\&quot;:null,\&quot;uploaded_background\&quot;:null,\&quot;can_edit\&quot;:false},{\&quot;id\&quot;:7,\&quot;name\&quot;:\&quot;demo\&quot;,\&quot;color\&quot;:\&quot;92278F\&quot;,\&quot;text_color\&quot;:\&quot;FFFFFF\&quot;,\&quot;slug\&quot;:\&quot;demo\&quot;,\&quot;topic_count\&quot;:261,\&quot;post_count\&quot;:1863,\&quot;position\&quot;:16,\&quot;description\&quot;:\&quot;Use this category to show off coolness you&#39;ve built.\&quot;,\&quot;description_text\&quot;:\&quot;Use this category to show off coolness you\\u0026#x27;ve built.\&quot;,\&quot;description_excerpt\&quot;:\&quot;Use this category to show off coolness you\\u0026#39;ve built.\&quot;,\&quot;topic_url\&quot;:\&quot;/t/demo-category/620\&quot;,\&quot;read_restricted\&quot;:false,\&quot;permission\&quot;:null,\&quot;notification_level\&quot;:1,\&quot;topic_template\&quot;:null,\&quot;has_children\&quot;:false,\&quot;sort_order\&quot;:null,\&quot;sort_ascending\&quot;:null,\&quot;show_subcategory_list\&quot;:false,\&quot;num_featured_topics\&quot;:3,\&quot;default_view\&quot;:null,\&quot;subcategory_list_style\&quot;:\&quot;rows_with_featured_topics\&quot;,\&quot;default_top_period\&quot;:\&quot;all\&quot;,\&quot;default_list_filter\&quot;:\&quot;all\&quot;,\&quot;minimum_required_tags\&quot;:0,\&quot;navigate_to_first_post_after_read\&quot;:false,\&quot;custom_fields\&quot;:{\&quot;enable_unassigned_filter\&quot;:null,\&quot;enable_accepted_answers\&quot;:null},\&quot;allowed_tags\&quot;:[],\&quot;allowed_tag_groups\&quot;:[],\&quot;allow_global_tags\&quot;:false,\&quot;min_tags_from_required_group\&quot;:1,\&quot;required_tag_group_name\&quot;:null,\&quot;read_only_banner\&quot;:null,\&quot;uploaded_logo\&quot;:null,\&quot;uploaded_background\&quot;:null,\&quot;can_edit\&quot;:false},{\&quot;id\&quot;:15,\&quot;name\&quot;:\&quot;jobs\&quot;,\&quot;color\&quot;:\&quot;9EB83B\&quot;,\&quot;text_color\&quot;:\&quot;FFFFFF\&quot;,\&quot;slug\&quot;:\&quot;jobs\&quot;,\&quot;topic_count\&quot;:524,\&quot;post_count\&quot;:2862,\&quot;position\&quot;:18,\&quot;description\&quot;:\&quot;Here&#39;s where you can post open job opportunities for Ionic developers (please note whether the work is full-time or freelance).\&quot;,\&quot;description_text\&quot;:\&quot;Here\\u0026#x27;s where you can post open job opportunities for Ionic developers (please note whether the work is full-time or freelance).\&quot;,\&quot;description_excerpt\&quot;:\&quot;Here\\u0026#39;s where you can post open job opportunities for Ionic developers (please note whether the work is full-time or freelance).\&quot;,\&quot;topic_url\&quot;:\&quot;/t/about-the-jobs-category/12815\&quot;,\&quot;read_restricted\&quot;:false,\&quot;permission\&quot;:null,\&quot;notification_level\&quot;:1,\&quot;topic_template\&quot;:null,\&quot;has_children\&quot;:false,\&quot;sort_order\&quot;:null,\&quot;sort_ascending\&quot;:null,\&quot;show_subcategory_list\&quot;:false,\&quot;num_featured_topics\&quot;:3,\&quot;default_view\&quot;:null,\&quot;subcategory_list_style\&quot;:\&quot;rows_with_featured_topics\&quot;,\&quot;default_top_period\&quot;:\&quot;all\&quot;,\&quot;default_list_filter\&quot;:\&quot;all\&quot;,\&quot;minimum_required_tags\&quot;:0,\&quot;navigate_to_first_post_after_read\&quot;:false,\&quot;custom_fields\&quot;:{\&quot;enable_unassigned_filter\&quot;:null,\&quot;enable_accepted_answers\&quot;:null},\&quot;allowed_tags\&quot;:[],\&quot;allowed_tag_groups\&quot;:[],\&quot;allow_global_tags\&quot;:false,\&quot;min_tags_from_required_group\&quot;:1,\&quot;required_tag_group_name\&quot;:null,\&quot;read_only_banner\&quot;:null,\&quot;uploaded_logo\&quot;:null,\&quot;uploaded_background\&quot;:null,\&quot;can_edit\&quot;:false},{\&quot;id\&quot;:16,\&quot;name\&quot;:\&quot;cordova\&quot;,\&quot;color\&quot;:\&quot;652D90\&quot;,\&quot;text_color\&quot;:\&quot;FFFFFF\&quot;,\&quot;slug\&quot;:\&quot;cordova\&quot;,\&quot;topic_count\&quot;:1698,\&quot;post_count\&quot;:5232,\&quot;position\&quot;:19,\&quot;description\&quot;:\&quot;Any Cordova questions in your Ionic app?  Feel free to post them here.\&quot;,\&quot;description_text\&quot;:\&quot;Any Cordova questions in your Ionic app?  Feel free to post them here.\&quot;,\&quot;description_excerpt\&quot;:\&quot;Any Cordova questions in your Ionic app?  Feel free to post them here.\&quot;,\&quot;topic_url\&quot;:\&quot;/t/about-the-cordova-category/15980\&quot;,\&quot;read_restricted\&quot;:false,\&quot;permission\&quot;:null,\&quot;notification_level\&quot;:1,\&quot;topic_template\&quot;:\&quot;\&quot;,\&quot;has_children\&quot;:false,\&quot;sort_order\&quot;:\&quot;\&quot;,\&quot;sort_ascending\&quot;:null,\&quot;show_subcategory_list\&quot;:false,\&quot;num_featured_topics\&quot;:3,\&quot;default_view\&quot;:\&quot;\&quot;,\&quot;subcategory_list_style\&quot;:\&quot;rows_with_featured_topics\&quot;,\&quot;default_top_period\&quot;:\&quot;all\&quot;,\&quot;default_list_filter\&quot;:\&quot;all\&quot;,\&quot;minimum_required_tags\&quot;:0,\&quot;navigate_to_first_post_after_read\&quot;:false,\&quot;custom_fields\&quot;:{\&quot;enable_unassigned_filter\&quot;:null,\&quot;enable_accepted_answers\&quot;:null},\&quot;allowed_tags\&quot;:[],\&quot;allowed_tag_groups\&quot;:[],\&quot;allow_global_tags\&quot;:false,\&quot;min_tags_from_required_group\&quot;:1,\&quot;required_tag_group_name\&quot;:null,\&quot;read_only_banner\&quot;:null,\&quot;uploaded_logo\&quot;:null,\&quot;uploaded_background\&quot;:null,\&quot;can_edit\&quot;:false},{\&quot;id\&quot;:17,\&quot;name\&quot;:\&quot;showcase\&quot;,\&quot;color\&quot;:\&quot;F1592A\&quot;,\&quot;text_color\&quot;:\&quot;FFFFFF\&quot;,\&quot;slug\&quot;:\&quot;show-off-what-youre-working-on\&quot;,\&quot;topic_count\&quot;:298,\&quot;post_count\&quot;:1024,\&quot;position\&quot;:20,\&quot;description\&quot;:\&quot;Have an app you&#39;re really proud of? Or do you have a plugin that you want to promote or showoff? The showcase category is a place to share/showoff things that you have made with ionic.\&quot;,\&quot;description_text\&quot;:\&quot;Have an app you\\u0026#x27;re really proud of? Or do you have a plugin that you want to promote or showoff? The showcase category is a place to share\\u0026#x2F;showoff things that you have made with ionic.\&quot;,\&quot;description_excerpt\&quot;:\&quot;Have an app you\\u0026#39;re really proud of? Or do you have a plugin that you want to promote or showoff? The showcase category is a place to share/showoff things that you have made with ionic.\&quot;,\&quot;topic_url\&quot;:\&quot;/t/about-the-showcase-category/30669\&quot;,\&quot;read_restricted\&quot;:false,\&quot;permission\&quot;:null,\&quot;notification_level\&quot;:1,\&quot;topic_template\&quot;:null,\&quot;has_children\&quot;:false,\&quot;sort_order\&quot;:null,\&quot;sort_ascending\&quot;:null,\&quot;show_subcategory_list\&quot;:false,\&quot;num_featured_topics\&quot;:3,\&quot;default_view\&quot;:null,\&quot;subcategory_list_style\&quot;:\&quot;rows_with_featured_topics\&quot;,\&quot;default_top_period\&quot;:\&quot;all\&quot;,\&quot;default_list_filter\&quot;:\&quot;all\&quot;,\&quot;minimum_required_tags\&quot;:0,\&quot;navigate_to_first_post_after_read\&quot;:false,\&quot;custom_fields\&quot;:{\&quot;enable_unassigned_filter\&quot;:null,\&quot;enable_accepted_answers\&quot;:null},\&quot;allowed_tags\&quot;:[],\&quot;allowed_tag_groups\&quot;:[],\&quot;allow_global_tags\&quot;:false,\&quot;min_tags_from_required_group\&quot;:1,\&quot;required_tag_group_name\&quot;:null,\&quot;read_only_banner\&quot;:null,\&quot;uploaded_logo\&quot;:null,\&quot;uploaded_background\&quot;:null,\&quot;can_edit\&quot;:false},{\&quot;id\&quot;:3,\&quot;name\&quot;:\&quot;meta\&quot;,\&quot;color\&quot;:\&quot;B3B5B4\&quot;,\&quot;text_color\&quot;:\&quot;FFFFFF\&quot;,\&quot;slug\&quot;:\&quot;meta\&quot;,\&quot;topic_count\&quot;:184,\&quot;post_count\&quot;:605,\&quot;position\&quot;:21,\&quot;description\&quot;:\&quot;The meta category is for all posts about the forum itself.\&quot;,\&quot;description_text\&quot;:\&quot;The meta category is for all posts about the forum itself.\&quot;,\&quot;description_excerpt\&quot;:\&quot;The meta category is for all posts about the forum itself.\&quot;,\&quot;topic_url\&quot;:\&quot;/t/meta-topics/12\&quot;,\&quot;read_restricted\&quot;:false,\&quot;permission\&quot;:null,\&quot;notification_level\&quot;:1,\&quot;topic_template\&quot;:null,\&quot;has_children\&quot;:false,\&quot;sort_order\&quot;:null,\&quot;sort_ascending\&quot;:null,\&quot;show_subcategory_list\&quot;:false,\&quot;num_featured_topics\&quot;:3,\&quot;default_view\&quot;:null,\&quot;subcategory_list_style\&quot;:\&quot;rows_with_featured_topics\&quot;,\&quot;default_top_period\&quot;:\&quot;all\&quot;,\&quot;default_list_filter\&quot;:\&quot;all\&quot;,\&quot;minimum_required_tags\&quot;:0,\&quot;navigate_to_first_post_after_read\&quot;:false,\&quot;custom_fields\&quot;:{\&quot;enable_unassigned_filter\&quot;:null,\&quot;enable_accepted_answers\&quot;:null},\&quot;allowed_tags\&quot;:[],\&quot;allowed_tag_groups\&quot;:[],\&quot;allow_global_tags\&quot;:false,\&quot;min_tags_from_required_group\&quot;:1,\&quot;required_tag_group_name\&quot;:null,\&quot;read_only_banner\&quot;:null,\&quot;uploaded_logo\&quot;:null,\&quot;uploaded_background\&quot;:null,\&quot;can_edit\&quot;:false},{\&quot;id\&quot;:25,\&quot;name\&quot;:\&quot;Translation\&quot;,\&quot;color\&quot;:\&quot;F7941D\&quot;,\&quot;text_color\&quot;:\&quot;000000\&quot;,\&quot;slug\&quot;:\&quot;translation\&quot;,\&quot;topic_count\&quot;:11,\&quot;post_count\&quot;:72,\&quot;position\&quot;:22,\&quot;description\&quot;:\&quot;This is the category to use when discussing translating the Ionic docs or any official Ionic related content.\&quot;,\&quot;description_text\&quot;:\&quot;This is the category to use when discussing translating the Ionic docs or any official Ionic related content.\&quot;,\&quot;description_excerpt\&quot;:\&quot;This is the category to use when discussing translating the Ionic docs or any official Ionic related content.\&quot;,\&quot;topic_url\&quot;:\&quot;/t/about-the-translation-category/166040\&quot;,\&quot;read_restricted\&quot;:false,\&quot;permission\&quot;:null,\&quot;notification_level\&quot;:1,\&quot;topic_template\&quot;:null,\&quot;has_children\&quot;:false,\&quot;sort_order\&quot;:null,\&quot;sort_ascending\&quot;:null,\&quot;show_subcategory_list\&quot;:false,\&quot;num_featured_topics\&quot;:3,\&quot;default_view\&quot;:null,\&quot;subcategory_list_style\&quot;:\&quot;rows_with_featured_topics\&quot;,\&quot;default_top_period\&quot;:\&quot;all\&quot;,\&quot;default_list_filter\&quot;:\&quot;all\&quot;,\&quot;minimum_required_tags\&quot;:0,\&quot;navigate_to_first_post_after_read\&quot;:false,\&quot;custom_fields\&quot;:{\&quot;enable_unassigned_filter\&quot;:null,\&quot;enable_accepted_answers\&quot;:null},\&quot;allowed_tags\&quot;:[],\&quot;allowed_tag_groups\&quot;:[],\&quot;allow_global_tags\&quot;:false,\&quot;min_tags_from_required_group\&quot;:1,\&quot;required_tag_group_name\&quot;:null,\&quot;read_only_banner\&quot;:null,\&quot;uploaded_logo\&quot;:null,\&quot;uploaded_background\&quot;:null,\&quot;can_edit\&quot;:false},{\&quot;id\&quot;:30,\&quot;name\&quot;:\&quot;Blog\&quot;,\&quot;color\&quot;:\&quot;0088CC\&quot;,\&quot;text_color\&quot;:\&quot;FFFFFF\&quot;,\&quot;slug\&quot;:\&quot;blog\&quot;,\&quot;topic_count\&quot;:10,\&quot;post_count\&quot;:41,\&quot;position\&quot;:23,\&quot;description\&quot;:null,\&quot;description_text\&quot;:null,\&quot;description_excerpt\&quot;:null,\&quot;topic_url\&quot;:\&quot;/t/about-the-blog-category/199391\&quot;,\&quot;read_restricted\&quot;:false,\&quot;permission\&quot;:null,\&quot;notification_level\&quot;:1,\&quot;topic_template\&quot;:\&quot;\&quot;,\&quot;has_children\&quot;:false,\&quot;sort_order\&quot;:\&quot;\&quot;,\&quot;sort_ascending\&quot;:null,\&quot;show_subcategory_list\&quot;:false,\&quot;num_featured_topics\&quot;:3,\&quot;default_view\&quot;:\&quot;\&quot;,\&quot;subcategory_list_style\&quot;:\&quot;rows_with_featured_topics\&quot;,\&quot;default_top_period\&quot;:\&quot;all\&quot;,\&quot;default_list_filter\&quot;:\&quot;all\&quot;,\&quot;minimum_required_tags\&quot;:0,\&quot;navigate_to_first_post_after_read\&quot;:false,\&quot;custom_fields\&quot;:{\&quot;enable_unassigned_filter\&quot;:null,\&quot;enable_accepted_answers\&quot;:null},\&quot;allowed_tags\&quot;:[],\&quot;allowed_tag_groups\&quot;:[],\&quot;allow_global_tags\&quot;:false,\&quot;min_tags_from_required_group\&quot;:1,\&quot;required_tag_group_name\&quot;:null,\&quot;read_only_banner\&quot;:\&quot;\&quot;,\&quot;uploaded_logo\&quot;:null,\&quot;uploaded_background\&quot;:null,\&quot;can_edit\&quot;:false}],\&quot;hosting_tier\&quot;:\&quot;enterprise\&quot;,\&quot;notification_email\&quot;:null,\&quot;archetypes\&quot;:[{\&quot;id\&quot;:\&quot;regular\&quot;,\&quot;name\&quot;:\&quot;Regular Topic\&quot;,\&quot;options\&quot;:[]},{\&quot;id\&quot;:\&quot;banner\&quot;,\&quot;name\&quot;:\&quot;Banner Topic\&quot;,\&quot;options\&quot;:[]}],\&quot;user_fields\&quot;:[],\&quot;auth_providers\&quot;:[]}&quot;,&quot;siteSettings&quot;:&quot;{\&quot;default_locale\&quot;:\&quot;en\&quot;,\&quot;title\&quot;:\&quot;Ionic Forum\&quot;,\&quot;short_site_description\&quot;:\&quot;Build cross-platform mobile apps with HTML, CSS, and JavaScript\&quot;,\&quot;exclude_rel_nofollow_domains\&quot;:\&quot;ionicframework.com|stenciljs.com|capacitor.ionicframework.com|blog.ionicframework.com|ionic.io|capacitorjs.com\&quot;,\&quot;logo\&quot;:\&quot;//discourse-cloud-file-uploads.s3.dualstack.us-west-2.amazonaws.com/ionicframework/original/3X/3/b/3bcceade60c32df77565a17af301b363f2a418ae.png\&quot;,\&quot;logo_small\&quot;:\&quot;//discourse-cloud-file-uploads.s3.dualstack.us-west-2.amazonaws.com/ionicframework/original/3X/f/7/f710802ea63a96972012e1f7c0274f81aa89ab27.png\&quot;,\&quot;digest_logo\&quot;:\&quot;//discourse-cloud-file-uploads.s3.dualstack.us-west-2.amazonaws.com/ionicframework/original/3X/3/1/3147b922b52d16b3aa73346a1d2cbd1cce5e00b9.png\&quot;,\&quot;mobile_logo\&quot;:\&quot;//discourse-cloud-file-uploads.s3.dualstack.us-west-2.amazonaws.com/ionicframework/original/3X/3/1/3147b922b52d16b3aa73346a1d2cbd1cce5e00b9.png\&quot;,\&quot;logo_dark\&quot;:\&quot;//discourse-cloud-file-uploads.s3.dualstack.us-west-2.amazonaws.com/ionicframework/original/3X/5/6/56d27588427047d53fb15a375f04b30c8af3ca93.png\&quot;,\&quot;logo_small_dark\&quot;:\&quot;//discourse-cloud-file-uploads.s3.dualstack.us-west-2.amazonaws.com/ionicframework/original/3X/4/6/467afba2387d7da7a21eec06bd65134552e61265.png\&quot;,\&quot;mobile_logo_dark\&quot;:\&quot;//discourse-cloud-file-uploads.s3.dualstack.us-west-2.amazonaws.com/ionicframework/original/3X/3/9/393ab9c04be461c315d77c58b8a31dba206fb9a5.png\&quot;,\&quot;large_icon\&quot;:\&quot;//discourse-cloud-file-uploads.s3.dualstack.us-west-2.amazonaws.com/ionicframework/original/3X/6/1/611c901fd53d1af605cd282e83292c2edf752d8d.png\&quot;,\&quot;favicon\&quot;:\&quot;//discourse-cloud-file-uploads.s3.dualstack.us-west-2.amazonaws.com/ionicframework/original/3X/a/4/a4bdd686c6074c2dfe3c9d529350a82781516b3e.png\&quot;,\&quot;apple_touch_icon\&quot;:\&quot;//discourse-cloud-file-uploads.s3.dualstack.us-west-2.amazonaws.com/ionicframework/original/3X/6/1/611c901fd53d1af605cd282e83292c2edf752d8d.png\&quot;,\&quot;display_local_time_in_user_card\&quot;:false,\&quot;allow_user_locale\&quot;:true,\&quot;set_locale_from_accept_language_header\&quot;:false,\&quot;support_mixed_text_direction\&quot;:true,\&quot;suggested_topics\&quot;:5,\&quot;ga_universal_tracking_code\&quot;:\&quot;\&quot;,\&quot;ga_universal_domain_name\&quot;:\&quot;auto\&quot;,\&quot;gtm_container_id\&quot;:\&quot;GTM-TKMGCBC\&quot;,\&quot;top_menu\&quot;:\&quot;categories|latest|new|unread|top\&quot;,\&quot;post_menu\&quot;:\&quot;read|like|share|flag|edit|bookmark|delete|admin|reply\&quot;,\&quot;post_menu_hidden_items\&quot;:\&quot;flag|bookmark|edit|delete|admin\&quot;,\&quot;share_links\&quot;:\&quot;twitter|facebook|email\&quot;,\&quot;share_quote_visibility\&quot;:\&quot;anonymous\&quot;,\&quot;share_quote_buttons\&quot;:\&quot;twitter|email\&quot;,\&quot;desktop_category_page_style\&quot;:\&quot;categories_and_latest_topics\&quot;,\&quot;category_colors\&quot;:\&quot;BF1E2E|F1592A|F7941D|9EB83B|3AB54A|12A89D|25AAE2|0E76BD|652D90|92278F|ED207B|8C6238|231F20|808281|B3B5B4|E45735\&quot;,\&quot;category_style\&quot;:\&quot;bullet\&quot;,\&quot;max_category_nesting\&quot;:2,\&quot;enable_mobile_theme\&quot;:true,\&quot;enable_experimental_image_uploader\&quot;:false,\&quot;enable_experimental_composer_uploader\&quot;:false,\&quot;enable_direct_s3_uploads\&quot;:false,\&quot;enable_upload_debug_mode\&quot;:false,\&quot;default_dark_mode_color_scheme_id\&quot;:-1,\&quot;relative_date_duration\&quot;:30,\&quot;fixed_category_positions\&quot;:true,\&quot;fixed_category_positions_on_create\&quot;:false,\&quot;enable_badges\&quot;:true,\&quot;enable_badge_sql\&quot;:false,\&quot;max_favorite_badges\&quot;:2,\&quot;enable_whispers\&quot;:false,\&quot;enable_bookmarks_with_reminders\&quot;:true,\&quot;push_notifications_prompt\&quot;:true,\&quot;vapid_public_key_bytes\&quot;:\&quot;4|234|219|239|22|38|129|231|80|88|103|60|157|250|87|3|149|181|186|105|204|174|136|149|106|21|142|177|31|68|191|86|218|98|39|182|45|186|160|231|60|202|152|55|77|166|226|2|215|97|103|85|252|89|87|204|176|188|41|196|122|135|172|208|121\&quot;,\&quot;invite_only\&quot;:false,\&quot;login_required\&quot;:false,\&quot;must_approve_users\&quot;:false,\&quot;enable_local_logins\&quot;:true,\&quot;enable_local_logins_via_email\&quot;:true,\&quot;allow_new_registrations\&quot;:true,\&quot;enable_signup_cta\&quot;:true,\&quot;facebook_app_id\&quot;:\&quot;\&quot;,\&quot;auth_skip_create_confirm\&quot;:false,\&quot;enable_discourse_connect\&quot;:true,\&quot;auth_overrides_email\&quot;:false,\&quot;discourse_connect_overrides_avatar\&quot;:false,\&quot;min_username_length\&quot;:3,\&quot;max_username_length\&quot;:20,\&quot;unicode_usernames\&quot;:false,\&quot;min_password_length\&quot;:10,\&quot;min_admin_password_length\&quot;:15,\&quot;email_editable\&quot;:true,\&quot;logout_redirect\&quot;:\&quot;\&quot;,\&quot;full_name_required\&quot;:false,\&quot;enable_names\&quot;:true,\&quot;invites_per_page\&quot;:40,\&quot;delete_user_max_post_age\&quot;:60,\&quot;delete_all_posts_max\&quot;:60,\&quot;prioritize_username_in_ux\&quot;:true,\&quot;enable_user_directory\&quot;:true,\&quot;allow_anonymous_posting\&quot;:false,\&quot;anonymous_posting_min_trust_level\&quot;:1,\&quot;allow_users_to_hide_profile\&quot;:true,\&quot;hide_user_profiles_from_public\&quot;:false,\&quot;allow_featured_topic_on_user_profiles\&quot;:true,\&quot;hide_suspension_reasons\&quot;:false,\&quot;ignored_users_count_message_threshold\&quot;:5,\&quot;ignored_users_message_gap_days\&quot;:365,\&quot;user_selected_primary_groups\&quot;:false,\&quot;gravatar_name\&quot;:\&quot;Gravatar\&quot;,\&quot;gravatar_base_url\&quot;:\&quot;www.gravatar.com\&quot;,\&quot;gravatar_login_url\&quot;:\&quot;/emails\&quot;,\&quot;enable_group_directory\&quot;:true,\&quot;enable_category_group_moderation\&quot;:false,\&quot;min_post_length\&quot;:20,\&quot;min_first_post_length\&quot;:20,\&quot;min_personal_message_post_length\&quot;:10,\&quot;max_post_length\&quot;:32000,\&quot;topic_featured_link_enabled\&quot;:true,\&quot;min_topic_views_for_delete_confirm\&quot;:5000,\&quot;min_topic_title_length\&quot;:10,\&quot;max_topic_title_length\&quot;:255,\&quot;enable_filtered_replies_view\&quot;:false,\&quot;min_personal_message_title_length\&quot;:2,\&quot;allow_uncategorized_topics\&quot;:false,\&quot;min_title_similar_length\&quot;:10,\&quot;enable_personal_messages\&quot;:true,\&quot;edit_history_visible_to_public\&quot;:true,\&quot;delete_removed_posts_after\&quot;:24,\&quot;traditional_markdown_linebreaks\&quot;:false,\&quot;enable_markdown_typographer\&quot;:true,\&quot;enable_markdown_linkify\&quot;:true,\&quot;markdown_linkify_tlds\&quot;:\&quot;com|net|org|io|onion|co|tv|ru|cn|us|uk|me|de|fr|fi|gov\&quot;,\&quot;markdown_typographer_quotation_marks\&quot;:\&quot;“|”|‘|’\&quot;,\&quot;enable_rich_text_paste\&quot;:true,\&quot;suppress_reply_directly_below\&quot;:true,\&quot;suppress_reply_directly_above\&quot;:true,\&quot;max_reply_history\&quot;:1,\&quot;enable_mentions\&quot;:true,\&quot;newuser_max_embedded_media\&quot;:3,\&quot;newuser_max_attachments\&quot;:3,\&quot;show_pinned_excerpt_mobile\&quot;:true,\&quot;show_pinned_excerpt_desktop\&quot;:true,\&quot;display_name_on_posts\&quot;:false,\&quot;show_time_gap_days\&quot;:7,\&quot;short_progress_text_threshold\&quot;:10000,\&quot;default_code_lang\&quot;:\&quot;auto\&quot;,\&quot;autohighlight_all_code\&quot;:false,\&quot;highlighted_languages\&quot;:\&quot;apache|bash|cs|cpp|css|coffeescript|diff|xml|http|ini|json|java|javascript|makefile|markdown|nginx|objectivec|ruby|perl|php|python|sql|handlebars\&quot;,\&quot;show_copy_button_on_codeblocks\&quot;:false,\&quot;enable_emoji\&quot;:true,\&quot;enable_emoji_shortcuts\&quot;:true,\&quot;emoji_set\&quot;:\&quot;twitter\&quot;,\&quot;emoji_autocomplete_min_chars\&quot;:0,\&quot;enable_inline_emoji_translation\&quot;:false,\&quot;code_formatting_style\&quot;:\&quot;code-fences\&quot;,\&quot;allowed_href_schemes\&quot;:\&quot;\&quot;,\&quot;watched_words_regular_expressions\&quot;:false,\&quot;enable_advanced_editor_preview_sync\&quot;:false,\&quot;enable_diffhtml_preview\&quot;:false,\&quot;enable_fast_edit\&quot;:true,\&quot;old_post_notice_days\&quot;:14,\&quot;blur_tl0_flagged_posts_media\&quot;:true,\&quot;email_time_window_mins\&quot;:10,\&quot;disable_digest_emails\&quot;:false,\&quot;email_in\&quot;:false,\&quot;enable_imap\&quot;:false,\&quot;enable_smtp\&quot;:false,\&quot;disable_emails\&quot;:\&quot;no\&quot;,\&quot;bounce_score_threshold\&quot;:4,\&quot;enable_secondary_emails\&quot;:true,\&quot;max_image_size_kb\&quot;:4096,\&quot;max_attachment_size_kb\&quot;:4096,\&quot;authorized_extensions\&quot;:\&quot;jpg|jpeg|png|gif|heic|heif|webp\&quot;,\&quot;authorized_extensions_for_staff\&quot;:\&quot;\&quot;,\&quot;max_image_width\&quot;:690,\&quot;max_image_height\&quot;:500,\&quot;prevent_anons_from_downloading_files\&quot;:false,\&quot;secure_media\&quot;:false,\&quot;enable_s3_uploads\&quot;:false,\&quot;allow_profile_backgrounds\&quot;:true,\&quot;allow_uploaded_avatars\&quot;:\&quot;0\&quot;,\&quot;default_avatars\&quot;:\&quot;\&quot;,\&quot;external_system_avatars_enabled\&quot;:true,\&quot;external_system_avatars_url\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/{first_letter}/{color}/{size}.png\&quot;,\&quot;external_emoji_url\&quot;:\&quot;https://emoji.discourse-cdn.com\&quot;,\&quot;selectable_avatars_enabled\&quot;:false,\&quot;selectable_avatars\&quot;:\&quot;\&quot;,\&quot;allow_staff_to_upload_any_file_in_pm\&quot;:true,\&quot;simultaneous_uploads\&quot;:5,\&quot;composer_media_optimization_image_enabled\&quot;:true,\&quot;composer_media_optimization_image_bytes_optimization_threshold\&quot;:524288,\&quot;composer_media_optimization_image_resize_dimensions_threshold\&quot;:1920,\&quot;composer_media_optimization_image_resize_width_target\&quot;:1920,\&quot;composer_media_optimization_image_resize_pre_multiply\&quot;:false,\&quot;composer_media_optimization_image_resize_linear_rgb\&quot;:false,\&quot;composer_media_optimization_image_encode_quality\&quot;:75,\&quot;composer_media_optimization_debug_mode\&quot;:false,\&quot;min_trust_level_to_allow_profile_background\&quot;:0,\&quot;min_trust_level_to_allow_user_card_background\&quot;:0,\&quot;min_trust_level_to_allow_ignore\&quot;:2,\&quot;tl1_requires_read_posts\&quot;:30,\&quot;tl3_links_no_follow\&quot;:false,\&quot;enforce_second_factor\&quot;:\&quot;no\&quot;,\&quot;moderators_change_post_ownership\&quot;:false,\&quot;moderators_view_emails\&quot;:false,\&quot;use_admin_ip_allowlist\&quot;:false,\&quot;allowed_iframes\&quot;:\&quot;https://www.google.com/maps/embed?|https://www.openstreetmap.org/export/embed.html?|https://calendar.google.com/calendar/embed?|https://codepen.io/|https://forum.ionicframework.com/discobot/certificate.svg\&quot;,\&quot;max_oneboxes_per_post\&quot;:50,\&quot;reviewable_claiming\&quot;:\&quot;disabled\&quot;,\&quot;reviewable_default_topics\&quot;:false,\&quot;reviewable_default_visibility\&quot;:\&quot;low\&quot;,\&quot;alert_admins_if_errors_per_minute\&quot;:0,\&quot;alert_admins_if_errors_per_hour\&quot;:0,\&quot;max_prints_per_hour_per_user\&quot;:5,\&quot;invite_link_max_redemptions_limit\&quot;:5000,\&quot;invite_link_max_redemptions_limit_users\&quot;:10,\&quot;enable_long_polling\&quot;:true,\&quot;enable_chunked_encoding\&quot;:true,\&quot;long_polling_base_url\&quot;:\&quot;/\&quot;,\&quot;background_polling_interval\&quot;:60000,\&quot;polling_interval\&quot;:3000,\&quot;anon_polling_interval\&quot;:30000,\&quot;flush_timings_secs\&quot;:60,\&quot;verbose_localization\&quot;:false,\&quot;max_new_topics\&quot;:500,\&quot;enable_safe_mode\&quot;:true,\&quot;tos_url\&quot;:\&quot;https://ionicframework.com/tos\&quot;,\&quot;privacy_policy_url\&quot;:\&quot;https://ionicframework.com/privacy\&quot;,\&quot;faq_url\&quot;:\&quot;\&quot;,\&quot;enable_backups\&quot;:true,\&quot;backup_location\&quot;:\&quot;s3\&quot;,\&quot;maximum_backups\&quot;:3,\&quot;use_pg_headlines_for_excerpt\&quot;:false,\&quot;min_search_term_length\&quot;:3,\&quot;log_search_queries\&quot;:true,\&quot;version_checks\&quot;:false,\&quot;suppress_uncategorized_badge\&quot;:true,\&quot;header_dropdown_category_count\&quot;:8,\&quot;slug_generation_method\&quot;:\&quot;ascii\&quot;,\&quot;summary_timeline_button\&quot;:false,\&quot;topic_views_heat_low\&quot;:1000,\&quot;topic_views_heat_medium\&quot;:2000,\&quot;topic_views_heat_high\&quot;:3600,\&quot;topic_post_like_heat_low\&quot;:0.5,\&quot;topic_post_like_heat_medium\&quot;:1.0,\&quot;topic_post_like_heat_high\&quot;:2.0,\&quot;history_hours_low\&quot;:12,\&quot;history_hours_medium\&quot;:24,\&quot;history_hours_high\&quot;:48,\&quot;cold_age_days_low\&quot;:14,\&quot;cold_age_days_medium\&quot;:90,\&quot;cold_age_days_high\&quot;:180,\&quot;global_notice\&quot;:\&quot;\&quot;,\&quot;show_create_topics_notice\&quot;:true,\&quot;bootstrap_mode_min_users\&quot;:50,\&quot;bootstrap_mode_enabled\&quot;:false,\&quot;automatically_unpin_topics\&quot;:true,\&quot;read_time_word_count\&quot;:500,\&quot;topic_page_title_includes_category\&quot;:true,\&quot;svg_icon_subset\&quot;:\&quot;\&quot;,\&quot;disable_mailing_list_mode\&quot;:false,\&quot;default_topics_automatic_unpin\&quot;:true,\&quot;mute_all_categories_by_default\&quot;:false,\&quot;tagging_enabled\&quot;:true,\&quot;tag_style\&quot;:\&quot;simple\&quot;,\&quot;max_tags_per_topic\&quot;:5,\&quot;max_tag_length\&quot;:20,\&quot;min_trust_level_to_tag_topics\&quot;:\&quot;0\&quot;,\&quot;max_tag_search_results\&quot;:5,\&quot;max_tags_in_filter_list\&quot;:30,\&quot;tags_sort_alphabetically\&quot;:false,\&quot;tags_listed_by_group\&quot;:false,\&quot;suppress_overlapping_tags_in_list\&quot;:false,\&quot;remove_muted_tags_from_latest\&quot;:\&quot;always\&quot;,\&quot;force_lowercase_tags\&quot;:true,\&quot;dashboard_hidden_reports\&quot;:\&quot;\&quot;,\&quot;dashboard_visible_tabs\&quot;:\&quot;moderation|security|reports\&quot;,\&quot;dashboard_general_tab_activity_metrics\&quot;:\&quot;page_view_total_reqs|visits|time_to_first_response|likes|flags|user_to_user_private_messages_with_replies\&quot;,\&quot;discourse_local_dates_email_format\&quot;:\&quot;YYYY-MM-DDTHH:mm:ss[Z]\&quot;,\&quot;discourse_local_dates_enabled\&quot;:true,\&quot;discourse_local_dates_default_formats\&quot;:\&quot;LLL|LTS|LL|LLLL\&quot;,\&quot;discourse_local_dates_default_timezones\&quot;:\&quot;Europe/Paris|America/Los_Angeles\&quot;,\&quot;discourse_narrative_bot_enabled\&quot;:true,\&quot;poll_enabled\&quot;:true,\&quot;poll_maximum_options\&quot;:20,\&quot;poll_minimum_trust_level_to_create\&quot;:1,\&quot;poll_groupable_user_fields\&quot;:\&quot;\&quot;,\&quot;poll_export_data_explorer_query_id\&quot;:-16,\&quot;presence_enabled\&quot;:true,\&quot;presence_max_users_shown\&quot;:5,\&quot;details_enabled\&quot;:true,\&quot;solved_enabled\&quot;:true,\&quot;allow_solved_on_all_topics\&quot;:true,\&quot;accept_all_solutions_trust_level\&quot;:4,\&quot;empty_box_on_unsolved\&quot;:false,\&quot;show_filter_by_solved_status\&quot;:true,\&quot;data_explorer_enabled\&quot;:false,\&quot;checklist_enabled\&quot;:true,\&quot;user_notes_enabled\&quot;:true,\&quot;spoiler_enabled\&quot;:true,\&quot;docs_enabled\&quot;:false,\&quot;docs_categories\&quot;:\&quot;\&quot;,\&quot;docs_tags\&quot;:\&quot;\&quot;,\&quot;docs_add_solved_filter\&quot;:false,\&quot;docs_add_to_top_menu\&quot;:false,\&quot;discourse_math_enabled\&quot;:false,\&quot;discourse_math_provider\&quot;:\&quot;mathjax\&quot;,\&quot;discourse_math_zoom_on_hover\&quot;:false,\&quot;discourse_math_enable_accessibility\&quot;:false,\&quot;discourse_math_enable_asciimath\&quot;:false,\&quot;affiliate_enabled\&quot;:false,\&quot;affiliate_amazon_ca\&quot;:\&quot;\&quot;,\&quot;affiliate_amazon_cn\&quot;:\&quot;\&quot;,\&quot;affiliate_amazon_co_jp\&quot;:\&quot;\&quot;,\&quot;affiliate_amazon_co_uk\&quot;:\&quot;\&quot;,\&quot;affiliate_amazon_com\&quot;:\&quot;\&quot;,\&quot;affiliate_amazon_com_au\&quot;:\&quot;\&quot;,\&quot;affiliate_amazon_com_br\&quot;:\&quot;\&quot;,\&quot;affiliate_amazon_com_mx\&quot;:\&quot;\&quot;,\&quot;affiliate_amazon_de\&quot;:\&quot;\&quot;,\&quot;affiliate_amazon_es\&quot;:\&quot;\&quot;,\&quot;affiliate_amazon_fr\&quot;:\&quot;\&quot;,\&quot;affiliate_amazon_in\&quot;:\&quot;\&quot;,\&quot;affiliate_amazon_it\&quot;:\&quot;\&quot;,\&quot;affiliate_amazon_nl\&quot;:\&quot;\&quot;,\&quot;affiliate_ldlc_com\&quot;:\&quot;\&quot;,\&quot;calendar_enabled\&quot;:false,\&quot;holiday_calendar_topic_id\&quot;:\&quot;\&quot;,\&quot;all_day_event_start_time\&quot;:\&quot;\&quot;,\&quot;all_day_event_end_time\&quot;:\&quot;\&quot;,\&quot;calendar_categories\&quot;:\&quot;\&quot;,\&quot;calendar_categories_outlet\&quot;:\&quot;discovery-list-container-top\&quot;,\&quot;working_days\&quot;:\&quot;Monday|Tuesday|Wednesday|Thursday|Friday\&quot;,\&quot;working_day_start_hour\&quot;:8,\&quot;working_day_end_hour\&quot;:17,\&quot;close_to_working_day_hours_extension\&quot;:2,\&quot;discourse_post_event_enabled\&quot;:false,\&quot;discourse_post_event_allowed_on_groups\&quot;:\&quot;\&quot;,\&quot;display_post_event_date_on_topic_title\&quot;:true,\&quot;discourse_post_event_allowed_custom_fields\&quot;:\&quot;\&quot;,\&quot;canned_replies_enabled\&quot;:true,\&quot;canned_replies_everyone_enabled\&quot;:false,\&quot;canned_replies_everyone_can_edit\&quot;:false,\&quot;cakeday_enabled\&quot;:true,\&quot;cakeday_emoji\&quot;:\&quot;cake\&quot;,\&quot;cakeday_birthday_enabled\&quot;:true,\&quot;cakeday_birthday_emoji\&quot;:\&quot;birthday\&quot;,\&quot;voting_enabled\&quot;:true,\&quot;voting_show_who_voted\&quot;:true,\&quot;voting_show_votes_on_profile\&quot;:true,\&quot;yearly_review_enabled\&quot;:false,\&quot;assign_enabled\&quot;:false,\&quot;assigns_public\&quot;:false,\&quot;assigns_user_url_path\&quot;:\&quot;/u/{username}/activity/assigned\&quot;,\&quot;remind_assigns_frequency\&quot;:0,\&quot;max_assigned_topics\&quot;:10,\&quot;assign_allowed_on_groups\&quot;:\&quot;3\&quot;,\&quot;available_locales\&quot;:\&quot;[{\\\&quot;name\\\&quot;:\\\&quot;اللغة العربية\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;ar\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;беларуская мова\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;be\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;български език\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;bg\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;bosanski jezik\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;bs_BA\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;català\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;ca\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;čeština\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;cs\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;dansk\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;da\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;Deutsch\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;de\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;ελληνικά\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;el\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;English (US)\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;en\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;English (UK)\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;en_GB\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;Español\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;es\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;eesti\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;et\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;فارسی\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;fa_IR\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;suomi\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;fi\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;Français\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;fr\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;galego\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;gl\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;עברית\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;he\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;magyar\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;hu\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;Հայերեն\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;hy\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;Indonesian\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;id\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;Italiano\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;it\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;日本語\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;ja\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;한국어\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;ko\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;lietuvių kalba\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;lt\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;latviešu valoda\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;lv\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;Norsk bokmål\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;nb_NO\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;Nederlands\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;nl\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;polski\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;pl_PL\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;Português\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;pt\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;Português (BR)\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;pt_BR\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;limba română\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;ro\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;Русский\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;ru\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;slovenčina\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;sk\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;slovenščina\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;sl\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;Shqip\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;sq\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;српски језик\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;sr\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;svenska\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;sv\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;Kiswahili\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;sw\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;తెలుగు\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;te\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;ไทย\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;th\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;Türkçe\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;tr_TR\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;українська мова\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;uk\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;اردو\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;ur\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;Việt Nam\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;vi\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;简体中文\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;zh_CN\\\&quot;},{\\\&quot;name\\\&quot;:\\\&quot;繁體中文\\\&quot;,\\\&quot;value\\\&quot;:\\\&quot;zh_TW\\\&quot;}]\&quot;,\&quot;require_invite_code\&quot;:false,\&quot;site_logo_url\&quot;:\&quot;https://aws1.discourse-cdn.com/ionicframework/original/3X/3/b/3bcceade60c32df77565a17af301b363f2a418ae.png\&quot;,\&quot;site_logo_small_url\&quot;:\&quot;https://aws1.discourse-cdn.com/ionicframework/original/3X/f/7/f710802ea63a96972012e1f7c0274f81aa89ab27.png\&quot;,\&quot;site_mobile_logo_url\&quot;:\&quot;https://aws1.discourse-cdn.com/ionicframework/original/3X/3/1/3147b922b52d16b3aa73346a1d2cbd1cce5e00b9.png\&quot;,\&quot;site_favicon_url\&quot;:\&quot;https://aws1.discourse-cdn.com/ionicframework/optimized/3X/a/4/a4bdd686c6074c2dfe3c9d529350a82781516b3e_2_32x32.png\&quot;,\&quot;site_logo_dark_url\&quot;:\&quot;https://aws1.discourse-cdn.com/ionicframework/original/3X/5/6/56d27588427047d53fb15a375f04b30c8af3ca93.png\&quot;,\&quot;site_logo_small_dark_url\&quot;:\&quot;https://aws1.discourse-cdn.com/ionicframework/original/3X/4/6/467afba2387d7da7a21eec06bd65134552e61265.png\&quot;,\&quot;site_mobile_logo_dark_url\&quot;:\&quot;https://aws1.discourse-cdn.com/ionicframework/original/3X/3/9/393ab9c04be461c315d77c58b8a31dba206fb9a5.png\&quot;}&quot;,&quot;customHTML&quot;:&quot;{\&quot;top\&quot;:\&quot;\&quot;,\&quot;footer\&quot;:\&quot;\&quot;}&quot;,&quot;banner&quot;:&quot;{}&quot;,&quot;customEmoji&quot;:&quot;[]&quot;,&quot;isReadOnly&quot;:&quot;false&quot;,&quot;activatedThemes&quot;:&quot;{\&quot;1\&quot;:\&quot;Ionic\&quot;,\&quot;3\&quot;:\&quot;Default\&quot;}&quot;,&quot;topic_177814&quot;:&quot;{\&quot;post_stream\&quot;:{\&quot;posts\&quot;:[{\&quot;id\&quot;:446326,\&quot;name\&quot;:\&quot;Swapnil P133\&quot;,\&quot;username\&quot;:\&quot;SwapnilP133\&quot;,\&quot;avatar_template\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/s/a9adbd/{size}.png\&quot;,\&quot;created_at\&quot;:\&quot;2019-11-18T06:49:00.883Z\&quot;,\&quot;cooked\&quot;:\&quot;\\u003cp\\u003eI recently came across Capacitor and i tried it, I find it better than Cordova.\\u003cbr\\u003e\\nBut the only thing is I could not find a command to generate .apk or archive.\\u003cbr\\u003e\\nIn Cordova, I was able to generate .apk without even opening Android Studio.\\u003cbr\\u003e\\nI am looking for capacitor equivalent commands for \\u003ccode\\u003eionic cordova build android\\u003c/code\\u003e and \\u003ccode\\u003eionic cordova build ios\\u003c/code\\u003e\\u003c/p\\u003e\&quot;,\&quot;post_number\&quot;:1,\&quot;post_type\&quot;:1,\&quot;updated_at\&quot;:\&quot;2020-11-10T17:53:24.923Z\&quot;,\&quot;reply_count\&quot;:0,\&quot;reply_to_post_number\&quot;:null,\&quot;quote_count\&quot;:0,\&quot;incoming_link_count\&quot;:37192,\&quot;reads\&quot;:544,\&quot;readers_count\&quot;:543,\&quot;score\&quot;:185663.8,\&quot;yours\&quot;:false,\&quot;topic_id\&quot;:177814,\&quot;topic_slug\&quot;:\&quot;how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project\&quot;,\&quot;display_username\&quot;:\&quot;Swapnil P133\&quot;,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;version\&quot;:2,\&quot;can_edit\&quot;:false,\&quot;can_delete\&quot;:false,\&quot;can_recover\&quot;:false,\&quot;can_wiki\&quot;:false,\&quot;read\&quot;:true,\&quot;user_title\&quot;:null,\&quot;bookmarked\&quot;:false,\&quot;actions_summary\&quot;:[],\&quot;moderator\&quot;:false,\&quot;admin\&quot;:false,\&quot;staff\&quot;:false,\&quot;user_id\&quot;:148822,\&quot;hidden\&quot;:false,\&quot;trust_level\&quot;:1,\&quot;deleted_at\&quot;:null,\&quot;user_deleted\&quot;:false,\&quot;edit_reason\&quot;:null,\&quot;can_view_edit_history\&quot;:true,\&quot;wiki\&quot;:false,\&quot;calendar_details\&quot;:[],\&quot;can_accept_answer\&quot;:false,\&quot;can_unaccept_answer\&quot;:false,\&quot;accepted_answer\&quot;:false,\&quot;can_vote\&quot;:false},{\&quot;id\&quot;:446406,\&quot;name\&quot;:\&quot;Terranmarine\&quot;,\&quot;username\&quot;:\&quot;terranmarine\&quot;,\&quot;avatar_template\&quot;:\&quot;/user_avatar/forum.ionicframework.com/terranmarine/{size}/125840_2.png\&quot;,\&quot;created_at\&quot;:\&quot;2019-11-18T14:39:17.932Z\&quot;,\&quot;cooked\&quot;:\&quot;\\u003cp\\u003eHello,\\u003c/p\\u003e\\n\\u003cp\\u003eGive this a try:\\u003cbr\\u003e\\n\\u003ccode\\u003e    \\\&quot;ios\\\&quot;: \\\&quot;sudo ionic build \\u0026amp;\\u0026amp; npx cap sync ios \\u0026amp;\\u0026amp; npx cap open ios\\\&quot;,     \\\&quot;android\\\&quot;: \\\&quot;sudo ionic build \\u0026amp;\\u0026amp; npx cap sync android \\u0026amp;\\u0026amp; npx cap open android\\\&quot;,\\u003c/code\\u003e\\u003c/p\\u003e\\n\\u003cp\\u003eYou can add there to your package json and when you want a new build just go \\u003ccode\\u003enpm run [platform]\\u003c/code\\u003e. You can also try running it without \\u003ccode\\u003esudo\\u003c/code\\u003e\\u003cbr\\u003e\\nAlex.\\u003c/p\\u003e\&quot;,\&quot;post_number\&quot;:2,\&quot;post_type\&quot;:1,\&quot;updated_at\&quot;:\&quot;2019-11-18T14:39:50.281Z\&quot;,\&quot;reply_count\&quot;:0,\&quot;reply_to_post_number\&quot;:null,\&quot;quote_count\&quot;:0,\&quot;incoming_link_count\&quot;:291,\&quot;reads\&quot;:543,\&quot;readers_count\&quot;:542,\&quot;score\&quot;:1563.6,\&quot;yours\&quot;:false,\&quot;topic_id\&quot;:177814,\&quot;topic_slug\&quot;:\&quot;how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project\&quot;,\&quot;display_username\&quot;:\&quot;Terranmarine\&quot;,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;version\&quot;:1,\&quot;can_edit\&quot;:false,\&quot;can_delete\&quot;:false,\&quot;can_recover\&quot;:false,\&quot;can_wiki\&quot;:false,\&quot;read\&quot;:true,\&quot;user_title\&quot;:null,\&quot;bookmarked\&quot;:false,\&quot;actions_summary\&quot;:[],\&quot;moderator\&quot;:false,\&quot;admin\&quot;:false,\&quot;staff\&quot;:false,\&quot;user_id\&quot;:151930,\&quot;hidden\&quot;:false,\&quot;trust_level\&quot;:2,\&quot;deleted_at\&quot;:null,\&quot;user_deleted\&quot;:false,\&quot;edit_reason\&quot;:null,\&quot;can_view_edit_history\&quot;:true,\&quot;wiki\&quot;:false,\&quot;can_accept_answer\&quot;:false,\&quot;can_unaccept_answer\&quot;:false,\&quot;accepted_answer\&quot;:false},{\&quot;id\&quot;:446439,\&quot;name\&quot;:\&quot;Mcroni\&quot;,\&quot;username\&quot;:\&quot;mcroni\&quot;,\&quot;avatar_template\&quot;:\&quot;/user_avatar/forum.ionicframework.com/mcroni/{size}/129308_2.png\&quot;,\&quot;created_at\&quot;:\&quot;2019-11-18T17:35:54.744Z\&quot;,\&quot;cooked\&quot;:\&quot;\\u003cp\\u003eHey,  type \\u003ccode\\u003enpx cap open android\\u003c/code\\u003e, this will open the android studio automatically. Wait till the gradle downloads successful and click on the play button (that’s if you have an android device connected to the pc) else click on \\u003ccode\\u003eBuild -- \\u0026gt;Build Bundle /Apk\\u003c/code\\u003e and you are good to go\\u003c/p\\u003e\&quot;,\&quot;post_number\&quot;:3,\&quot;post_type\&quot;:1,\&quot;updated_at\&quot;:\&quot;2019-11-18T17:35:54.744Z\&quot;,\&quot;reply_count\&quot;:1,\&quot;reply_to_post_number\&quot;:null,\&quot;quote_count\&quot;:0,\&quot;incoming_link_count\&quot;:112,\&quot;reads\&quot;:529,\&quot;readers_count\&quot;:528,\&quot;score\&quot;:685.8,\&quot;yours\&quot;:false,\&quot;topic_id\&quot;:177814,\&quot;topic_slug\&quot;:\&quot;how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project\&quot;,\&quot;display_username\&quot;:\&quot;Mcroni\&quot;,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;version\&quot;:1,\&quot;can_edit\&quot;:false,\&quot;can_delete\&quot;:false,\&quot;can_recover\&quot;:false,\&quot;can_wiki\&quot;:false,\&quot;read\&quot;:true,\&quot;user_title\&quot;:null,\&quot;bookmarked\&quot;:false,\&quot;actions_summary\&quot;:[{\&quot;id\&quot;:2,\&quot;count\&quot;:1}],\&quot;moderator\&quot;:false,\&quot;admin\&quot;:false,\&quot;staff\&quot;:false,\&quot;user_id\&quot;:158431,\&quot;hidden\&quot;:false,\&quot;trust_level\&quot;:1,\&quot;deleted_at\&quot;:null,\&quot;user_deleted\&quot;:false,\&quot;edit_reason\&quot;:null,\&quot;can_view_edit_history\&quot;:true,\&quot;wiki\&quot;:false,\&quot;can_accept_answer\&quot;:false,\&quot;can_unaccept_answer\&quot;:false,\&quot;accepted_answer\&quot;:false},{\&quot;id\&quot;:446722,\&quot;name\&quot;:\&quot;Roboter\&quot;,\&quot;username\&quot;:\&quot;roboter\&quot;,\&quot;avatar_template\&quot;:\&quot;/user_avatar/forum.ionicframework.com/roboter/{size}/129354_2.png\&quot;,\&quot;created_at\&quot;:\&quot;2019-11-20T11:13:52.693Z\&quot;,\&quot;cooked\&quot;:\&quot;\\u003cp\\u003eHey, did you read the question?\\u003c/p\\u003e\\n\\u003cblockquote\\u003e\\n\\u003cp\\u003ewithout using Android Studio\\u003c/p\\u003e\\n\\u003c/blockquote\\u003e\\n\\u003cp\\u003eLooking for same\\u003c/p\\u003e\&quot;,\&quot;post_number\&quot;:5,\&quot;post_type\&quot;:1,\&quot;updated_at\&quot;:\&quot;2019-11-20T11:13:52.693Z\&quot;,\&quot;reply_count\&quot;:0,\&quot;reply_to_post_number\&quot;:3,\&quot;quote_count\&quot;:0,\&quot;incoming_link_count\&quot;:144,\&quot;reads\&quot;:503,\&quot;readers_count\&quot;:502,\&quot;score\&quot;:940.6,\&quot;yours\&quot;:false,\&quot;topic_id\&quot;:177814,\&quot;topic_slug\&quot;:\&quot;how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project\&quot;,\&quot;display_username\&quot;:\&quot;Roboter\&quot;,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;version\&quot;:1,\&quot;can_edit\&quot;:false,\&quot;can_delete\&quot;:false,\&quot;can_recover\&quot;:false,\&quot;can_wiki\&quot;:false,\&quot;read\&quot;:true,\&quot;user_title\&quot;:null,\&quot;reply_to_user\&quot;:{\&quot;username\&quot;:\&quot;mcroni\&quot;,\&quot;avatar_template\&quot;:\&quot;/user_avatar/forum.ionicframework.com/mcroni/{size}/129308_2.png\&quot;},\&quot;bookmarked\&quot;:false,\&quot;actions_summary\&quot;:[{\&quot;id\&quot;:2,\&quot;count\&quot;:8}],\&quot;moderator\&quot;:false,\&quot;admin\&quot;:false,\&quot;staff\&quot;:false,\&quot;user_id\&quot;:158492,\&quot;hidden\&quot;:false,\&quot;trust_level\&quot;:1,\&quot;deleted_at\&quot;:null,\&quot;user_deleted\&quot;:false,\&quot;edit_reason\&quot;:null,\&quot;can_view_edit_history\&quot;:true,\&quot;wiki\&quot;:false,\&quot;can_accept_answer\&quot;:false,\&quot;can_unaccept_answer\&quot;:false,\&quot;accepted_answer\&quot;:false},{\&quot;id\&quot;:446747,\&quot;name\&quot;:\&quot;Swapnil P133\&quot;,\&quot;username\&quot;:\&quot;SwapnilP133\&quot;,\&quot;avatar_template\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/s/a9adbd/{size}.png\&quot;,\&quot;created_at\&quot;:\&quot;2019-11-20T14:17:48.872Z\&quot;,\&quot;cooked\&quot;:\&quot;\\u003cp\\u003eI have a current project in Cordova and it is integrated with Team City CI / CD.\\u003cbr\\u003e\\nWe generate .apk and Xcode archives by running Cordova build whenever we push something to the master branch.\\u003cbr\\u003e\\nI like Capacitor but didn’t find the capacitor build commands for my scenario.\\u003c/p\\u003e\&quot;,\&quot;post_number\&quot;:6,\&quot;post_type\&quot;:1,\&quot;updated_at\&quot;:\&quot;2019-11-20T14:17:48.872Z\&quot;,\&quot;reply_count\&quot;:0,\&quot;reply_to_post_number\&quot;:null,\&quot;quote_count\&quot;:0,\&quot;incoming_link_count\&quot;:212,\&quot;reads\&quot;:475,\&quot;readers_count\&quot;:474,\&quot;score\&quot;:1155.0,\&quot;yours\&quot;:false,\&quot;topic_id\&quot;:177814,\&quot;topic_slug\&quot;:\&quot;how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project\&quot;,\&quot;display_username\&quot;:\&quot;Swapnil P133\&quot;,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;version\&quot;:1,\&quot;can_edit\&quot;:false,\&quot;can_delete\&quot;:false,\&quot;can_recover\&quot;:false,\&quot;can_wiki\&quot;:false,\&quot;read\&quot;:true,\&quot;user_title\&quot;:null,\&quot;bookmarked\&quot;:false,\&quot;actions_summary\&quot;:[],\&quot;moderator\&quot;:false,\&quot;admin\&quot;:false,\&quot;staff\&quot;:false,\&quot;user_id\&quot;:148822,\&quot;hidden\&quot;:false,\&quot;trust_level\&quot;:1,\&quot;deleted_at\&quot;:null,\&quot;user_deleted\&quot;:false,\&quot;edit_reason\&quot;:null,\&quot;can_view_edit_history\&quot;:true,\&quot;wiki\&quot;:false,\&quot;can_accept_answer\&quot;:false,\&quot;can_unaccept_answer\&quot;:false,\&quot;accepted_answer\&quot;:false},{\&quot;id\&quot;:446773,\&quot;name\&quot;:\&quot;Mikrochipkid\&quot;,\&quot;username\&quot;:\&quot;mikrochipkid\&quot;,\&quot;avatar_template\&quot;:\&quot;/user_avatar/forum.ionicframework.com/mikrochipkid/{size}/116956_2.png\&quot;,\&quot;created_at\&quot;:\&quot;2019-11-20T19:11:14.646Z\&quot;,\&quot;cooked\&quot;:\&quot;\\u003cp\\u003eYou can’t. Capacitor just opens the IDEs that you need in order to build Platform projects.\\u003c/p\\u003e\&quot;,\&quot;post_number\&quot;:7,\&quot;post_type\&quot;:1,\&quot;updated_at\&quot;:\&quot;2019-11-20T19:11:14.646Z\&quot;,\&quot;reply_count\&quot;:1,\&quot;reply_to_post_number\&quot;:null,\&quot;quote_count\&quot;:0,\&quot;incoming_link_count\&quot;:355,\&quot;reads\&quot;:461,\&quot;readers_count\&quot;:460,\&quot;score\&quot;:1887.2,\&quot;yours\&quot;:false,\&quot;topic_id\&quot;:177814,\&quot;topic_slug\&quot;:\&quot;how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project\&quot;,\&quot;display_username\&quot;:\&quot;Mikrochipkid\&quot;,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;version\&quot;:1,\&quot;can_edit\&quot;:false,\&quot;can_delete\&quot;:false,\&quot;can_recover\&quot;:false,\&quot;can_wiki\&quot;:false,\&quot;read\&quot;:true,\&quot;user_title\&quot;:null,\&quot;bookmarked\&quot;:false,\&quot;actions_summary\&quot;:[{\&quot;id\&quot;:2,\&quot;count\&quot;:1}],\&quot;moderator\&quot;:false,\&quot;admin\&quot;:false,\&quot;staff\&quot;:false,\&quot;user_id\&quot;:133774,\&quot;hidden\&quot;:false,\&quot;trust_level\&quot;:2,\&quot;deleted_at\&quot;:null,\&quot;user_deleted\&quot;:false,\&quot;edit_reason\&quot;:null,\&quot;can_view_edit_history\&quot;:true,\&quot;wiki\&quot;:false,\&quot;can_accept_answer\&quot;:false,\&quot;can_unaccept_answer\&quot;:false,\&quot;accepted_answer\&quot;:false},{\&quot;id\&quot;:446777,\&quot;name\&quot;:\&quot;Robert Coie\&quot;,\&quot;username\&quot;:\&quot;rapropos\&quot;,\&quot;avatar_template\&quot;:\&quot;/user_avatar/forum.ionicframework.com/rapropos/{size}/100227_2.png\&quot;,\&quot;created_at\&quot;:\&quot;2019-11-20T19:25:36.276Z\&quot;,\&quot;cooked\&quot;:\&quot;\\u003cp\\u003eI would suggest following/participating in \\u003ca href=\\\&quot;https://github.com/ionic-team/capacitor/issues/324\\\&quot;\\u003ethis issue\\u003c/a\\u003e.\\u003c/p\\u003e\&quot;,\&quot;post_number\&quot;:8,\&quot;post_type\&quot;:1,\&quot;updated_at\&quot;:\&quot;2019-11-20T19:25:36.276Z\&quot;,\&quot;reply_count\&quot;:0,\&quot;reply_to_post_number\&quot;:null,\&quot;quote_count\&quot;:0,\&quot;incoming_link_count\&quot;:817,\&quot;reads\&quot;:458,\&quot;readers_count\&quot;:457,\&quot;score\&quot;:4166.6,\&quot;yours\&quot;:false,\&quot;topic_id\&quot;:177814,\&quot;topic_slug\&quot;:\&quot;how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project\&quot;,\&quot;display_username\&quot;:\&quot;Robert Coie\&quot;,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;version\&quot;:1,\&quot;can_edit\&quot;:false,\&quot;can_delete\&quot;:false,\&quot;can_recover\&quot;:false,\&quot;can_wiki\&quot;:false,\&quot;link_counts\&quot;:[{\&quot;url\&quot;:\&quot;https://github.com/ionic-team/capacitor/issues/324\&quot;,\&quot;internal\&quot;:false,\&quot;reflection\&quot;:false,\&quot;title\&quot;:\&quot;Support building from CLI · Issue #324 · ionic-team/capacitor · GitHub\&quot;,\&quot;clicks\&quot;:667}],\&quot;read\&quot;:true,\&quot;user_title\&quot;:\&quot;Moderator\&quot;,\&quot;title_is_group\&quot;:false,\&quot;bookmarked\&quot;:false,\&quot;actions_summary\&quot;:[{\&quot;id\&quot;:2,\&quot;count\&quot;:1}],\&quot;moderator\&quot;:true,\&quot;admin\&quot;:false,\&quot;staff\&quot;:true,\&quot;user_id\&quot;:106489,\&quot;hidden\&quot;:false,\&quot;trust_level\&quot;:2,\&quot;deleted_at\&quot;:null,\&quot;user_deleted\&quot;:false,\&quot;edit_reason\&quot;:null,\&quot;can_view_edit_history\&quot;:true,\&quot;wiki\&quot;:false,\&quot;can_accept_answer\&quot;:false,\&quot;can_unaccept_answer\&quot;:false,\&quot;accepted_answer\&quot;:false},{\&quot;id\&quot;:464315,\&quot;name\&quot;:\&quot;Codebru\&quot;,\&quot;username\&quot;:\&quot;codebru\&quot;,\&quot;avatar_template\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/c/7ea924/{size}.png\&quot;,\&quot;created_at\&quot;:\&quot;2020-04-09T16:48:35.514Z\&quot;,\&quot;cooked\&quot;:\&quot;\\u003cp\\u003eI was having this issue and the way I worked out to do this:\\u003c/p\\u003e\\n\\u003cp\\u003eYou need to add android first:\\u003c/p\\u003e\\n\\u003cpre\\u003e\\u003ccode class=\\\&quot;lang-auto\\\&quot;\\u003eionic capacitor add android \\n\\u003c/code\\u003e\\u003c/pre\\u003e\\n\\u003cpre\\u003e\\u003ccode class=\\\&quot;lang-auto\\\&quot;\\u003eionic capacitor copy android \\u0026amp;\\u0026amp; cd android \\u0026amp;\\u0026amp; ./gradlew assembleDebug \\u0026amp;\\u0026amp; cd ..\\n\\u003c/code\\u003e\\u003c/pre\\u003e\\n\\u003cp\\u003eThen your apk will be at:\\u003c/p\\u003e\\n\\u003cpre\\u003e\\u003ccode class=\\\&quot;lang-auto\\\&quot;\\u003eandroid/app/build/outputs/apk/debug/app-debug.apk\\n\\u003c/code\\u003e\\u003c/pre\\u003e\\n\\u003cp\\u003eIf you want to run on device directly from command line:\\u003c/p\\u003e\\n\\u003cpre\\u003e\\u003ccode class=\\\&quot;lang-auto\\\&quot;\\u003eionic capacitor copy android \\u0026amp;\\u0026amp; cd android \\u0026amp;\\u0026amp; ./gradlew assembleDebug \\u0026amp;\\u0026amp; ./gradlew installDebug \\u0026amp;\\u0026amp; cd ..\\n\\u003c/code\\u003e\\u003c/pre\\u003e\\n\\u003cp\\u003eNote: It doesn’t work without entering the android directory\\u003c/p\\u003e\\n\\u003cp\\u003eI hope that helps!\\u003c/p\\u003e\&quot;,\&quot;post_number\&quot;:9,\&quot;post_type\&quot;:1,\&quot;updated_at\&quot;:\&quot;2020-04-09T16:48:35.514Z\&quot;,\&quot;reply_count\&quot;:7,\&quot;reply_to_post_number\&quot;:null,\&quot;quote_count\&quot;:0,\&quot;incoming_link_count\&quot;:1198,\&quot;reads\&quot;:421,\&quot;readers_count\&quot;:420,\&quot;score\&quot;:6374.2,\&quot;yours\&quot;:false,\&quot;topic_id\&quot;:177814,\&quot;topic_slug\&quot;:\&quot;how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project\&quot;,\&quot;display_username\&quot;:\&quot;Codebru\&quot;,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;version\&quot;:1,\&quot;can_edit\&quot;:false,\&quot;can_delete\&quot;:false,\&quot;can_recover\&quot;:false,\&quot;can_wiki\&quot;:false,\&quot;read\&quot;:true,\&quot;user_title\&quot;:null,\&quot;bookmarked\&quot;:false,\&quot;actions_summary\&quot;:[{\&quot;id\&quot;:2,\&quot;count\&quot;:20}],\&quot;moderator\&quot;:false,\&quot;admin\&quot;:false,\&quot;staff\&quot;:false,\&quot;user_id\&quot;:161702,\&quot;hidden\&quot;:false,\&quot;trust_level\&quot;:1,\&quot;deleted_at\&quot;:null,\&quot;user_deleted\&quot;:false,\&quot;edit_reason\&quot;:null,\&quot;can_view_edit_history\&quot;:true,\&quot;wiki\&quot;:false,\&quot;can_accept_answer\&quot;:false,\&quot;can_unaccept_answer\&quot;:false,\&quot;accepted_answer\&quot;:false},{\&quot;id\&quot;:467486,\&quot;name\&quot;:\&quot;Rahulsharma841990\&quot;,\&quot;username\&quot;:\&quot;rahulsharma841990\&quot;,\&quot;avatar_template\&quot;:\&quot;/user_avatar/forum.ionicframework.com/rahulsharma841990/{size}/131095_2.png\&quot;,\&quot;created_at\&quot;:\&quot;2020-05-02T08:26:51.565Z\&quot;,\&quot;cooked\&quot;:\&quot;\\u003cp\\u003eAwesome dude!\\u003c/p\\u003e\\n\\u003cp\\u003eIt work’s. What about the release and production apk?\\u003c/p\\u003e\&quot;,\&quot;post_number\&quot;:10,\&quot;post_type\&quot;:1,\&quot;updated_at\&quot;:\&quot;2020-05-02T08:26:51.565Z\&quot;,\&quot;reply_count\&quot;:1,\&quot;reply_to_post_number\&quot;:9,\&quot;quote_count\&quot;:0,\&quot;incoming_link_count\&quot;:304,\&quot;reads\&quot;:370,\&quot;readers_count\&quot;:369,\&quot;score\&quot;:1599.0,\&quot;yours\&quot;:false,\&quot;topic_id\&quot;:177814,\&quot;topic_slug\&quot;:\&quot;how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project\&quot;,\&quot;display_username\&quot;:\&quot;Rahulsharma841990\&quot;,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;version\&quot;:1,\&quot;can_edit\&quot;:false,\&quot;can_delete\&quot;:false,\&quot;can_recover\&quot;:false,\&quot;can_wiki\&quot;:false,\&quot;read\&quot;:true,\&quot;user_title\&quot;:null,\&quot;reply_to_user\&quot;:{\&quot;username\&quot;:\&quot;codebru\&quot;,\&quot;avatar_template\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/c/7ea924/{size}.png\&quot;},\&quot;bookmarked\&quot;:false,\&quot;actions_summary\&quot;:[],\&quot;moderator\&quot;:false,\&quot;admin\&quot;:false,\&quot;staff\&quot;:false,\&quot;user_id\&quot;:161032,\&quot;hidden\&quot;:false,\&quot;trust_level\&quot;:2,\&quot;deleted_at\&quot;:null,\&quot;user_deleted\&quot;:false,\&quot;edit_reason\&quot;:null,\&quot;can_view_edit_history\&quot;:true,\&quot;wiki\&quot;:false,\&quot;can_accept_answer\&quot;:false,\&quot;can_unaccept_answer\&quot;:false,\&quot;accepted_answer\&quot;:false},{\&quot;id\&quot;:467705,\&quot;name\&quot;:\&quot;Codebru\&quot;,\&quot;username\&quot;:\&quot;codebru\&quot;,\&quot;avatar_template\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/c/7ea924/{size}.png\&quot;,\&quot;created_at\&quot;:\&quot;2020-05-04T09:13:18.252Z\&quot;,\&quot;cooked\&quot;:\&quot;\\u003cp\\u003eI have not done this yet, please share your solution if you do it.\\u003c/p\\u003e\&quot;,\&quot;post_number\&quot;:11,\&quot;post_type\&quot;:1,\&quot;updated_at\&quot;:\&quot;2020-05-04T09:13:18.252Z\&quot;,\&quot;reply_count\&quot;:1,\&quot;reply_to_post_number\&quot;:10,\&quot;quote_count\&quot;:0,\&quot;incoming_link_count\&quot;:357,\&quot;reads\&quot;:342,\&quot;readers_count\&quot;:341,\&quot;score\&quot;:1843.4,\&quot;yours\&quot;:false,\&quot;topic_id\&quot;:177814,\&quot;topic_slug\&quot;:\&quot;how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project\&quot;,\&quot;display_username\&quot;:\&quot;Codebru\&quot;,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;version\&quot;:1,\&quot;can_edit\&quot;:false,\&quot;can_delete\&quot;:false,\&quot;can_recover\&quot;:false,\&quot;can_wiki\&quot;:false,\&quot;read\&quot;:true,\&quot;user_title\&quot;:null,\&quot;reply_to_user\&quot;:{\&quot;username\&quot;:\&quot;rahulsharma841990\&quot;,\&quot;avatar_template\&quot;:\&quot;/user_avatar/forum.ionicframework.com/rahulsharma841990/{size}/131095_2.png\&quot;},\&quot;bookmarked\&quot;:false,\&quot;actions_summary\&quot;:[],\&quot;moderator\&quot;:false,\&quot;admin\&quot;:false,\&quot;staff\&quot;:false,\&quot;user_id\&quot;:161702,\&quot;hidden\&quot;:false,\&quot;trust_level\&quot;:1,\&quot;deleted_at\&quot;:null,\&quot;user_deleted\&quot;:false,\&quot;edit_reason\&quot;:null,\&quot;can_view_edit_history\&quot;:true,\&quot;wiki\&quot;:false,\&quot;can_accept_answer\&quot;:false,\&quot;can_unaccept_answer\&quot;:false,\&quot;accepted_answer\&quot;:false},{\&quot;id\&quot;:467906,\&quot;name\&quot;:\&quot;Kazlauskis\&quot;,\&quot;username\&quot;:\&quot;kazlauskis\&quot;,\&quot;avatar_template\&quot;:\&quot;/user_avatar/forum.ionicframework.com/kazlauskis/{size}/134293_2.png\&quot;,\&quot;created_at\&quot;:\&quot;2020-05-05T14:38:16.374Z\&quot;,\&quot;cooked\&quot;:\&quot;\\u003cp\\u003eHere is how to production build for Android:\\u003c/p\\u003e\\n\\u003cpre\\u003e\\u003ccode class=\\\&quot;lang-auto\\\&quot;\\u003ecd android \\u0026amp;\\u0026amp; \\n./gradlew assembleRelease \\u0026amp;\\u0026amp; \\ncd app/build/outputs/apk/release \\u0026amp;\\u0026amp;\\njarsigner -keystore YOUR_KEYSTORE_PATH -storepass YOUR_KEYSTORE_PASS app-release-unsigned.apk YOUR_KEYSTORE_ALIAS \\u0026amp;\\u0026amp;\\nzipalign 4 app-release-unsigned.apk app-release.apk\\n\\u003c/code\\u003e\\u003c/pre\\u003e\\n\\u003cp\\u003eThis will generate \\u003ccode\\u003eapp-release.apk\\u003c/code\\u003e which should be good to go the play store (see \\u003ccode\\u003eandroid/app/build/outputs/apk/release\\u003c/code\\u003e folder).\\u003c/p\\u003e\\n\\u003cp\\u003eHere is the jarsigner command \\u003ca href=\\\&quot;https://docs.oracle.com/en/java/javase/14/docs/specs/man/jarsigner.html\\\&quot; rel=\\\&quot;nofollow noopener\\\&quot;\\u003emanual\\u003c/a\\u003e.\\u003c/p\\u003e\&quot;,\&quot;post_number\&quot;:12,\&quot;post_type\&quot;:1,\&quot;updated_at\&quot;:\&quot;2020-05-05T14:38:16.374Z\&quot;,\&quot;reply_count\&quot;:2,\&quot;reply_to_post_number\&quot;:11,\&quot;quote_count\&quot;:0,\&quot;incoming_link_count\&quot;:178,\&quot;reads\&quot;:324,\&quot;readers_count\&quot;:323,\&quot;score\&quot;:1099.8,\&quot;yours\&quot;:false,\&quot;topic_id\&quot;:177814,\&quot;topic_slug\&quot;:\&quot;how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project\&quot;,\&quot;display_username\&quot;:\&quot;Kazlauskis\&quot;,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;version\&quot;:1,\&quot;can_edit\&quot;:false,\&quot;can_delete\&quot;:false,\&quot;can_recover\&quot;:false,\&quot;can_wiki\&quot;:false,\&quot;link_counts\&quot;:[{\&quot;url\&quot;:\&quot;https://docs.oracle.com/en/java/javase/14/docs/specs/man/jarsigner.html\&quot;,\&quot;internal\&quot;:false,\&quot;reflection\&quot;:false,\&quot;title\&quot;:\&quot;The jarsigner Command\&quot;,\&quot;clicks\&quot;:200}],\&quot;read\&quot;:true,\&quot;user_title\&quot;:\&quot;\&quot;,\&quot;reply_to_user\&quot;:{\&quot;username\&quot;:\&quot;codebru\&quot;,\&quot;avatar_template\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/c/7ea924/{size}.png\&quot;},\&quot;bookmarked\&quot;:false,\&quot;actions_summary\&quot;:[{\&quot;id\&quot;:2,\&quot;count\&quot;:9}],\&quot;moderator\&quot;:false,\&quot;admin\&quot;:false,\&quot;staff\&quot;:false,\&quot;user_id\&quot;:162375,\&quot;hidden\&quot;:false,\&quot;trust_level\&quot;:1,\&quot;deleted_at\&quot;:null,\&quot;user_deleted\&quot;:false,\&quot;edit_reason\&quot;:null,\&quot;can_view_edit_history\&quot;:true,\&quot;wiki\&quot;:false,\&quot;can_accept_answer\&quot;:false,\&quot;can_unaccept_answer\&quot;:false,\&quot;accepted_answer\&quot;:false},{\&quot;id\&quot;:468089,\&quot;name\&quot;:\&quot;Ansh Varun\&quot;,\&quot;username\&quot;:\&quot;anshcena\&quot;,\&quot;avatar_template\&quot;:\&quot;/user_avatar/forum.ionicframework.com/anshcena/{size}/129403_2.png\&quot;,\&quot;created_at\&quot;:\&quot;2020-05-06T15:47:15.198Z\&quot;,\&quot;cooked\&quot;:\&quot;\\u003cp\\u003eThanks, worked fine! Saved my day \\u003cimg src=\\\&quot;https://emoji.discourse-cdn.com/twitter/slight_smile.png?v=9\\\&quot; title=\\\&quot;:slight_smile:\\\&quot; class=\\\&quot;emoji\\\&quot; alt=\\\&quot;:slight_smile:\\\&quot;\\u003e\\u003c/p\\u003e\&quot;,\&quot;post_number\&quot;:13,\&quot;post_type\&quot;:1,\&quot;updated_at\&quot;:\&quot;2020-05-06T15:47:15.198Z\&quot;,\&quot;reply_count\&quot;:0,\&quot;reply_to_post_number\&quot;:9,\&quot;quote_count\&quot;:0,\&quot;incoming_link_count\&quot;:41,\&quot;reads\&quot;:301,\&quot;readers_count\&quot;:300,\&quot;score\&quot;:280.2,\&quot;yours\&quot;:false,\&quot;topic_id\&quot;:177814,\&quot;topic_slug\&quot;:\&quot;how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project\&quot;,\&quot;display_username\&quot;:\&quot;Ansh Varun\&quot;,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;version\&quot;:1,\&quot;can_edit\&quot;:false,\&quot;can_delete\&quot;:false,\&quot;can_recover\&quot;:false,\&quot;can_wiki\&quot;:false,\&quot;read\&quot;:true,\&quot;user_title\&quot;:\&quot;\&quot;,\&quot;reply_to_user\&quot;:{\&quot;username\&quot;:\&quot;codebru\&quot;,\&quot;avatar_template\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/c/7ea924/{size}.png\&quot;},\&quot;bookmarked\&quot;:false,\&quot;actions_summary\&quot;:[{\&quot;id\&quot;:2,\&quot;count\&quot;:1}],\&quot;moderator\&quot;:false,\&quot;admin\&quot;:false,\&quot;staff\&quot;:false,\&quot;user_id\&quot;:158311,\&quot;hidden\&quot;:false,\&quot;trust_level\&quot;:2,\&quot;deleted_at\&quot;:null,\&quot;user_deleted\&quot;:false,\&quot;edit_reason\&quot;:null,\&quot;can_view_edit_history\&quot;:true,\&quot;wiki\&quot;:false,\&quot;can_accept_answer\&quot;:false,\&quot;can_unaccept_answer\&quot;:false,\&quot;accepted_answer\&quot;:false},{\&quot;id\&quot;:468512,\&quot;name\&quot;:\&quot;Codebru\&quot;,\&quot;username\&quot;:\&quot;codebru\&quot;,\&quot;avatar_template\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/c/7ea924/{size}.png\&quot;,\&quot;created_at\&quot;:\&quot;2020-05-11T08:12:33.937Z\&quot;,\&quot;cooked\&quot;:\&quot;\\u003cp\\u003eThanks, this worked for me and saved me a bunch of time!\\u003c/p\\u003e\&quot;,\&quot;post_number\&quot;:14,\&quot;post_type\&quot;:1,\&quot;updated_at\&quot;:\&quot;2020-05-11T08:12:33.937Z\&quot;,\&quot;reply_count\&quot;:0,\&quot;reply_to_post_number\&quot;:12,\&quot;quote_count\&quot;:0,\&quot;incoming_link_count\&quot;:36,\&quot;reads\&quot;:289,\&quot;readers_count\&quot;:288,\&quot;score\&quot;:267.8,\&quot;yours\&quot;:false,\&quot;topic_id\&quot;:177814,\&quot;topic_slug\&quot;:\&quot;how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project\&quot;,\&quot;display_username\&quot;:\&quot;Codebru\&quot;,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;version\&quot;:1,\&quot;can_edit\&quot;:false,\&quot;can_delete\&quot;:false,\&quot;can_recover\&quot;:false,\&quot;can_wiki\&quot;:false,\&quot;read\&quot;:true,\&quot;user_title\&quot;:null,\&quot;reply_to_user\&quot;:{\&quot;username\&quot;:\&quot;kazlauskis\&quot;,\&quot;avatar_template\&quot;:\&quot;/user_avatar/forum.ionicframework.com/kazlauskis/{size}/134293_2.png\&quot;},\&quot;bookmarked\&quot;:false,\&quot;actions_summary\&quot;:[{\&quot;id\&quot;:2,\&quot;count\&quot;:2}],\&quot;moderator\&quot;:false,\&quot;admin\&quot;:false,\&quot;staff\&quot;:false,\&quot;user_id\&quot;:161702,\&quot;hidden\&quot;:false,\&quot;trust_level\&quot;:1,\&quot;deleted_at\&quot;:null,\&quot;user_deleted\&quot;:false,\&quot;edit_reason\&quot;:null,\&quot;can_view_edit_history\&quot;:true,\&quot;wiki\&quot;:false,\&quot;can_accept_answer\&quot;:false,\&quot;can_unaccept_answer\&quot;:false,\&quot;accepted_answer\&quot;:false},{\&quot;id\&quot;:473825,\&quot;name\&quot;:\&quot;Cordial666\&quot;,\&quot;username\&quot;:\&quot;cordial666\&quot;,\&quot;avatar_template\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/c/13edae/{size}.png\&quot;,\&quot;created_at\&quot;:\&quot;2020-06-30T22:21:18.410Z\&quot;,\&quot;cooked\&quot;:\&quot;\\u003caside class=\\\&quot;quote no-group\\\&quot; data-username=\\\&quot;kazlauskis\\\&quot; data-post=\\\&quot;12\\\&quot; data-topic=\\\&quot;177814\\\&quot;\\u003e\\n\\u003cdiv class=\\\&quot;title\\\&quot;\\u003e\\n\\u003cdiv class=\\\&quot;quote-controls\\\&quot;\\u003e\\u003c/div\\u003e\\n\\u003cimg alt=\\\&quot;\\\&quot; width=\\\&quot;20\\\&quot; height=\\\&quot;20\\\&quot; src=\\\&quot;https://sea2.discourse-cdn.com/ionicframework/user_avatar/forum.ionicframework.com/kazlauskis/40/132156_2.png\\\&quot; class=\\\&quot;avatar\\\&quot;\\u003e kazlauskis:\\u003c/div\\u003e\\n\\u003cblockquote\\u003e\\n\\u003cp\\u003e\\u003ccode\\u003eYOUR_KEYSTORE_PASS\\u003c/code\\u003e\\u003c/p\\u003e\\n\\u003c/blockquote\\u003e\\n\\u003c/aside\\u003e\\n\\u003cp\\u003eWhat should YOUR_KEYSTORE_ALIAS be?\\u003c/p\\u003e\&quot;,\&quot;post_number\&quot;:15,\&quot;post_type\&quot;:1,\&quot;updated_at\&quot;:\&quot;2020-06-30T22:21:18.410Z\&quot;,\&quot;reply_count\&quot;:1,\&quot;reply_to_post_number\&quot;:12,\&quot;quote_count\&quot;:1,\&quot;incoming_link_count\&quot;:59,\&quot;reads\&quot;:250,\&quot;readers_count\&quot;:249,\&quot;score\&quot;:350.0,\&quot;yours\&quot;:false,\&quot;topic_id\&quot;:177814,\&quot;topic_slug\&quot;:\&quot;how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project\&quot;,\&quot;display_username\&quot;:\&quot;Cordial666\&quot;,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;version\&quot;:1,\&quot;can_edit\&quot;:false,\&quot;can_delete\&quot;:false,\&quot;can_recover\&quot;:false,\&quot;can_wiki\&quot;:false,\&quot;read\&quot;:true,\&quot;user_title\&quot;:null,\&quot;bookmarked\&quot;:false,\&quot;actions_summary\&quot;:[],\&quot;moderator\&quot;:false,\&quot;admin\&quot;:false,\&quot;staff\&quot;:false,\&quot;user_id\&quot;:163478,\&quot;hidden\&quot;:false,\&quot;trust_level\&quot;:1,\&quot;deleted_at\&quot;:null,\&quot;user_deleted\&quot;:false,\&quot;edit_reason\&quot;:null,\&quot;can_view_edit_history\&quot;:true,\&quot;wiki\&quot;:false,\&quot;can_accept_answer\&quot;:false,\&quot;can_unaccept_answer\&quot;:false,\&quot;accepted_answer\&quot;:false},{\&quot;id\&quot;:473851,\&quot;name\&quot;:\&quot;Kazlauskis\&quot;,\&quot;username\&quot;:\&quot;kazlauskis\&quot;,\&quot;avatar_template\&quot;:\&quot;/user_avatar/forum.ionicframework.com/kazlauskis/{size}/134293_2.png\&quot;,\&quot;created_at\&quot;:\&quot;2020-07-01T08:17:31.120Z\&quot;,\&quot;cooked\&quot;:\&quot;\\u003cp\\u003eYou can find your keystore alias by running \\u003ccode\\u003ekeytool -v -list -keystore YOUR_KEYSTORE_PATH\\u003c/code\\u003e\\u003c/p\\u003e\&quot;,\&quot;post_number\&quot;:16,\&quot;post_type\&quot;:1,\&quot;updated_at\&quot;:\&quot;2020-07-01T08:17:31.120Z\&quot;,\&quot;reply_count\&quot;:0,\&quot;reply_to_post_number\&quot;:15,\&quot;quote_count\&quot;:0,\&quot;incoming_link_count\&quot;:37,\&quot;reads\&quot;:228,\&quot;readers_count\&quot;:227,\&quot;score\&quot;:230.6,\&quot;yours\&quot;:false,\&quot;topic_id\&quot;:177814,\&quot;topic_slug\&quot;:\&quot;how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project\&quot;,\&quot;display_username\&quot;:\&quot;Kazlauskis\&quot;,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;version\&quot;:1,\&quot;can_edit\&quot;:false,\&quot;can_delete\&quot;:false,\&quot;can_recover\&quot;:false,\&quot;can_wiki\&quot;:false,\&quot;read\&quot;:true,\&quot;user_title\&quot;:\&quot;\&quot;,\&quot;reply_to_user\&quot;:{\&quot;username\&quot;:\&quot;cordial666\&quot;,\&quot;avatar_template\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/c/13edae/{size}.png\&quot;},\&quot;bookmarked\&quot;:false,\&quot;actions_summary\&quot;:[],\&quot;moderator\&quot;:false,\&quot;admin\&quot;:false,\&quot;staff\&quot;:false,\&quot;user_id\&quot;:162375,\&quot;hidden\&quot;:false,\&quot;trust_level\&quot;:1,\&quot;deleted_at\&quot;:null,\&quot;user_deleted\&quot;:false,\&quot;edit_reason\&quot;:null,\&quot;can_view_edit_history\&quot;:true,\&quot;wiki\&quot;:false,\&quot;can_accept_answer\&quot;:false,\&quot;can_unaccept_answer\&quot;:false,\&quot;accepted_answer\&quot;:false},{\&quot;id\&quot;:478765,\&quot;name\&quot;:\&quot;Karthik V V\&quot;,\&quot;username\&quot;:\&quot;Karthik-V-V\&quot;,\&quot;avatar_template\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/k/76d3ee/{size}.png\&quot;,\&quot;created_at\&quot;:\&quot;2020-08-19T06:33:13.785Z\&quot;,\&quot;cooked\&quot;:\&quot;\\u003cp\\u003eAfter spending a whole night trying to configure Android studio, which wouldn’t let a simple ionic app build properly, and then trying to fix issues for cordova, this post of yours gave me my spirits back! You’re really awesome man!!\\u003c/p\\u003e\&quot;,\&quot;post_number\&quot;:17,\&quot;post_type\&quot;:1,\&quot;updated_at\&quot;:\&quot;2020-08-19T06:33:13.785Z\&quot;,\&quot;reply_count\&quot;:0,\&quot;reply_to_post_number\&quot;:9,\&quot;quote_count\&quot;:0,\&quot;incoming_link_count\&quot;:111,\&quot;reads\&quot;:195,\&quot;readers_count\&quot;:194,\&quot;score\&quot;:604.0,\&quot;yours\&quot;:false,\&quot;topic_id\&quot;:177814,\&quot;topic_slug\&quot;:\&quot;how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project\&quot;,\&quot;display_username\&quot;:\&quot;Karthik V V\&quot;,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;version\&quot;:1,\&quot;can_edit\&quot;:false,\&quot;can_delete\&quot;:false,\&quot;can_recover\&quot;:false,\&quot;can_wiki\&quot;:false,\&quot;read\&quot;:true,\&quot;user_title\&quot;:null,\&quot;reply_to_user\&quot;:{\&quot;username\&quot;:\&quot;codebru\&quot;,\&quot;avatar_template\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/c/7ea924/{size}.png\&quot;},\&quot;bookmarked\&quot;:false,\&quot;actions_summary\&quot;:[{\&quot;id\&quot;:2,\&quot;count\&quot;:1}],\&quot;moderator\&quot;:false,\&quot;admin\&quot;:false,\&quot;staff\&quot;:false,\&quot;user_id\&quot;:164600,\&quot;hidden\&quot;:false,\&quot;trust_level\&quot;:1,\&quot;deleted_at\&quot;:null,\&quot;user_deleted\&quot;:false,\&quot;edit_reason\&quot;:null,\&quot;can_view_edit_history\&quot;:true,\&quot;wiki\&quot;:false,\&quot;can_accept_answer\&quot;:false,\&quot;can_unaccept_answer\&quot;:false,\&quot;accepted_answer\&quot;:false},{\&quot;id\&quot;:480863,\&quot;name\&quot;:\&quot;Rahjain\&quot;,\&quot;username\&quot;:\&quot;rahjain\&quot;,\&quot;avatar_template\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/r/e274bd/{size}.png\&quot;,\&quot;created_at\&quot;:\&quot;2020-09-05T08:01:49.693Z\&quot;,\&quot;cooked\&quot;:\&quot;\\u003cp\\u003eJust a trick to know all the targets -\\u003c/p\\u003e\\n\\u003cpre\\u003e\\u003ccode class=\\\&quot;lang-auto\\\&quot;\\u003ecd android \\ngradlew app:tasks --all\\n\\u003c/code\\u003e\\u003c/pre\\u003e\\n\\u003cp\\u003eThis will out you all the tasks which can be called by gradlew without opening android studio.\\u003cbr\\u003e\\nExample for building app bundle\\u003c/p\\u003e\\n\\u003cpre\\u003e\\u003ccode class=\\\&quot;lang-auto\\\&quot;\\u003e./gradlew bundleRelease\\n\\u003c/code\\u003e\\u003c/pre\\u003e\\n\\u003cp\\u003eHope it helps \\u003cimg src=\\\&quot;https://emoji.discourse-cdn.com/twitter/slight_smile.png?v=9\\\&quot; title=\\\&quot;:slight_smile:\\\&quot; class=\\\&quot;emoji\\\&quot; alt=\\\&quot;:slight_smile:\\\&quot;\\u003e\\u003c/p\\u003e\&quot;,\&quot;post_number\&quot;:18,\&quot;post_type\&quot;:1,\&quot;updated_at\&quot;:\&quot;2020-09-05T08:01:49.693Z\&quot;,\&quot;reply_count\&quot;:0,\&quot;reply_to_post_number\&quot;:null,\&quot;quote_count\&quot;:0,\&quot;incoming_link_count\&quot;:77,\&quot;reads\&quot;:189,\&quot;readers_count\&quot;:188,\&quot;score\&quot;:447.8,\&quot;yours\&quot;:false,\&quot;topic_id\&quot;:177814,\&quot;topic_slug\&quot;:\&quot;how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project\&quot;,\&quot;display_username\&quot;:\&quot;Rahjain\&quot;,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;version\&quot;:1,\&quot;can_edit\&quot;:false,\&quot;can_delete\&quot;:false,\&quot;can_recover\&quot;:false,\&quot;can_wiki\&quot;:false,\&quot;read\&quot;:true,\&quot;user_title\&quot;:null,\&quot;bookmarked\&quot;:false,\&quot;actions_summary\&quot;:[{\&quot;id\&quot;:2,\&quot;count\&quot;:2}],\&quot;moderator\&quot;:false,\&quot;admin\&quot;:false,\&quot;staff\&quot;:false,\&quot;user_id\&quot;:151481,\&quot;hidden\&quot;:false,\&quot;trust_level\&quot;:2,\&quot;deleted_at\&quot;:null,\&quot;user_deleted\&quot;:false,\&quot;edit_reason\&quot;:null,\&quot;can_view_edit_history\&quot;:true,\&quot;wiki\&quot;:false,\&quot;can_accept_answer\&quot;:false,\&quot;can_unaccept_answer\&quot;:false,\&quot;accepted_answer\&quot;:false},{\&quot;id\&quot;:486431,\&quot;name\&quot;:\&quot;Hfunescom\&quot;,\&quot;username\&quot;:\&quot;hfunescom\&quot;,\&quot;avatar_template\&quot;:\&quot;/user_avatar/forum.ionicframework.com/hfunescom/{size}/133991_2.png\&quot;,\&quot;created_at\&quot;:\&quot;2020-10-23T20:38:38.887Z\&quot;,\&quot;cooked\&quot;:\&quot;\\u003caside class=\\\&quot;quote no-group\\\&quot; data-username=\\\&quot;codebru\\\&quot; data-post=\\\&quot;9\\\&quot; data-topic=\\\&quot;177814\\\&quot;\\u003e\\n\\u003cdiv class=\\\&quot;title\\\&quot;\\u003e\\n\\u003cdiv class=\\\&quot;quote-controls\\\&quot;\\u003e\\u003c/div\\u003e\\n\\u003cimg alt=\\\&quot;\\\&quot; width=\\\&quot;20\\\&quot; height=\\\&quot;20\\\&quot; src=\\\&quot;https://avatars.discourse-cdn.com/v4/letter/c/7ea924/40.png\\\&quot; class=\\\&quot;avatar\\\&quot;\\u003e codebru:\\u003c/div\\u003e\\n\\u003cblockquote\\u003e\\n\\u003cp\\u003e\\u003ccode\\u003eandroid/app/build/outputs/apk/debug/\\u003c/code\\u003e\\u003c/p\\u003e\\n\\u003c/blockquote\\u003e\\n\\u003c/aside\\u003e\\n\\u003cp\\u003eCould continue with my Gitlab CI config because of you \\u003cimg src=\\\&quot;https://emoji.discourse-cdn.com/twitter/slight_smile.png?v=9\\\&quot; title=\\\&quot;:slight_smile:\\\&quot; class=\\\&quot;emoji\\\&quot; alt=\\\&quot;:slight_smile:\\\&quot;\\u003e\\u003cbr\\u003e\\nThank you so much!\\u003c/p\\u003e\&quot;,\&quot;post_number\&quot;:19,\&quot;post_type\&quot;:1,\&quot;updated_at\&quot;:\&quot;2020-10-23T20:38:38.887Z\&quot;,\&quot;reply_count\&quot;:0,\&quot;reply_to_post_number\&quot;:9,\&quot;quote_count\&quot;:1,\&quot;incoming_link_count\&quot;:31,\&quot;reads\&quot;:155,\&quot;readers_count\&quot;:154,\&quoquot;score\&quot;:201.0,\&quot;yours\&quot;:false,\&quot;topic_id\&quot;:177814,\&quot;topic_slug\&quot;:\&quot;how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project\&quot;,\&quot;display_username\&quot;:\&quot;Hfunescom\&quot;,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;version\&quot;:1,\&quot;can_edit\&quot;:false,\&quot;can_delete\&quot;:false,\&quot;can_recover\&quot;:false,\&quot;can_wiki\&quot;:false,\&quot;read\&quot;:true,\&quot;user_title\&quot;:null,\&quot;bookmarked\&quot;:false,\&quot;actions_summary\&quot;:[{\&quot;id\&quot;:2,\&quot;count\&quot;:1}],\&quot;moderator\&quot;:false,\&quot;admin\&quot;:false,\&quot;staff\&quot;:false,\&quot;user_id\&quot;:165153,\&quot;hidden\&quot;:false,\&quot;trust_level\&quot;:0,\&quot;deleted_at\&quot;:null,\&quot;user_deleted\&quot;:false,\&quot;edit_reason\&quot;:null,\&quot;can_view_edit_history\&quot;:true,\&quot;wiki\&quot;:false,\&quot;can_accept_answer\&quot;:false,\&quot;can_unaccept_answer\&quot;:false,\&quot;accepted_answer\&quot;:false},{\&quot;id\&quot;:486660,\&quot;name\&quot;:\&quot;Ai Abdrahim\&quot;,\&quot;username\&quot;:\&quot;AiAbdrahim\&quot;,\&quot;avatar_template\&quot;:\&quot;/user_avatar/forum.ionicframework.com/aiabdrahim/{size}/134644_2.png\&quot;,\&quot;created_at\&quot;:\&quot;2020-10-26T10:50:47.990Z\&quot;,\&quot;cooked\&quot;:\&quot;\\u003cp\\u003eThank u bro \\u003cimg src=\\\&quot;https://emoji.discourse-cdn.com/twitter/heart_eyes.png?v=9\\\&quot; title=\\\&quot;:heart_eyes:\\\&quot; class=\\\&quot;emoji\\\&quot; alt=\\\&quot;:heart_eyes:\\\&quot;\\u003e \\u003cimg src=\\\&quot;https://emoji.discourse-cdn.com/twitter/smiling_face_with_three_hearts.png?v=9\\\&quot; title=\\\&quot;:smiling_face_with_three_hearts:\\\&quot; class=\\\&quot;emoji\\\&quot; alt=\\\&quot;:smiling_face_with_three_hearts:\\\&quot;\\u003e \\u003cimg src=\\\&quot;https://emoji.discourse-cdn.com/twitter/tada.png?v=9\\\&quot; title=\\\&quot;:tada:\\\&quot; class=\\\&quot;emoji\\\&quot; alt=\\\&quot;:tada:\\\&quot;\\u003e \\u003cimg src=\\\&quot;https://emoji.discourse-cdn.com/twitter/tada.png?v=9\\\&quot; title=\\\&quot;:tada:\\\&quot; class=\\\&quot;emoji\\\&quot; alt=\\\&quot;:tada:\\\&quot;\\u003e \\u003cimg src=\\\&quot;https://emoji.discourse-cdn.com/twitter/tada.png?v=9\\\&quot; title=\\\&quot;:tada:\\\&quot; class=\\\&quot;emoji\\\&quot; alt=\\\&quot;:tada:\\\&quot;\\u003e \\u003cimg src=\\\&quot;https://emoji.discourse-cdn.com/twitter/tada.png?v=9\\\&quot; title=\\\&quot;:tada:\\\&quot; class=\\\&quot;emoji\\\&quot; alt=\\\&quot;:tada:\\\&quot;\\u003e \\u003cimg src=\\\&quot;https://emoji.discourse-cdn.com/twitter/confetti_ball.png?v=9\\\&quot; title=\\\&quot;:confetti_ball:\\\&quot; class=\\\&quot;emoji\\\&quot; alt=\\\&quot;:confetti_ball:\\\&quot;\\u003e \\u003cimg src=\\\&quot;https://emoji.discourse-cdn.com/twitter/confetti_ball.png?v=9\\\&quot; title=\\\&quot;:confetti_ball:\\\&quot; class=\\\&quot;emoji\\\&quot; alt=\\\&quot;:confetti_ball:\\\&quot;\\u003e \\u003cimg src=\\\&quot;https://emoji.discourse-cdn.com/twitter/1st_place_medal.png?v=9\\\&quot; title=\\\&quot;:1st_place_medal:\\\&quot; class=\\\&quot;emoji\\\&quot; alt=\\\&quot;:1st_place_medal:\\\&quot;\\u003e \\u003cimg src=\\\&quot;https://emoji.discourse-cdn.com/twitter/1st_place_medal.png?v=9\\\&quot; title=\\\&quot;:1st_place_medal:\\\&quot; class=\\\&quot;emoji\\\&quot; alt=\\\&quot;:1st_place_medal:\\\&quot;\\u003e \\u003cimg src=\\\&quot;https://emoji.discourse-cdn.com/twitter/1st_place_medal.png?v=9\\\&quot; title=\\\&quot;:1st_place_medal:\\\&quot; class=\\\&quot;emoji\\\&quot; alt=\\\&quot;:1st_place_medal:\\\&quot;\\u003e \\u003cimg src=\\\&quot;https://emoji.discourse-cdn.com/twitter/1st_place_medal.png?v=9\\\&quot; title=\\\&quot;:1st_place_medal:\\\&quot; class=\\\&quot;emoji\\\&quot; alt=\\\&quot;:1st_place_medal:\\\&quot;\\u003e\\u003c/p\\u003e\&quot;,\&quot;post_number\&quot;:20,\&quot;post_type\&quot;:1,\&quot;updated_at\&quot;:\&quot;2020-10-26T10:50:47.990Z\&quot;,\&quot;reply_count\&quot;:0,\&quot;reply_to_post_number\&quot;:9,\&quot;quote_count\&quot;:0,\&quot;incoming_link_count\&quot;:30,\&quot;reads\&quot;:141,\&quot;readers_count\&quot;:140,\&quot;score\&quot;:193.2,\&quot;yours\&quot;:false,\&quot;topic_id\&quot;:177814,\&quot;topic_slug\&quot;:\&quot;how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project\&quot;,\&quot;display_username\&quot;:\&quot;Ai Abdrahim\&quot;,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;version\&quot;:1,\&quot;can_edit\&quot;:false,\&quot;can_delete\&quot;:false,\&quot;can_recover\&quot;:false,\&quot;can_wiki\&quot;:false,\&quot;read\&quot;:true,\&quot;user_title\&quot;:null,\&quot;reply_to_user\&quot;:{\&quot;username\&quot;:\&quot;codebru\&quot;,\&quot;avatar_template\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/c/7ea924/{size}.png\&quot;},\&quot;bookmarked\&quot;:false,\&quot;actions_summary\&quot;:[{\&quot;id\&quot;:2,\&quot;count\&quot;:1}],\&quot;moderator\&quot;:false,\&quot;admin\&quot;:false,\&quot;staff\&quot;:false,\&quot;user_id\&quot;:166120,\&quot;hidden\&quot;:false,\&quot;trust_level\&quot;:1,\&quot;deleted_at\&quot;:null,\&quot;user_deleted\&quot;:false,\&quot;edit_reason\&quot;:null,\&quot;can_view_edit_history\&quot;:true,\&quot;wiki\&quot;:false,\&quot;can_accept_answer\&quot;:false,\&quot;can_unaccept_answer\&quot;:false,\&quot;accepted_answer\&quot;:false},{\&quot;id\&quot;:492557,\&quot;name\&quot;:\&quot;Obinnae\&quot;,\&quot;username\&quot;:\&quot;obinnae\&quot;,\&quot;avatar_template\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/o/a183cd/{size}.png\&quot;,\&quot;created_at\&quot;:\&quot;2020-12-28T01:57:12.767Z\&quot;,\&quot;cooked\&quot;:\&quot;\\u003cp\\u003eIn case someone on a Mac Big Sur is still having issues, run this (same as the chosen answer, but with ‘sudo’ added)…\\u003c/p\\u003e\\n\\u003cp\\u003e\\u003ccode\\u003esudo ionic capacitor copy android \\u0026amp;\\u0026amp; cd android \\u0026amp;\\u0026amp; sudo ./gradlew assembleDebug \\u0026amp;\\u0026amp; cd ..\\u003c/code\\u003e\\u003c/p\\u003e\&quot;,\&quot;post_number\&quot;:22,\&quot;post_type\&quot;:1,\&quot;updated_at\&quot;:\&quot;2020-12-28T01:57:12.767Z\&quot;,\&quot;reply_count\&quot;:0,\&quot;reply_to_post_number\&quot;:null,\&quot;quote_count\&quot;:0,\&quot;incoming_link_count\&quot;:183,\&quot;reads\&quot;:114,\&quot;readers_count\&quot;:113,\&quot;score\&quot;:947.8,\&quot;yours\&quot;:false,\&quot;topic_id\&quot;:177814,\&quot;topic_slug\&quot;:\&quot;how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project\&quot;,\&quot;display_username\&quot;:\&quot;Obinnae\&quot;,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;version\&quot;:1,\&quot;can_edit\&quot;:false,\&quot;can_delete\&quot;:false,\&quot;can_recover\&quot;:false,\&quot;can_wiki\&quot;:false,\&quot;read\&quot;:true,\&quot;user_title\&quot;:null,\&quot;bookmarked\&quot;:false,\&quot;actions_summary\&quot;:[{\&quot;id\&quot;:2,\&quot;count\&quot;:1}],\&quot;moderator\&quot;:false,\&quot;admin\&quot;:false,\&quot;staff\&quot;:false,\&quot;user_id\&quot;:132700,\&quot;hidden\&quot;:false,\&quot;trust_level\&quot;:2,\&quot;deleted_at\&quot;:null,\&quot;user_deleted\&quot;:false,\&quot;edit_reason\&quot;:null,\&quot;can_view_edit_history\&quot;:true,\&quot;wiki\&quot;:false,\&quot;can_accept_answer\&quot;:false,\&quot;can_unaccept_answer\&quot;:false,\&quot;accepted_answer\&quot;:false}],\&quot;stream\&quot;:[446326,446406,446439,446722,446747,446773,446777,464315,467486,467705,467906,468089,468512,473825,473851,478765,480863,486431,486660,492557,492559,492670,494021,494809,497935,498040,498156,498170,500521,503114,532615]},\&quot;timeline_lookup\&quot;:[[1,691],[4,689],[8,548],[9,525],[10,523],[11,522],[12,521],[13,516],[14,466],[15,465],[16,416],[17,399],[18,351],[19,348],[20,286],[22,284],[23,269],[24,262],[25,233],[26,232],[27,231],[28,230],[29,207],[30,177],[31,26]],\&quot;tags\&quot;:[],\&quot;id\&quot;:177814,\&quot;title\&quot;:\&quot;How to build an Android APK file without using Android Studio in a Capacitor project?\&quot;,\&quot;fancy_title\&quot;:\&quot;How to build an Android APK file without using Android Studio in a Capacitor project?\&quot;,\&quot;posts_count\&quot;:31,\&quot;created_at\&quot;:\&quot;2019-11-18T06:49:00.750Z\&quot;,\&quot;views\&quot;:43837,\&quot;reply_count\&quot;:20,\&quot;like_count\&quot;:50,\&quot;last_posted_at\&quot;:\&quot;2021-09-13T10:14:36.531Z\&quot;,\&quot;visible\&quot;:true,\&quot;closed\&quot;:false,\&quot;archived\&quot;:false,\&quot;has_summary\&quot;:false,\&quot;archetype\&quot;:\&quot;regular\&quot;,\&quot;slug\&quot;:\&quot;how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project\&quot;,\&quot;category_id\&quot;:26,\&quot;word_count\&quot;:1205,\&quot;deleted_at\&quot;:null,\&quot;user_id\&quot;:148822,\&quot;featured_link\&quot;:null,\&quot;pinned_globally\&quot;:false,\&quot;pinned_at\&quot;:null,\&quot;pinned_until\&quot;:null,\&quot;image_url\&quot;:null,\&quot;slow_mode_seconds\&quot;:0,\&quot;draft\&quot;:null,\&quot;draft_key\&quot;:\&quot;topic_177814\&quot;,\&quot;draft_sequence\&quot;:null,\&quot;unpinned\&quot;:null,\&quot;pinned\&quot;:false,\&quot;current_post_number\&quot;:1,\&quot;highest_post_number\&quot;:33,\&quot;deleted_by\&quot;:null,\&quot;actions_summary\&quot;:[{\&quot;id\&quot;:4,\&quot;count\&quot;:0,\&quot;hidden\&quot;:false,\&quot;can_act\&quot;:false},{\&quot;id\&quot;:8,\&quot;count\&quot;:0,\&quot;hidden\&quot;:false,\&quot;can_act\&quot;:false},{\&quot;id\&quot;:7,\&quot;count\&quot;:0,\&quot;hidden\&quot;:false,\&quot;can_act\&quot;:false}],\&quot;chunk_size\&quot;:20,\&quot;bookmarked\&quot;:false,\&quot;bookmarks\&quot;:[],\&quot;topic_timer\&quot;:null,\&quot;message_bus_last_id\&quot;:0,\&quot;participant_count\&quot;:26,\&quot;show_read_indicator\&quot;:false,\&quot;thumbnails\&quot;:null,\&quot;slow_mode_enabled_until\&quot;:null,\&quot;can_vote\&quot;:false,\&quot;vote_count\&quot;:0,\&quot;user_voted\&quot;:false,\&quot;details\&quot;:{\&quot;can_edit\&quot;:false,\&quot;notification_level\&quot;:1,\&quot;participants\&quot;:[{\&quot;id\&quot;:161702,\&quot;username\&quot;:\&quot;codebru\&quot;,\&quot;name\&quot;:\&quot;Codebru\&quot;,\&quot;avatar_template\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/c/7ea924/{size}.png\&quot;,\&quot;post_count\&quot;:3,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;trust_level\&quot;:1},{\&quot;id\&quot;:162375,\&quot;username\&quot;:\&quot;kazlauskis\&quot;,\&quot;name\&quot;:\&quot;Kazlauskis\&quot;,\&quot;avatar_template\&quot;:\&quot;/user_avatar/forum.ionicframework.com/kazlauskis/{size}/134293_2.png\&quot;,\&quot;post_count\&quot;:2,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;trust_level\&quot;:1},{\&quot;id\&quot;:168150,\&quot;username\&quot;:\&quot;Aniee\&quot;,\&quot;name\&quot;:\&quot;Aniee\&quot;,\&quot;avatar_template\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/a/8797f3/{size}.png\&quot;,\&quot;post_count\&quot;:2,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;trust_level\&quot;:1},{\&quot;id\&quot;:148822,\&quot;username\&quot;:\&quot;SwapnilP133\&quot;,\&quot;name\&quot;:\&quot;Swapnil P133\&quot;,\&quot;avatar_template\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/s/a9adbd/{size}.png\&quot;,\&quot;post_count\&quot;:2,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;trust_level\&quot;:1},{\&quot;id\&quot;:161032,\&quot;username\&quot;:\&quot;rahulsharma841990\&quot;,\&quot;name\&quot;:\&quot;Rahulsharma841990\&quot;,\&quot;avatar_template\&quot;:\&quot;/user_avatar/forum.ionicframework.com/rahulsharma841990/{size}/131095_2.png\&quot;,\&quot;post_count\&quot;:1,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;trust_level\&quot;:2},{\&quot;id\&quot;:170290,\&quot;username\&quot;:\&quot;matonga\&quot;,\&quot;name\&quot;:\&quot;Matonga\&quot;,\&quot;avatar_template\&quot;:\&quot;/user_avatar/forum.ionicframework.com/matonga/{size}/137246_2.png\&quot;,\&quot;post_count\&quot;:1,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;trust_level\&quot;:0},{\&quot;id\&quot;:168968,\&quot;username\&quot;:\&quot;Amirul6265\&quot;,\&quot;name\&quot;:\&quot;Amirul6265\&quot;,\&quot;avatar_template\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/a/c89c15/{size}.png\&quot;,\&quot;post_count\&quot;:1,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;trust_level\&quot;:0},{\&quot;id\&quot;:151930,\&quot;username\&quot;:\&quot;terranmarine\&quot;,\&quot;name\&quot;:\&quot;Terranmarine\&quot;,\&quot;avatar_template\&quot;:\&quot;/user_avatar/forum.ionicframework.com/terranmarine/{size}/125840_2.png\&quot;,\&quot;post_count\&quot;:1,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;trust_level\&quot;:2},{\&quot;id\&quot;:171894,\&quot;username\&quot;:\&quot;TomaEduard\&quot;,\&quot;name\&quot;:\&quot;Toma Eduard\&quot;,\&quot;avatar_template\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/t/82dd89/{size}.png\&quot;,\&quot;post_count\&quot;:1,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;trust_level\&quot;:1},{\&quot;id\&quot;:163478,\&quot;username\&quot;:\&quot;cordial666\&quot;,\&quot;name\&quot;:\&quot;Cordial666\&quot;,\&quot;avatar_template\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/c/13edae/{size}.png\&quot;,\&quot;post_count\&quot;:1,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;trust_level\&quot;:1},{\&quot;id\&quot;:165153,\&quot;username\&quot;:\&quot;hfunescom\&quot;,\&quot;name\&quot;:\&quot;Hfunescom\&quot;,\&quot;avatar_template\&quot;:\&quot;/user_avatar/forum.ionicframework.com/hfunescom/{size}/133991_2.png\&quot;,\&quot;post_count\&quot;:1,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;trust_level\&quot;:0},{\&quot;id\&quot;:158431,\&quot;username\&quot;:\&quot;mcroni\&quot;,\&quot;name\&quot;:\&quot;Mcroni\&quot;,\&quot;avatar_template\&quot;:\&quot;/user_avatar/forum.ionicframework.com/mcroni/{size}/129308_2.png\&quot;,\&quot;post_count\&quot;:1,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;trust_level\&quot;:1},{\&quot;id\&quot;:151481,\&quot;username\&quot;:\&quot;rahjain\&quot;,\&quot;name\&quot;:\&quot;Rahjain\&quot;,\&quot;avatar_template\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/r/e274bd/{size}.png\&quot;,\&quot;post_count\&quot;:1,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;trust_level\&quot;:2},{\&quot;id\&quot;:168701,\&quot;username\&quot;:\&quot;pro1\&quot;,\&quot;name\&quot;:\&quot;pro1\&quot;,\&quot;avatar_template\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/p/e68b1a/{size}.png\&quot;,\&quot;post_count\&quot;:1,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;trust_level\&quot;:1},{\&quot;id\&quot;:167575,\&quot;username\&quot;:\&quot;Nusry12\&quot;,\&quot;name\&quot;:\&quot;Nusry12\&quot;,\&quot;avatar_template\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/n/3e96dc/{size}.png\&quot;,\&quot;post_count\&quot;:1,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;trust_level\&quot;:0},{\&quot;id\&quot;:167540,\&quot;username\&quot;:\&quot;sampada21\&quot;,\&quot;name\&quot;:\&quot;Sampada21\&quot;,\&quot;avatar_template\&quot;:\&quot;/user_avatar/forum.ionicframework.com/sampada21/{size}/135525_2.png\&quot;,\&quot;post_count\&quot;:1,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;trust_level\&quot;:0},{\&quot;id\&quot;:158492,\&quot;username\&quot;:\&quot;roboter\&quot;,\&quot;name\&quot;:\&quot;Roboter\&quot;,\&quot;avatar_template\&quot;:\&quot;/user_avatar/forum.ionicframework.com/roboter/{size}/129354_2.png\&quot;,\&quot;post_count\&quot;:1,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;trust_level\&quot;:1},{\&quot;id\&quot;:169569,\&quot;username\&quot;:\&quot;John30013\&quot;,\&quot;name\&quot;:\&quot;John30013\&quot;,\&quot;avatar_template\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/j/4af34b/{size}.png\&quot;,\&quot;post_count\&quot;:1,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;trust_level\&quot;:0},{\&quot;id\&quot;:158311,\&quot;username\&quot;:\&quot;anshcena\&quot;,\&quot;name\&quot;:\&quot;Ansh Varun\&quot;,\&quot;avatar_template\&quot;:\&quot;/user_avatar/forum.ionicframework.com/anshcena/{size}/129403_2.png\&quot;,\&quot;post_count\&quot;:1,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;trust_level\&quot;:2},{\&quot;id\&quot;:106489,\&quot;username\&quot;:\&quot;rapropos\&quot;,\&quot;name\&quot;:\&quot;Robert Coie\&quot;,\&quot;avatar_template\&quot;:\&quot;/user_avatar/forum.ionicframework.com/rapropos/{size}/100227_2.png\&quot;,\&quot;post_count\&quot;:1,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;moderator\&quot;:true,\&quot;trust_level\&quot;:2},{\&quot;id\&quot;:167936,\&quot;username\&quot;:\&quot;alexhales324\&quot;,\&quot;name\&quot;:\&quot;Alexhales324\&quot;,\&quot;avatar_template\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/a/ee7513/{size}.png\&quot;,\&quot;post_count\&quot;:1,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;trust_level\&quot;:0},{\&quot;id\&quot;:132700,\&quot;username\&quot;:\&quot;obinnae\&quot;,\&quot;name\&quot;:\&quot;Obinnae\&quot;,\&quot;avatar_template\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/o/a183cd/{size}.png\&quot;,\&quot;post_count\&quot;:1,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;trust_level\&quot;:2},{\&quot;id\&quot;:166120,\&quot;username\&quot;:\&quot;AiAbdrahim\&quot;,\&quot;name\&quot;:\&quot;Ai Abdrahim\&quot;,\&quot;avatar_template\&quot;:\&quot;/user_avatar/forum.ionicframework.com/aiabdrahim/{size}/134644_2.png\&quot;,\&quot;post_count\&quot;:1,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;trust_level\&quot;:1},{\&quot;id\&quot;:164600,\&quot;username\&quot;:\&quot;Karthik-V-V\&quot;,\&quot;name\&quot;:\&quot;Karthik V V\&quot;,\&quot;avatar_template\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/k/76d3ee/{size}.png\&quot;,\&quot;post_count\&quot;:1,\&quot;primary_group_name\&quot;:null,\&quot;flair_name\&quot;:null,\&quot;flair_url\&quot;:null,\&quot;flair_color\&quot;:null,\&quot;flair_bg_color\&quot;:null,\&quot;trust_level\&quot;:1}],\&quot;created_by\&quot;:{\&quot;id\&quot;:148822,\&quot;username\&quot;:\&quot;SwapnilP133\&quot;,\&quot;name\&quot;:\&quot;Swapnil P133\&quot;,\&quot;avatar_template\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/s/a9adbd/{size}.png\&quot;},\&quot;last_poster\&quot;:{\&quot;id\&quot;:171894,\&quot;username\&quot;:\&quot;TomaEduard\&quot;,\&quot;name\&quot;:\&quot;Toma Eduard\&quot;,\&quot;avatar_template\&quot;:\&quot;https://avatars.discourse-cdn.com/v4/letter/t/82dd89/{size}.png\&quot;},\&quot;links\&quot;:[{\&quot;url\&quot;:\&quot;https://github.com/ionic-team/capacitor/issues/324\&quot;,\&quot;title\&quot;:\&quot;Support building from CLI · Issue #324 · ionic-team/capacitor · GitHub\&quot;,\&quot;internal\&quot;:false,\&quot;attachment\&quot;:false,\&quot;reflection\&quot;:false,\&quot;clicks\&quot;:667,\&quot;user_id\&quot;:106489,\&quot;domain\&quot;:\&quot;github.com\&quot;,\&quot;root_domain\&quot;:\&quot;github.com\&quot;},{\&quot;url\&quot;:\&quot;https://docs.oracle.com/en/java/javase/14/docs/specs/man/jarsigner.html\&quot;,\&quot;title\&quot;:\&quot;The jarsigner Command\&quot;,\&quot;internal\&quot;:false,\&quot;attachment\&quot;:false,\&quot;reflection\&quot;:false,\&quot;clicks\&quot;:200,\&quot;user_id\&quot;:162375,\&quot;domain\&quot;:\&quot;docs.oracle.com\&quot;,\&quot;root_domain\&quot;:\&quot;oracle.com\&quot;},{\&quot;url\&quot;:\&quot;https://nsrtechx.com/run-cordova-without-installing-android-studio/\&quot;,\&quot;title\&quot;:\&quot;Run cordova without android studio\&quot;,\&quot;internal\&quot;:false,\&quot;attachment\&quot;:false,\&quot;reflection\&quot;:false,\&quot;clicks\&quot;:103,\&quot;user_id\&quot;:167575,\&quot;domain\&quot;:\&quot;nsrtechx.com\&quot;,\&quot;root_domain\&quot;:\&quot;nsrtechx.com\&quot;},{\&quot;url\&quot;:\&quot;https://docs.gradle.org/5.6.4/release-notes.html\&quot;,\&quot;title\&quot;:\&quot;Gradle 5.6.4 Release Notes\&quot;,\&quot;internal\&quot;:false,\&quot;attachment\&quot;:false,\&quot;reflection\&quot;:false,\&quot;clicks\&quot;:4,\&quot;user_id\&quot;:168150,\&quot;domain\&quot;:\&quot;docs.gradle.org\&quot;,\&quot;root_domain\&quot;:\&quot;gradle.org\&quot;},{\&quot;url\&quot;:\&quot;https://help.gradle.org\&quot;,\&quot;title\&quot;:null,\&quot;internal\&quot;:false,\&quot;attachment\&quot;:false,\&quot;reflection\&quot;:false,\&quot;clicks\&quot;:2,\&quot;user_id\&quot;:168150,\&quot;domain\&quot;:\&quot;help.gradle.org\&quot;,\&quot;root_domain\&quot;:\&quot;gradle.org\&quot;}]}}&quot;}"></div>
    <link rel="preload" href="https://aws1.discourse-cdn.com/ionicframework/assets/start-discourse-efa4e5abfbd1b50b5152ffbe64d5dcea9f7c33f766dcc6387e2711f0f2112148.br.js" as="script">
<script src="https://aws1.discourse-cdn.com/ionicframework/assets/start-discourse-efa4e5abfbd1b50b5152ffbe64d5dcea9f7c33f766dcc6387e2711f0f2112148.br.js"></script>


    

    <link rel="preload" href="https://aws1.discourse-cdn.com/ionicframework/assets/browser-update-eec13eb6f8386f18f10b5dd6ebb7a3598d28421bb796e539b91a7e4a4c5d4c08.br.js" as="script">
<script src="https://aws1.discourse-cdn.com/ionicframework/assets/browser-update-eec13eb6f8386f18f10b5dd6ebb7a3598d28421bb796e539b91a7e4a4c5d4c08.br.js"></script>


      

      
  </body>
</html>
