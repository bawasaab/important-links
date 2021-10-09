<div class="crayons-article__main">

          <div class="crayons-article__body text-styles spec__body" data-article-id="732489" id="article-body">
            <p>Ionic 5's official documentation recommends <a href="https://ionicframework.com/docs/angular/your-first-app/6-deploying-mobile#android-deployment">using Android Studio to build</a> the project. However, I can think of a few reasons to sidestep Android Studio in the build process:</p>

<ul>
<li>Android Studio is relatively resource-intensive</li>
<li>A command-line method could be simpler and faster than opening up a full-blown Android development environment</li>
<li>Using Android Studio just for the build process might break your workflow, if you've gotten comfortable with your existing development chain, say VScode and the CLI tools</li>
</ul>

<p>Whatever your reasons are, Android apks could be built from your Ionic 5 project with a few extra commands. Before building, you can test if your app runs fine in the browser with this command:<br>
</p>

<div class="highlight js-code-highlight">
<pre class="highlight shell"><code>ionic serve
</code></pre>
<div class="highlight__panel js-actions-panel">
<div class="highlight__panel-action js-fullscreen-code-action">
    <svg xmlns="http://www.w3.org/2000/svg" width="20px" height="20px" viewBox="0 0 24 24" class="highlight-action crayons-icon highlight-action--fullscreen-on">
    <path d="M16 3h6v6h-2V5h-4V3zM2 3h6v2H4v4H2V3zm18 16v-4h2v6h-6v-2h4zM4 19h4v2H2v-6h2v4z"></path>
</svg>

    <svg xmlns="http://www.w3.org/2000/svg" width="20px" height="20px" viewBox="0 0 24 24" class="highlight-action crayons-icon highlight-action--fullscreen-off"><title>Exit fullscreen mode</title>
    <path d="M18 7h4v2h-6V3h2v4zM8 9H2V7h4V3h2v6zm10 8v4h-2v-6h6v2h-4zM8 15v6H6v-4H2v-2h6z"></path>
</svg>

</div>
</div>
</div>



<p>If you don't have an Ionic 5 project ready, create a blank project with this command:<br>
</p>

<div class="highlight js-code-highlight">
<pre class="highlight shell"><code>ionic start sample-ionic-angular-app blank <span class="nt">--type</span><span class="o">=</span>angular <span class="nt">--capacitor</span>
</code></pre>
<div class="highlight__panel js-actions-panel">
<div class="highlight__panel-action js-fullscreen-code-action">
    <svg xmlns="http://www.w3.org/2000/svg" width="20px" height="20px" viewBox="0 0 24 24" class="highlight-action crayons-icon highlight-action--fullscreen-on">
    <path d="M16 3h6v6h-2V5h-4V3zM2 3h6v2H4v4H2V3zm18 16v-4h2v6h-6v-2h4zM4 19h4v2H2v-6h2v4z"></path>
</svg>

    <svg xmlns="http://www.w3.org/2000/svg" width="20px" height="20px" viewBox="0 0 24 24" class="highlight-action crayons-icon highlight-action--fullscreen-off"><title>Exit fullscreen mode</title>
    <path d="M18 7h4v2h-6V3h2v4zM8 9H2V7h4V3h2v6zm10 8v4h-2v-6h6v2h-4zM8 15v6H6v-4H2v-2h6z"></path>
</svg>

</div>
</div>
</div>



<p>Refer to <a href="https://ionicframework.com/docs/angular/your-first-app">Ionic 5's first app docs</a> for more details on how to get started with Ionic app development.</p>

<p><strong>Step 1</strong>: Build the Ionic project<br>
</p>

<div class="highlight js-code-highlight">
<pre class="highlight shell"><code>ionic build
</code></pre>
<div class="highlight__panel js-actions-panel">
<div class="highlight__panel-action js-fullscreen-code-action">
    <svg xmlns="http://www.w3.org/2000/svg" width="20px" height="20px" viewBox="0 0 24 24" class="highlight-action crayons-icon highlight-action--fullscreen-on"><title>Enter fullscreen mode</title>
    <path d="M16 3h6v6h-2V5h-4V3zM2 3h6v2H4v4H2V3zm18 16v-4h2v6h-6v-2h4zM4 19h4v2H2v-6h2v4z"></path>
</svg>

    <svg xmlns="http://www.w3.org/2000/svg" width="20px" height="20px" viewBox="0 0 24 24" class="highlight-action crayons-icon highlight-action--fullscreen-off"><title>Exit fullscreen mode</title>
    <path d="M18 7h4v2h-6V3h2v4zM8 9H2V7h4V3h2v6zm10 8v4h-2v-6h6v2h-4zM8 15v6H6v-4H2v-2h6z"></path>
</svg>

</div>
</div>
</div>



<p><strong>Step 2</strong>: Add support for the Android platform<br>
</p>

