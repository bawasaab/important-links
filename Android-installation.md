<h2 id="linux" data-text="Linux" role="presentation"><span class="devsite-heading" role="heading" aria-level="2">Linux</span><button type="button" class="devsite-heading-link button-flat material-icons" aria-label="Copy link to this section: Linux" data-title="Copy link to this section: Linux" data-id="linux"></button></h2>

<p>To install Android Studio on Linux, proceed as follows:</p>

<ol>
  <li>Unpack the <code translate="no" dir="ltr">.zip</code> file you downloaded to an
      appropriate location for your applications, such as within
      <code translate="no" dir="ltr">/usr/local/</code> for your user profile, or <code translate="no" dir="ltr">/opt/</code>
      for shared users.
    <p>
      If you're using a 64-bit version of Linux, make sure you first install the
      <a href="#64bit-libs">required libraries for 64-bit machines</a>.
    </p>
  </li><li>To launch Android Studio, open a terminal,
    navigate to the <code translate="no" dir="ltr">android-studio/bin/</code> directory,
   and execute <code translate="no" dir="ltr">studio.sh</code>.
  </li>
  <li>Select whether you want to import previous Android Studio settings
    or not, then click <strong>OK</strong>.</li>
  <li>The Android Studio Setup Wizard guides you through the rest of the
    setup, which includes downloading Android SDK components
    that are required for development.</li>
</ol>


<h3 id="64bit-libs" data-text="   Required libraries for 64-bit machines " role="presentation"><span class="devsite-heading" role="heading" aria-level="3">
  Required libraries for 64-bit machines
</span><button type="button" class="devsite-heading-link button-flat material-icons" aria-label="Copy link to this section: 
  Required libraries for 64-bit machines
" data-title="Copy link to this section: 
  Required libraries for 64-bit machines
" data-id="64bit-libs"></button></h3>


<p>If you are running a 64-bit version of Ubuntu, you need to install some 32-bit
libraries with the following command:</p>


<devsite-code data-copy-event-label=""><div class="devsite-code-buttons-container" role="group" aria-label="Action buttons"><button type="button" class="gc-analytics-event material-icons devsite-icon-code-dark devsite-toggle-dark" data-category="Site-Wide Custom Events" data-label="Dark Code Toggle" track-type="exampleCode" track-name="darkCodeToggle" aria-label="Dark code theme" data-title="Dark code theme"></button><button type="button" class="gc-analytics-event material-icons devsite-icon-code-light devsite-toggle-light" data-category="Site-Wide Custom Events" data-label="Light Code Toggle" track-type="exampleCode" track-name="lightCodeToggle" aria-label="Light code theme" data-title="Light code theme"></button><button type="button" class="gc-analytics-event material-icons devsite-icon-copy" data-category="Site-Wide Custom Events" data-label="Click To Copy" track-type="exampleCode" track-name="clickToCopy" aria-label="Copy code sample" data-title="Copy code sample"></button></div><pre class="none devsite-terminal" translate="no" dir="ltr" is-upgraded="">sudo apt-get install libc6:i386 libncurses5:i386 libstdc++6:i386 lib32z1 libbz2-1.0:i386
</pre></devsite-code>


<p>That's it.
The following video shows each step of the recommended setup procedure.</p>


<devsite-code data-copy-event-label=""><div class="devsite-code-buttons-container" role="group" aria-label="Action buttons"><button type="button" class="gc-analytics-event material-icons devsite-icon-code-dark devsite-toggle-dark" data-category="Site-Wide Custom Events" data-label="Dark Code Toggle" track-type="exampleCode" track-name="darkCodeToggle" aria-label="Dark code theme" data-title="Dark code theme"></button><button type="button" class="gc-analytics-event material-icons devsite-icon-code-light devsite-toggle-light" data-category="Site-Wide Custom Events" data-label="Light Code Toggle" track-type="exampleCode" track-name="lightCodeToggle" aria-label="Light code theme" data-title="Light code theme"></button><button type="button" class="gc-analytics-event material-icons devsite-icon-copy" data-category="Site-Wide Custom Events" data-label="Click To Copy" track-type="exampleCode" track-name="clickToCopy" aria-label="Copy code sample" data-title="Copy code sample"></button></div><pre class="none devsite-terminal" translate="no" dir="ltr" is-upgraded="">sudo yum install zlib.i686 ncurses-libs.i686 bzip2-libs.i686
</pre></devsite-code>
