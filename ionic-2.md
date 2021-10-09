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