<div class="highlight js-code-highlight">
<pre class="highlight shell"><code>ionic capacitor add android
</code></pre>
<div class="highlight__panel js-actions-panel">
<div class="highlight__panel-action js-fullscreen-code-action">
    <svg xmlns="http://www.w3.org/2000/svg" width="20px" height="20px" viewBox="0 0 24 24" class="highlight-action crayons-icon highlight-action--fullscreen-on"><title>Enter fullscreen mode</title>
    <path d="M16 3h6v6h-2V5h-4V3zM2 3h6v2H4v4H2V3zm18 16v-4h2v6h-6v-2h4zM4 19h4v2H2v-6h2v4z"></path>
</svg>

    <svg xmlns="http://www.w3.org/2000/svg" width="20px" height="20px" viewBox="0 0 24 24" class="highlight-action crayons-icon highlight-action--fullscreen-off"><title>Exit fullscreen mode</title>
    <path d="M18 7h4v2h-6V3h2v4zM8 9H2V7h4V3h2v6zm10 8v4h-2v-6h6v2h-4zM8 15v6H6v-4H2v-2h6z"></path>
</svg>

</div>
</div>
</div>



<p><strong>Step 3</strong>: Sync changes from your Ionic project to the Android part<br>
</p>

<div class="highlight js-code-highlight">
<pre class="highlight shell"><code>ionic capacitor <span class="nb">sync</span>
</code></pre>
<div class="highlight__panel js-actions-panel">
<div class="highlight__panel-action js-fullscreen-code-action">
    <svg xmlns="http://www.w3.org/2000/svg" width="20px" height="20px" viewBox="0 0 24 24" class="highlight-action crayons-icon highlight-action--fullscreen-on"><title>Enter fullscreen mode</title>
    <path d="M16 3h6v6h-2V5h-4V3zM2 3h6v2H4v4H2V3zm18 16v-4h2v6h-6v-2h4zM4 19h4v2H2v-6h2v4z"></path>
</svg>

    <svg xmlns="http://www.w3.org/2000/svg" width="20px" height="20px" viewBox="0 0 24 24" class="highlight-action crayons-icon highlight-action--fullscreen-off"><title>Exit fullscreen mode</title>
    <path d="M18 7h4v2h-6V3h2v4zM8 9H2V7h4V3h2v6zm10 8v4h-2v-6h6v2h-4zM8 15v6H6v-4H2v-2h6z"></path>
</svg>

</div>
</div>
</div>



<p><strong>Step 4</strong>: Build for Android and generate apk<br>
</p>

<div class="highlight js-code-highlight">
<pre class="highlight shell"><code><span class="nb">cd </span>android <span class="o">&amp;&amp;</span> ./gradlew assembleDebug <span class="o">&amp;&amp;</span> <span class="nb">cd</span> ..
</code></pre>
<div class="highlight__panel js-actions-panel">
<div class="highlight__panel-action js-fullscreen-code-action">
    <svg xmlns="http://www.w3.org/2000/svg" width="20px" height="20px" viewBox="0 0 24 24" class="highlight-action crayons-icon highlight-action--fullscreen-on"><title>Enter fullscreen mode</title>
    <path d="M16 3h6v6h-2V5h-4V3zM2 3h6v2H4v4H2V3zm18 16v-4h2v6h-6v-2h4zM4 19h4v2H2v-6h2v4z"></path>
</svg>

    <svg xmlns="http://www.w3.org/2000/svg" width="20px" height="20px" viewBox="0 0 24 24" class="highlight-action crayons-icon highlight-action--fullscreen-off"><title>Exit fullscreen mode</title>
    <path d="M18 7h4v2h-6V3h2v4zM8 9H2V7h4V3h2v6zm10 8v4h-2v-6h6v2h-4zM8 15v6H6v-4H2v-2h6z"></path>
</svg>

</div>
</div>
</div>



<p>If the build completes successfully, you'll find your app's apk at <code>android/app/build/outputs/apk/debug/app-debug.apk</code>. From now on, whenever you need to build for Android, you need to repeat only steps 3 and 4.</p>

<h2>
  <a name="credits-amp-sources" href="#credits-amp-sources">
  </a>
  Credits &amp; Sources
</h2>

<ul>
<li><a href="https://forum.ionicframework.com/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814/9">How to build an Android APK file without using Android Studio in a Capacitor project?</a></li>
<li>Cover image created from logos of <a href="https://source.android.com/setup/start/brands">Android</a> and <a href="https://commons.wikimedia.org/wiki/File:Ionic_Logo.svg">Ionic</a>
</li>
</ul>


          </div>

        </div>


<br>
<br>
<br>
<br>


