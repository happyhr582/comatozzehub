<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Subscription + 20 Ads + Redirect</title>
<script src="https://cdn.tailwindcss.com"></script>
<style>
body{box-sizing:border-box;margin:0;}
.neon-bg{background:linear-gradient(45deg,#0f0f23,#1a1a2e,#16213e,#0f3460);
background-size:400% 400%;animation:gradientShift 8s ease infinite;}
@keyframes gradientShift{0%,100%{background-position:0% 50%;}50%{background-position:100% 50%;}}
.ad-banner{background:rgba(0,0,0,0.3);color:#0ff;text-align:center;font-weight:bold;
padding:8px;border:1px dashed #0ff;border-radius:10px;font-family:sans-serif;}
.ad-container{position:fixed;z-index:1000;}
.ad-top{top:0;left:0;right:0;}
.ad-bottom{bottom:0;left:0;right:0;}
.ad-left{top:50%;left:10px;transform:translateY(-50%);width:120px;}
.ad-right{top:50%;right:10px;transform:translateY(-50%);width:120px;}
.video-popup{display:none;position:fixed;top:0;left:0;width:100%;height:100%;
background:rgba(0,0,0,0.9);z-index:2000;justify-content:center;align-items:center;flex-direction:column;}
.video-popup video{width:80%;border:3px solid #0ff;border-radius:20px;}
.pulse-glow{
  background:#0ff;color:#000;font-weight:bold;padding:10px 30px;border-radius:10px;
  cursor:pointer;animation:pulse 1.5s ease-in-out infinite alternate;
}
@keyframes pulse{
  from{box-shadow:0 0 10px #0ff,0 0 20px #0ff;}
  to{box-shadow:0 0 25px #0ff,0 0 45px #0ff;}
}
.ad-meta{font-size:11px;color:#7ff;padding-top:6px;display:block;word-break:break-all;}
.ad-sim{margin-top:6px;background:rgba(255,255,255,0.03);padding:6px;border-radius:6px;color:#bff;font-size:12px;}
.video-ad-container {
    position: relative;
    width: 640px;
    height: 360px;
    background: #000;
    margin: 20px auto;
}
</style>
<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-2029062882510569"
 crossorigin="anonymous"></script>
</head>
<body class="neon-bg min-h-screen relative">

<!-- fixed banners -->
<div class="ad-container ad-top ad-banner">
    <ins class="adsbygoogle"
         style="display:block"
         data-ad-client="ca-pub-2029062882510569"
         data-ad-slot="6284780310"
         data-ad-format="auto"
         data-full-width-responsive="true"></ins>
    <script>
         (adsbygoogle = window.adsbygoogle || []).push({});
    </script>
</div>
<div class="ad-container ad-bottom ad-banner" data-ad-unit="ca-app-pub-2029062882510569/9142043799">Ad 2 Bottom</div>
<div class="ad-container ad-left ad-banner" data-ad-unit="ca-app-pub-2029062882510569/1032453630">Ad 3 Left</div>
<div class="ad-container ad-right ad-banner" data-ad-unit="ca-app-pub-2029062882510569/8224725555">Ad 4 Right</div>

<main class="container mx-auto px-4 py-12 relative z-10 text-center">
<h1 class="text-5xl font-bold bg-gradient-to-r from-cyan-400 via-purple-500 to-pink-500 bg-clip-text text-transparent mb-4">
Comatozze Subscription</h1>
<p class="text-xl text-cyan-300 mb-8">Choose your plan and enjoy premium videos</p>

<!-- inline ad rows -->
<div class="grid grid-cols-2 md:grid-cols-4 gap-4 mb-6">
  <div class="ad-banner" data-ad-unit="ca-app-pub-2029062882510569/7707303504">Ad 5</div>
  <div class="ad-banner" data-ad-unit="ca-app-pub-2029062882510569/5598562219">Ad 6</div>
  <div class="ad-banner" data-ad-unit="ca-app-pub-2029062882510569/6309008655">Ad 7</div>
  <div class="ad-banner" data-ad-unit="ca-app-pub-2029062882510569/2726439561">Ad 8</div>
</div>

<div class="max-w-4xl mx-auto grid md:grid-cols-2 gap-8">
<div class="bg-gradient-to-br from-gray-900/80 to-black/80 rounded-3xl p-8 border-2 border-cyan-500/50 neon-glow">
<h2 class="text-2xl font-bold text-white mb-2">One Time Access</h2>
<p class="text-cyan-300 mb-4">?299 single payment</p>
<!-- Pay button opens video ad (video ad unit: ca-app-pub-2029062882510569/6226700870) -->
<a href="#" onclick="showVideoAd('ca-app-pub-2029062882510569/6226700870')" class="bg-gradient-to-r from-cyan-500 to-blue-600 text-white font-bold py-4 px-6 rounded-2xl inline-block">Pay ?299</a>
</div>
<div class="bg-gradient-to-br from-purple-900/80 to-pink-900/80 rounded-3xl p-8 border-2 border-purple-500/50 neon-glow">
<h2 class="text-2xl font-bold text-white mb-2">Lifetime Access</h2>
<p class="text-purple-300 mb-4">?499 forever access</p>
<!-- Pay button opens second video ad (video ad unit: ca-app-pub-2029062882510569/4832275452) -->
<a href="#" onclick="showVideoAd('ca-app-pub-2029062882510569/4832275452')" class="bg-gradient-to-r from-purple-500 to-pink-600 text-white font-bold py-4 px-6 rounded-2xl inline-block">Pay ?499</a>
</div>
</div>

<!-- more ad placeholders -->
<div class="grid grid-cols-2 md:grid-cols-4 gap-4 mt-10">
  <div class="ad-banner" data-ad-unit="ca-app-pub-2029062882510569/5901636930">Ad 9</div>
  <div class="ad-banner" data-ad-unit="ca-app-pub-2029062882510569/3275473598">Ad 10</div>
  <div class="ad-banner" data-ad-unit="ca-app-pub-2029062882510569/1467745512">Ad 11</div>
  <div class="ad-banner" data-ad-unit="ca-app-pub-2029062882510569/1276173821">Ad 12</div>
  <div class="ad-banner" data-ad-unit="ca-app-pub-2029062882510569/3682845317">Ad 13</div>
  <div class="ad-banner" data-ad-unit="ca-app-pub-2029062882510569/6336928815">Ad 14</div>
  <div class="ad-banner" data-ad-unit="ca-app-pub-2029062882510569/6801415942">Ad 15</div>
  <div class="ad-banner" data-ad-unit="ca-app-pub-2029062882510569/7850773738">Ad 16</div>
  <div class="ad-banner" data-ad-unit="ca-app-pub-2029062882510569/6609844252">Ad 17</div>
  <div class="ad-banner" data-ad-unit="ca-app-pub-2029062882510569/2237901700">Ad 18</div>
  <div class="ad-banner" data-ad-unit="ca-app-pub-2029062882510569/5105190894">Ad 19</div>
  <div class="ad-banner" data-ad-unit="ca-app-pub-2029062882510569/9238246710">Ad 20</div>
</div>

<div id="paymentStatus" class="max-w-2xl mx-auto mt-12 p-6 rounded-xl text-center hidden"></div>
</main>

<!-- popup video -->
<div class="video-popup" id="videoAd" data-video-unit="">
  <video id="adVideo" controls>
    <source src="https://www.w3schools.com/html/mov_bbb.mp4" type="video/mp4" />
  </video>
  <div class="ad-meta" id="videoAdMeta"></div>
  <div class="pulse-glow" id="continueBtn" onclick="redirectFiverr()">Continue</div>
</div>

<script>
// Render ad placeholders (safe/demo rendering)
// Each .ad-banner should show its configured ad unit id. In a real integration,
// replace this with the correct AdMob/AdSense scripts and tags for web or apps.
(function renderAdPlaceholders(){
  const ads = document.querySelectorAll('.ad-banner');
  ads.forEach((el, idx) => {
    const unit = el.getAttribute('data-ad-unit') || ('ad-unit-missing-'+(idx+1));
    // add visible meta for debugging/demo
    const meta = document.createElement('span');
    meta.className = 'ad-meta';
    meta.textContent = 'Unit: ' + unit;
    const sim = document.createElement('div');
    sim.className = 'ad-sim';
    sim.textContent = 'Simulated ad creative for ' + unit;
    el.appendChild(meta);
    el.appendChild(sim);
    // For local demo: log to console
    console.log('Ad placeholder rendered:', unit);
  });
})();

// Video ad handling: show popup and attach the video ad unit id to the popup for tracking
function showVideoAd(videoUnit) {
    // Initialize the video ad
    const videoAdContainer = document.getElementById('videoAd');
    
    // Create video ad slot
    const adContainer = document.createElement('div');
    adContainer.className = 'video-ad-container';
    
    const videoAd = document.createElement('ins');
    videoAd.className = 'adsbygoogle';
    videoAd.style.display = 'block';
    videoAd.dataset.adClient = 'ca-pub-2029062882510569';
    videoAd.dataset.adSlot = videoUnit;
    videoAd.dataset.adFormat = 'video';
    
    adContainer.appendChild(videoAd);
    videoAdContainer.appendChild(adContainer);
    
    // Push the ad
    (adsbygoogle = window.adsbygoogle || []).push({
        callback: function(r) {
            // After video ad completes
            videoAdContainer.style.display = 'none';
            redirectFiverr();
        }
    });
    
    videoAdContainer.style.display = 'flex';
}

// Close popup and redirect (simulate completion)
function redirectFiverr(){
  const popup = document.getElementById('videoAd');
  const vid = document.getElementById('adVideo');
  const unit = popup.getAttribute('data-video-unit') || 'unknown';
  // stop video
  vid.pause();
  popup.style.display = 'none';
  console.log('Video ad closed. Unit:', unit);
  // simulated post-ad action
  window.location.href = "https://www.fiverr.com/";
}


</body></script></html>