<div class="regular contents"><div class="cooked"><p dir="ltr">I was having this issue and the way I worked out to do this:</p>
<p dir="ltr">You need to add android first:</p>
<pre dir="ltr"><code class="hljs csharp" dir="ltr">ionic capacitor <span class="hljs-keyword">add</span> android 
</code></pre>
<pre dir="ltr"><code class="hljs bash" dir="ltr">ionic capacitor copy android &amp;&amp; <span class="hljs-built_in">cd</span> android &amp;&amp; ./gradlew assembleDebug &amp;&amp; <span class="hljs-built_in">cd</span> ..
</code></pre>
<p dir="ltr">Then your apk will be at:</p>
<pre dir="ltr"><code class="hljs lua" dir="ltr">android/app/build/outputs/apk/<span class="hljs-built_in">debug</span>/app-<span class="hljs-built_in">debug</span>.apk
</code></pre>
<p dir="ltr">If you want to run on device directly from command line:</p>
<pre dir="ltr"><code class="hljs bash" dir="ltr">ionic capacitor copy android &amp;&amp; <span class="hljs-built_in">cd</span> android &amp;&amp; ./gradlew assembleDebug &amp;&amp; ./gradlew installDebug &amp;&amp; <span class="hljs-built_in">cd</span> ..
</code></pre>
<p dir="ltr">Note: It doesn’t work without entering the android directory</p>
<p dir="ltr">I hope that helps!</p></div><section class="post-menu-area clearfix"><nav class="post-controls expanded"><button class="widget-button btn-flat show-replies btn-icon-text" aria-label="7 Replies" title="7 Replies"><span class="d-button-label">7 Replies</span><svg class="fa d-icon d-icon-chevron-down svg-icon svg-node" aria-hidden="true"><use xlink:href="#chevron-down"></use></svg></button><div class="actions"><div class="double-button"><button class="widget-button btn-flat button-count like-count highlight-action regular-likes btn-text" aria-label="20 people liked this post" title="20 people liked this post">20</button><button class="widget-button btn-flat toggle-like like no-text btn-icon" aria-label="like this post" title="like this post"><svg class="fa d-icon d-icon-d-unliked svg-icon svg-node" aria-hidden="true"><use xlink:href="#far-heart"></use></svg></button></div><button class="widget-button btn-flat share no-text btn-icon" aria-label="share a link to this post" title="share a link to this post" data-share-url="/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814/9" data-post-number="9"><svg class="fa d-icon d-icon-link svg-icon svg-node" aria-hidden="true"><use xlink:href="#link"></use></svg></button></div></nav></section></div>

<br>
<br>
<br>
<br>
<br>
<br>
<br>

<div class="regular contents"><div class="cooked"><p dir="ltr">Here is how to production build for Android:</p>
<pre dir="ltr"><code class="hljs sql" dir="ltr">cd android <span class="hljs-operator">&amp;&amp;</span> 
.<span class="hljs-operator">/</span>gradlew assembleRelease <span class="hljs-operator">&amp;&amp;</span> 
cd app<span class="hljs-operator">/</span>build<span class="hljs-operator">/</span>outputs<span class="hljs-operator">/</span>apk<span class="hljs-operator">/</span><span class="hljs-keyword">release</span> <span class="hljs-operator">&amp;&amp;</span>
jarsigner <span class="hljs-operator">-</span>keystore YOUR_KEYSTORE_PATH <span class="hljs-operator">-</span>storepass YOUR_KEYSTORE_PASS app<span class="hljs-operator">-</span><span class="hljs-keyword">release</span><span class="hljs-operator">-</span>unsigned.apk YOUR_KEYSTORE_ALIAS <span class="hljs-operator">&amp;&amp;</span>
zipalign <span class="hljs-number">4</span> app<span class="hljs-operator">-</span><span class="hljs-keyword">release</span><span class="hljs-operator">-</span>unsigned.apk app<span class="hljs-operator">-</span>release.apk
</code></pre>
<p dir="ltr">This will generate <code dir="ltr">app-release.apk</code> which should be good to go the play store (see <code dir="ltr">android/app/build/outputs/apk/release</code> folder).</p>
<p dir="ltr">Here is the jarsigner command <a href="https://docs.oracle.com/en/java/javase/14/docs/specs/man/jarsigner.html" rel="nofollow noopener" dir="ltr">manual <span class="badge badge-notification clicks" title="200 clicks" dir="ltr">201</span></a>.</p></div><section class="post-menu-area clearfix"><nav class="post-controls expanded"><button class="widget-button btn-flat show-replies btn-icon-text" aria-label="2 Replies" title="2 Replies"><span class="d-button-label">2 Replies</span><svg class="fa d-icon d-icon-chevron-down svg-icon svg-node" aria-hidden="true"><use xlink:href="#chevron-down"></use></svg></button><div class="actions"><div class="double-button"><button class="widget-button btn-flat button-count like-count highlight-action regular-likes btn-text" aria-label="9 people liked this post" title="9 people liked this post">9</button><button class="widget-button btn-flat toggle-like like no-text btn-icon" aria-label="like this post" title="like this post"><svg class="fa d-icon d-icon-d-unliked svg-icon svg-node" aria-hidden="true"><use xlink:href="#far-heart"></use></svg></button></div><button class="widget-button btn-flat share no-text btn-icon" aria-label="share a link to this post" title="share a link to this post" data-share-url="/t/how-to-build-an-android-apk-file-without-using-android-studio-in-a-capacitor-project/177814/12" data-post-number="12"><svg class="fa d-icon d-icon-link svg-icon svg-node" aria-hidden="true"><use xlink:href="#link"></use></svg></button></div></nav></section></div>
